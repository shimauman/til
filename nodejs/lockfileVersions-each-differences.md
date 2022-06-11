## Version
- npm v7
- npm v8

## `lockfileVersion`
package-lock.json

```json
{
  "lockfileVersion": 2
}
```

## Each Differences

### version 1
- used by npm v5, v6.

### version 2
- used by npm v7.
- compatible to version 1.

### version 3
- used by npm v7.
- not compatible to version 1.
- used for the hidden lockfile at `node_modules/.package-lock.json`.
- used in a future version of npm when no support npm v6.

## Reference
- [npm official document lockfileVersion](https://docs.npmjs.com/cli/v8/configuring-npm/package-lock-json#lockfileversion)
