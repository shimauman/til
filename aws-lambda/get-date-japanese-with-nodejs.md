## Version
- 

## How To
```js
const current = new Date(Date.now() + (9 * 60 * 60 * 1000));
```
```js
const current = new Date(Date.now() + ((new Date().getTimezoneOffset() + (9 * 60)) * 60 * 1000));
```

## Description
- On AWS Lambda, we always get UTC time.
- `getTimezoneOffset()` returns time difference with UTC.
    - On Japan time environment, we get `-540`.
    - On UTC environment, we get `0`.
    - So, on Lambda, new Date().getTimezoneOffset() always returns 0 because Lambda is UTC environment.
- So, we add seconds for 9 hours.
- With `new Date().getTimezoneOffset()`, we can deal with any cases other than Japan time and UTC.

## Reference
- [MDN Web Docs : Date.prototype.getTimezoneOffset()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date/getTimezoneOffset)
