# Nuchain Migration Plugin

The migration plugin can be used to migrate data from a stand-alone to a parachain.

This code based on [Centrifuge migration plugin](https://github.com/centrifuge/centrifuge-cli/tree/main/packages/plugins/migration)
with some modifications for nuchain specific types and functionality.

## How to Use

The plugin expects a few parameters to be provided as also two json-files defining the migration
itself.

### Arguments

1. The ws-endpoint from where the data shall be fetched
2. The ws-endpoint to where the data shall be migrated

### Flags

* -b/--block : Defines the blocknumber the state is fetched at. If not defined latest is used.
* --config : Defines the modules and the sequence of migration for them. 
  
    Example for Altair:
    ```json
    [
      {
        "source": {
          "pallet": "Balances",
          "item": "TotalIssuance"
        },
        "destination": {
          "pallet": "Balances",
          "item": "TotalIssuance"
        }
      },
      {
        "source": {
          "pallet": "System",
          "item": "Account"
        },
        "destination": {
          "pallet": "System",
          "item": "Account"
        }
      }
    ]
    ```
* --creds : Credentials that will be used to execute the extriniscs. I.e. the root-key.
    ```json
    {
    "rawSeed": "//Alice"
    }
    ```
* --verify : If flag is given, the migration will be verified directly afterwards.
* --just-verify : This option expects a path to a json file of the following form in order to verify a past migration.
    ```json
    export interface MigrationSummary {
      fromFetchedAt: string,
      fromStartedAt: string,
      toStartedAt: string
      toEndAt: string,
    }
    ```
  
* --finalize : If flag is present, then the call-filters will be disabled after the migration.

An exemplary command will look like this:
```shell
migration \
  node packages/cli/bin/run migration \
    wss://sg.node.nuchain.network \
    ws://127.0.0.1:9944 \
    -b 7295085 \
    --config config/migration-modules.json \
    --creds creds.json \
    --verify
```
