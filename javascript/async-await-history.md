## Version
- 

## History
```js
// second
// first
// third

setTimeout(() => console.log('first'), 2000);
setTimeout(() => console.log('second'), 1000);
setTimeout(() => console.log('third'), 3000);
```

↓ Get output first->second->third

```js
// first
// second
// third

setTimeout(() => {
    console.log('first');
    setTimeout(() => {
        console.log('second');
        setTimeout(() => {
            console.log('third');
        }, 3000);
    }, 1000);
}, 2000);
```

↓ More readable

```js
new Promise(resolve => {
  setTimeout(() => {
    console.log('first');
    resolve();
  }, 2000);
}).then(() => {
  return new Promise(resolve => {
    setTimeout(() => {
      console.log('second');
      resolve();
    }, 1000);
  });
}).then(() => {
  return new Promise(resolve => {
    setTimeout(() => {
      console.log('third');
      resolve();
    }, 3000);
  });
});
```

↓ More readable

```js
async function outputs() {
  await outputOne('first', 2000);
  await outputOne('second', 1000);
  await outputOne('third', 3000);
}

// Return promise object.
function outputOne(target, interval) {
  return new Promise(resolve => {
    setTimeout(() => {
      console.log(target);
      resolve();
    }, interval);
  });
}

outputs();
```

## Reference
- [youtube : async/await/Promise入門【JavaScript講座】](https://youtu.be/kbKIENQKuxQ)
