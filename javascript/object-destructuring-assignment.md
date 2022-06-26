## Version
- 

## Sample
```js
const {a, b} = {a: 0, b: 1};

// 0 1
console.log(a, b);
```
```js
const {a, b, c} = {a: 0, b: 1, d: 2};

// 0 1 undifined
console.log(a, b, c);
```
```js
const {a, b, c = 3} = {a: 0, b: 1, d: 2};

// 0 1 3
console.log(a, b, c);
```
```js
const {a, b, ...c} = {a: 0, b: 1, c: 2, d: 3};

// 0 1 {c: 2, d: 3}
console.log(a, b, c);
```
```js
const first = {first: 'val1'};
const second = {second: 'val2'};
const third = {third: 'val3'};

function mergeObject(...objects) {
    return {...objects};
}

$merged = mergeObject(first, second, third);

// {0: {first: 'val1'}, 1: {second: 'val2'}, 2: {third: 'val3'}}
console.log($merged);
// { first: 'val1' }
console.log($merged[0]);
// false
console.log(Array.isArray($merged));
```

## Reference
- 
