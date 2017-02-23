# testen [![NPM version](https://img.shields.io/npm/v/testen.svg)](https://npmjs.com/package/testen) [![NPM downloads](https://img.shields.io/npm/dm/testen.svg)](https://npmjs.com/package/testen)

[testen repo]: https://github.com/egoist/testen

Run tests for multiple versions of Node.js in local env.  

![preview](https://ooo.0o0.ooo/2016/04/17/571460f682122.gif)

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

# use system default node version
$ testen --system
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

## CLI

```bash
$ testen --help

Usage:

  --system:             Use current node version
  -n/--node [version]:  Add a node version to test
  -s, --sequence:       Run tests in sequence
  -- [command]:         The test command you expect
  -V/--verbose:         Always output everything
                          ~ example: there are `console.log` in test
```

## License

MIT © [EGOIST](https://github.com/egoist)
