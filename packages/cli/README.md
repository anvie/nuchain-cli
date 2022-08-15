nuchain-cli
==============

Nuchain-cli tool. Allows to interact with different components of the nuchain infrastructure and provides different tools as plugins.

[![oclif](https://img.shields.io/badge/cli-oclif-brightgreen.svg)](https://oclif.io)
[![Version](https://img.shields.io/npm/v/nuchain-cli.svg)](https://npmjs.org/package/nuchain-cli)
[![Downloads/week](https://img.shields.io/npm/dw/nuchain-cli.svg)](https://npmjs.org/package/nuchain-cli)
[![License](https://img.shields.io/npm/l/nuchain-cli.svg)](https://github.com/nuchain/nuchain-cli/blob/master/package.json)

<!-- toc -->
* [Usage](#usage)
* [Commands](#commands)
<!-- tocstop -->
# Usage
<!-- usage -->
```sh-session
$ npm install -g nuchain-cli
$ nuchain COMMAND
running command...
$ nuchain (-v|--version|version)
nuchain-cli/0.0.1 darwin-x64 node-v14.16.1
$ nuchain --help [COMMAND]
USAGE
  $ nuchain COMMAND
...
```
<!-- usagestop -->
# Commands
<!-- commands -->
* [`nuchain hello [FILE]`](#nuchain-hello-file)
* [`nuchain help [COMMAND]`](#nuchain-help-command)

## `nuchain hello [FILE]`

describe the command here

```
USAGE
  $ nuchain hello [FILE]

OPTIONS
  -f, --force
  -h, --help       show CLI help
  -n, --name=name  name to print

EXAMPLE
  $ nuchain hello
  hello world from ./src/hello.ts!
```

_See code: [src/commands/hello.ts](https://github.com/nuchain/nuchain-cli/blob/v0.0.1/src/commands/hello.ts)_

## `nuchain help [COMMAND]`

display help for nuchain

```
USAGE
  $ nuchain help [COMMAND]

ARGUMENTS
  COMMAND  command to show help for

OPTIONS
  --all  see all commands in CLI
```

_See code: [@oclif/plugin-help](https://github.com/oclif/plugin-help/blob/v3.2.3/src/commands/help.ts)_
<!-- commandsstop -->
