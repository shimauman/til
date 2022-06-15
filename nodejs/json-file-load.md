## Version
- 

## How To
```json
// user-list.json
[
  {
    "name": "a",
    "age": 10
  },
  {
    "name": "b",
    "age": 20
  }
]
```
```js
const fs = require('fs');

// When we load json file synchronously.
const loadedJson = fs.readFileSync('./user-list.json', 'utf8');
// When we load json file asynchronously.
const jsonData = await fs.readFile('./user-list.json', 'utf8');

// [
//   {
//     name: "a",
//     age: 10
//   },
//   {
//     name: "b",
//     age: 20
//   }
// ]
const parsedJson = JSON.parse(loadedJson);
```

## Reference
- [Node.js docs : fs.readFileSync()](https://nodejs.org/api/fs.html#fsreadfilesyncpath-options)
- [Node.js docs : fs.readFile()](https://nodejs.org/api/fs.html#fsreadfilepath-options-callback)
- [MDN Web Docs : JSON.parse()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/JSON/parse)
