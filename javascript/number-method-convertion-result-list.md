## Version
- 

## Output List
```js
// 0
console.log(Number(0));

// 123
console.log(Number(123));

// 123
console.log(Number('123'));

// 123.45
console.log(Number(123.45));

// 123.45
console.log(Number('123.45'));

// -123.45
console.log(Number(-123.45));

// -123
console.log(Number(-123));

// 0
console.log(Number(null));

// 0
console.log(Number(''));

// NaN
console.log(Number('foo'));

// NaN
console.log(Number(undefined));

// Nan
console.log(Number(NaN));

// 819170640000
const date = new Date('December 17, 1995 03:24:00');
console.log(Number(date));
```

## Reference
- [MDN Web Docs : Convert numeric strings and null to numbers](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number#convert_numeric_strings_and_null_to_numbers)
- [MDN Web Docs : Using Number to convert a Date object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number#using_number_to_convert_a_date_object)
