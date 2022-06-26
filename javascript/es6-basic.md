## Version
- ES6(ES2015)

## Concatenation
```js
// Hi! Mr.Shimauman
console.log('Hi！ ' + 'Mr.Shimauman');
```

## Templateliteral
```js
const name = 'Mr.Shimauman';

// Hi! Mr.Shimauman
cosole.log(`Hi！ ${name}`);
```

## Switch Case
```js
const color = 'green';

// go
switch (color) {
    case 'red':
        console.log('stop');
        break;
    case 'green':
        console.log('go');
        break;
    case 'yellow':
        console.log('slow');
        break;
    default:
        console.log('unknown');
        break;
}
```
```js
// go, slow, unknown
switch (color) {
    case 'red':
        console.log('stop');
        break;
    case 'green':
        console.log('go');
    case 'yellow':
        console.log('slow');
    default:
        console.log('unknown');
        break;
}
```

## Array Length
```js
const array = ['apple', 'banana', 'peach'];

// 3
console.log(array.length);
```

## Object
```js
const object = {
    itemName: 'bread',
    price: 300
};

// bread
console.log(object.itemName)

object.price = 500;
```

## For Syntax
```js
const array = [1,2,3];

for (let i = 0; i < array.length; i ++) {

}
```

## Undefined
```js
const object = {
    itemName: 'coffee',
    price: 350
};

if (object.tax === undifend) {
    ***
}
```

## Function
```js
const showMessage = function() {
    console.log('hello');
};

showMessage();
```

### Use Arrow Function
```js
const showMessage = (text) => {
    console.log(`${text}, guys.`);
};

const text = 'hello';
showMessage(text);
```
```js
const object = {
    name: 'Taro',
    skill: () => {
        console.log('no skill');
    }
};

object.skill();
```

## Class
```js
class Animal {}
// undefined
const animal = new Animal();
// undefined
console.log(animal);
// VM262:1 Animal {}__proto__: constructor: class Animalarguments: (...)caller: (...)length: 0name: "Animal"prototype: {constructor: ƒ}__proto__: ƒ ()[[FunctionLocation]]: VM140:1[[Scopes]]: Scopes[2]__proto__: Object
```

### Constructor
```js
class Item {
    constructor() {
        ***
    }
}
```

### Private Property
```js
class User {
    let #name;
    let #age;

    constructor(name, age) {
        this.#name = name;
        this.#age = age;
    }
}

const user = new User('田中', 25);
console.log(`名前: ${user.name}`);
console.log(`年齢: ${user.age}`);
```

### Method
```js
class User {
    constructor(name, birthday) {
        this.name = name;
        this.birthday = birthday;
    }

    getAge() {
        ***
        const today = this.getToday();
        ***
    }

    getToday() {
        ***
    }
}
```

### Override Constructor
```js
class User {
    constructor(name, age) {
        this.name = name;
        this.age = age;
    }
}

class AdminUser extends User {
    constructor(name, age, role) {
        // Call parent constructor().
        super(name, age);

        this.role = role;
    }
}
```

### Divide Responsibility
```js
// user.js
class User {
    ***
}
export default User;
```
```js
// adminUser.js
import User from './user.js';

class AdminUser extends User {
    ***
}
```

<br>

```js
// user.js
const name = 'taro';

export default name;
```

```js
// import.js
import name from './user.js';

// taro
console.log(name);
```

<br>

```js
// user.js
class User {
    ***
}

export defult User;
```
```js
// adminUser.js
import UserTemplate from './user.js'
```

<br>

```js
const firstUser = ***;
const secondUser = ***;

export default firstUser;
// NG. We can export default onlu one.
export default secondUser;
```

<br>

```js
const firstUser = ***;
const secondUser = ***;

export {firstUser, secondUser};
```

<br>

```js
import {name, age} from 'file-path';

// NG. Use same imported names.
import {userName, userAge};
```

## Package
### Import
```js
import {const-name} from 'file-path';
```

## Array Manipulation
### Push
```js
const array = [1,2,3];

// [1,2,3,4]
array.push(4);
```

### ForEach
```js
const array = [1,2,3];

array.forEach((number) => {
    const doubledNumber = number * 2;
    console.log(doubledNumber);
});
```

### Find
```js
const array = [1,2,3];

// 2
const firstNumberOverOne = array.find((number) => {
    return number > 1;
});
```
```js
const heros = [
    {name: 'hero1', age: '30'},
    {name: 'hero2', age: '19'}
];

// {name: 'hero2', age: '19'}
const firstYoungHero = heros.find((hero) => {
    return hero.age < 20;
});
```

### Filter
```js
const array = [1,2,3];

// [2,3]
const allNumbersOverOne = array.filter((number) => {
    return number > 1;
});
```

### Map
```js
const array = [1,2,3];

// [2,4,6]
const doubledArray = array.map((number) => {
    return number * 2;
});
```

## Callback Function
```js
const greeting = (callbackFunction) => {
    console.log('My Profile is');

    // Run call back function.
    callbackFunction('taro', 'tanaka');
};

const showFullName = (firstName, lastName) => {
    console.log(firstName + lastName);
}

// Give function name.
greeting(showFullName);
```
```js
const greeting = (callback) => {
    console.log('My Profile is');
    callback('taro', 'tanaka');
};

greeting((firstName, lastName) => {
    console.log(firstName + lastName);
});
```

## Reference
-
