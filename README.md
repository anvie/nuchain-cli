# Welcome to Nuchain CLI

Tool to manage nuchain development, deployment, and migration.

## Setup
These are optional but highly recommended steps

* Install [nvm](https://github.com/nvm-sh/nvm)
* Run `nvm use`

## Build
All of the following commands must be run in the root directory of the repository.

* Install the dependencies:

```shell=
yarn install
```

* Build artifacts (this needs to be run everytime some code changes):

```shell=
lerna run build
```

## Run
Once the project has been built, you can choose to run it like so:

```bash
node packages/cli/bin/run <subcommand>
```
