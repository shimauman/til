## Version
- npm v7
- npm v8

## How To
package.json

```json
{
  "engines": {
    "node": "16.14.0",
    "npm": "8.3.1"
  }
}
```

We can display error when we install node packages
- under not node v16.14.0
- and by not npm v8.3.1

## Caution
When use npm
```
$ npm install --engine-strict
```

## Benefits
- Fix node and npm versions in among team.

## Reference
- [npm official document engines field](https://docs.npmjs.com/cli/v8/configuring-npm/package-json#engines)
- [package.jsonに"engines"を設定すると「このバージョンのNode.jsでしか動かない」を表明できる](https://qiita.com/suin/items/994458418c737cc9c3e8)
