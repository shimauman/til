## Version
- 

## How To
```js
const sampleObject = {
  key1: 'value1',
  key2: 'value2',
  key3: 'value3',
};

// Output key1, key2, key3.
Object.keys(sampleObject).forEach(
  key => console.log(key)
);

// Output value1, value2, value3.
Object.values(sampleObject).forEach(
  value => console.log(value)
);

// Output [key1, value1], [key2, value2], [key3, value3]
Object.entries(sampleObject).forEach(
  (keyAndValue) => console.log(keyAndValue)
);

// Output key1: value1, key2: value2, key3: value3
for (const [key, value] of Object.entries(sampleObject)) {
  console.log(`${key}: ${value}`);
}
```

## We can't use `forEach()`
`forEach()` is method. Howevr, Object class doesn't have this method. Array and Array and Map have the method.

## Caution
- `for each ... in` : can't use anymore
- `for ... in` : not recommended

However, needs closer investigation.

## Reference
- [mdn web docs : object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)
- [mdn web docs : array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)
- [mdn web docs : map](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Map)
- [how to loop object (japanese article)](https://note.affi-sapo-sv.com/js-obj-foreach.php)
