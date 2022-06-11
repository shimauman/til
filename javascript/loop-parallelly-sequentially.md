## Version
- 

## Sample
```js
const tasks = ["1st", "2nd", "3rd", "4th", "5th"];

async function doTask(task) {
    console.log(task);

    return new Promise((resolve) =>
        // Make each running time different.
        setTimeout(() => {
            console.log(`${task} is resolved.`);
            resolve();
        }, 1000 * getRandomInt(0, 5))
    );
}

function getRandomInt(min, max) {
  min = Math.ceil(min);
  max = Math.floor(max);
  return Math.floor(Math.random() * (max - min + 1) + min);
}

// Parallelly
tasks.forEach(task => {
  doTask(task);
})

// Sequentially 1
tasks.reduce((previousTask, currentTask) => {
    return previousTask.then(() => {
        return doTask(currentTask);
    });
}, Promise.resolve());

// Sequentially 2
for(const task of tasks) {
  doTask(task);
}
```

## Parallelly
```
1st
2nd
3rd
4th
5th
4th is resolved.
1st is resolved.
3rd is resolved.
5th is resolved.
2nd is resolved.
```

## Sequentially
```
1st
1st is resolved.
2nd
2nd is resolved.
3rd
3rd is resolved.
4th
4th is resolved.
5th
5th is resolved.
```

## Use Case
- When we do not want to send some requests in same time by asynchronous processing. This might be considered as spam bot attacks.

## Reference
- [qiita : JavascriptでPromiseを使って非同期処理を逐次実行する方法](https://qiita.com/AkihiroTakamura/items/1fdf6dfcb5cb8d5cfc4c)
