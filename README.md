# testen [![NPM version](https://img.shields.io/npm/v/testen.svg)](https://npmjs.com/package/testen) [![NPM downloads](https://img.shields.io/npm/dm/testen.svg)](https://npmjs.com/package/testen) [![Build Status](https://img.shields.io/circleci/project/egoist/testen/master.svg)](https://circleci.com/gh/egoist/testen)

> Test JavaScript code in multi Node environments locally.

![preview](https://ooo.0o0.ooo/2016/02/16/56c2dec030097.png)

## Install

```
$ npm install -g testen
```

## Usage

```bash
$ testen -n 0.12.0 -n 4.2.4 -n 5.6.0 -- ava

# Using NVM instead of n?
$ testen -n 0.12.0 --nvm -- ava
```

## CLI

```bash
$ testen --help

Usage:

  --node/-n <version>:  Add a node version to test
  -- <command>:         The test command you expect
  --nvm:                Test with NVM
```

## License

MIT © [EGOIST](https://github.com/egoist)
