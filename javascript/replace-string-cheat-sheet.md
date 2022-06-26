## Version
- 

## Sample

```js
const sample = 'a,b,c,d,a';
```

```js
// 'e,b,c,d,a'
console.log(sample.replace('a', 'e'));
```

```js
// 'e,b,c,d,e'
console.log(sample.replace(/a/g, 'e'));
```

```js
// 'e,f,c,d,e'
console.log(sample.replace(/a/g, 'e').replace('b', 'f'));
```

```js
// ',b,c,d,'
console.log(sample.replace(/a/g, ''));

// 'bcd'
console.log(sample.replace(/a/g, '').replace(/、/g, ''));
```

## Reference
- [MDN Web Docs : String.prototype.replace()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/replace)
