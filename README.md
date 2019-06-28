# sourcemap-stacktrace

This package is more or less a stripped down reimplementation of `node-source-map-support`. It only exposes one function `sourcemapStacktrace` that returns the sourcemapped stacktrace. The main difference between the 2 is that `node-source-map-support` doesn't expose the function used for sourcemapping a stacktrace. This is only useful in cases you need to use the function directly.

## Usecases

Common usecases would be js frameworks that would like to send the stacktrace to the client for debugging and other libraries like `apollo-server` where you can use the `formatError` function to sourcemap the stacktrace of an error.

## Example

```js
import { sourcemapStacktrace } from 'sourcemap-stacktrace'

const mappedStack = sourcemapStacktrace(stacktrace)
```
