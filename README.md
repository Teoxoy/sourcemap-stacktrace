# sourcemap-stacktrace

[![npm](https://img.shields.io/npm/v/sourcemap-stacktrace.svg?style=flat-square)](https://www.npmjs.com/package/sourcemap-stacktrace)
[![GitHub](https://img.shields.io/github/license/teoxoy/sourcemap-stacktrace.svg?style=flat-square&color=blue)](./LICENSE)

This package is more or less a stripped down reimplementation of `node-source-map-support`. It only exposes one function `sourcemapStacktrace` that returns the sourcemapped stacktrace. The main difference between the 2 is that `node-source-map-support` doesn't expose the function used for sourcemapping a stacktrace. This is only useful in cases you need to use the function directly.

## Usecases

Common usecases would be js frameworks that would like to send the stacktrace to the client for debugging and other libraries like `apollo-server` where you can use the `formatError` function to sourcemap the stacktrace of an error.

## Install

```
npm i sourcemap-stacktrace
```

## Example

```js
import { sourcemapStacktrace } from 'sourcemap-stacktrace'

const mappedStack = sourcemapStacktrace(stacktrace)
```
