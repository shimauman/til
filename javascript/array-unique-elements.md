## Version
- 

## How To
```js
const sampleArray = [1, 2, 3, 3, 4];

const ArrayHasUniqueElements = Array.from(new Set(sampleArray));

// [1, 2, 3, 4]
console.log(ArrayHasUniqueElements);
```

```js
const sampleArray = ['A', 'B', 'C', 'C', 'D'];

const ArrayHasUniqueElements = Array.from(new Set(sampleArray));

// ['A', 'B', 'C', 'D']
console.log(ArrayHasUniqueElements);
```

## Bad Solution
This solution has O(N2) time complexity.
```js
const sampleArray = [1, 2, 3, 3, 4];

// indexOf(O(N)) * filter(O(N)) = O(N2)
const ArrayHasUniqueElements = sampleArray.filter((x, i) => sampleArray.indexOf(x) === i);
```

## Reference
- [qiita : JavaScriptで重複排除を自分で実装してはいけない](https://qiita.com/netebakari/items/7c1db0b0cea14a3d4419)
