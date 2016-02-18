# testen [![NPM version](https://img.shields.io/npm/v/testen.svg)](https://npmjs.com/package/testen) [![NPM downloads](https://img.shields.io/npm/dm/testen.svg)](https://npmjs.com/package/testen) ![testen badge](https://img.shields.io/badge/testen-passing-brightgreen.svg)

Run tests for multiple versions of Node.js in local env.  
Automatically update testen badge in your README after running tests.

![preview](https://ooo.0o0.ooo/2016/02/16/56c3365973b7f.gif)

## Install

```bash
# if you are using `n`
$ npm install -g testen@0.1

# if you are using `nvm`
$ npm install -g testen
```

## Usage

```bash
# use system's default node version to run `npm test`
$ testen

# multiple versions
# please ensure the version you wanna test with was already intalled
$ testen -n 4.2.4 -n 5.6.0 -n 0.12.0

# override test script, default is '-- npm test'
$ testen -n 0.12.0 -n 4.2.4 -n 5.6.0 -- ava
```

**Auto-update badge**

Add `![testen badge]()` to your `README.md` and it will automatically update the badge after running each test. Use `--disable-badge` or remove that mark to disable this behavior.

## CLI

```bash
$ testen --help

Usage:

	--node/-n [version]:  Add a node version to test
	-- [command]:         The test command you expect
	--disable-badge:      Disable auto-update testen badge
```

## License

MIT © [EGOIST](https://github.com/egoist)
