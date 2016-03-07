# testen [![NPM version](https://img.shields.io/npm/v/testen.svg)](https://npmjs.com/package/testen) [![NPM downloads](https://img.shields.io/npm/dm/testen.svg)](https://npmjs.com/package/testen) ![testen badge](https://img.shields.io/badge/testen-passing-brightgreen.svg)

Run tests for multiple versions of Node.js in local env.  
Automatically update testen badge in your README after running tests.

![preview](https://ooo.0o0.ooo/2016/03/06/56dd033db2517.gif)

## Install

You should have `nvm` and `node >= 4` installed.

```bash
$ npm install -g testen
```

## Usage

```bash
$ testen
```

This will run `npm test` script, if `.travis.yml` or `circle.yml` exists, use node versions in it. Otherwise use [preset node versions](/lib/preset-versions.json).

Sometimes you wanna override these node versions, just pass `-n` to do this:

```bash
$ testen -n 0.10 -n 0.12
```

**Read Node.js versions from `package.json`**

```json
{
  "testen": {
    "node": ["0.12.0", "5", "4.2.4"]
  }
}
```

**Read test command from `package.json`**

```json
{
  "testen": {
    "test": "npm run test:custom"
  }
}
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
  --verbose/V:          Always output everything
                          ~ example: there are `console.log` in test
```

## License

MIT © [EGOIST](https://github.com/egoist)
