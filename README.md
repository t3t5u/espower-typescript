espower-typescript
====

> power-assert instrumentor for TypeScript

[![npm version][npm-image]][npm-url]
![Node.js Version Support][node-version]
[![build status][travis-image]][travis-url]
[![Dependency Status][deps-image]][deps-url]
![License][license]

## Install

```console
$ npm install -D espower-typescript
```

## TypeScript versions

* espower-typescript v8.x uses TypeScript v2.2
* espower-typescript v7.x uses TypeScript v2.1
* espower-typescript v6.x uses TypeScript v2.0
* espower-typescript v5.x uses TypeScript v1.8
* espower-typescript v4.x uses TypeScript v1.7
* espower-typescript v2.x and v3.x uses TypeScript v1.6
* espower-typescript v1.x uses TypeScript v1.5

## Usage

### Zero-config mode

```console
$ mocha --compilers ts:espower-typescript/guess test/**/*.ts
```

### If your tests are not in test dir

You can set test directory in your `package.json`

```json
{
    "name": "your-module",
    "description": "Your module",
    "version": "0.0.1",
    "directories": {
        "test": "spec/"
    },
...
}
```

Then, run mocha with `--compilers ts:espower-typescript/guess`

```console
$ mocha --compilers ts:espower-typescript/guess spec/**/*.ts
```

Note: `'espower-typescript/guess'` is inspired by [intelli-espower-loader](https://github.com/azu/intelli-espower-loader)

### tsconfig.json and CompilerOptions

If [tsconfig.json](https://github.com/Microsoft/TypeScript/wiki/tsconfig.json) is in your prject root, `'espower-typescript/guess'` loads it automatically.

Note: only `compilerOptions` field in tsconfig.json is applied.

### JSX/React

`.tsx` files are supported.

## License

* MIT License: Teppei Sato &lt;teppeis@gmail.com&gt;
* Includes [yosuke-furukawa/espower-traceur](https://github.com/yosuke-furukawa/espower-traceur)
* Includes [azu/espower-babel](https://github.com/azu/espower-babel)

[npm-image]: https://img.shields.io/npm/v/espower-typescript.svg
[npm-url]: https://npmjs.org/package/espower-typescript
[travis-image]: https://travis-ci.org/power-assert-js/espower-typescript.svg?branch=master
[travis-url]: https://travis-ci.org/power-assert-js/espower-typescript
[deps-image]: https://david-dm.org/power-assert-js/espower-typescript.svg
[deps-url]: https://david-dm.org/power-assert-js/espower-typescript
[node-version]: https://img.shields.io/badge/Node.js%20support-v4,v6,v7-brightgreen.svg
[license]: https://img.shields.io/npm/l/espower-typescript.svg
