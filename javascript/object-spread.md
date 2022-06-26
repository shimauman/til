## Version
- ES2018

## Sample
```js
{...object}
```
```js
const object1 = {first: 'val1', second: 'val2'};
const object2 = {...object1};

// {first: 'val1', second: 'val2'}
console.log(object2);
```
```js
const object1 = {first: 'val1', second: 'val2'};
const object2 = {...object1, third: 'val3'};

// {first: 'val1', second: 'val2', third: 'val3'}
console.log(object2);
```

## Caution
```js
const object1 = {first: 'val1', second: {third: 'val3', forth: 'val4'}};
const object2 = {...object1};

object1.second.forth = 'val5';

// {first: 'val1', second: {third: 'val3', forth: 'val5'}}
console.log(object1);
console.log(object2);

object2.second.forth = 'val4';

// {first: 'val1', second: {third: 'val3', forth: 'val4'}}
console.log(object1);
console.log(object2);

```

## Reference
- [MDN Web Docs : Spread in object literals](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Spread_syntax#spread_in_object_literals)
