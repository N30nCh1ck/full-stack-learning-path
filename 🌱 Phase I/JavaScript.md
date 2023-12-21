JavaScript (JS) is a high-level, interpreted programming language primarily used for building dynamic and interactive websites. As a client-side scripting language, it runs in web browsers and allows developers to manipulate the content and behavior of web pages, enhancing user experiences through features like asynchronous communication, event handling, and DOM manipulation.

#### Syntax I
###### Variables
In JavaScript, `let` and `const` are used to declare variables. Here are examples of how they work:
```js
// Using let to declare a variable
let count = 0;

// Modifying the value of the variable
count = 1;

// Block-scoping with let
if (true) {
    let innerCount = 2;
    console.log(innerCount); // Output: 2
}

// Error: innerCount is not defined outside the block
// console.log(innerCount);

// Redeclaration is allowed with let
let count = 3; // Error: Identifier 'count' has already been declared

// Using const to declare a constant variable
const pi = 3.14;

// Error: Assignment to constant variable
// pi = 3.14159;

// Block-scoping with const
if (true) {
    const innerPi = 3.14159;
    console.log(innerPi); // Output: 3.14159
}

// Error: innerPi is not defined outside the block
// console.log(innerPi);

// const must be initialized
// const x; // Error: Missing initializer in const declaration

// const cannot be redeclared
// const pi = 3.14159; // Error: Identifier 'pi' has already been declared
```

**In summary:**
- Use `let` for variables that may be reassigned.
- Use `const` for constants or variables that shouldn't be reassigned.
- Both `let` and `const` are block-scoped, meaning they are only accessible within the block (e.g., within curly braces `{}`) where they are defined.
- `const` must be initialized with a value, and it cannot be reassigned.

###### Data Types
JavaScript has several data types, and you can use the `typeof` operator to determine the type of a variable or a value. Here are examples of various data types and their corresponding `typeof` checks:

**Number**
```js
let numberVar = 42;
console.log(typeof numberVar); // Output: "number"
```

**String**
```js
let stringVar = "Hello, World!";
console.log(typeof stringVar); // Output: "string"
```

**Boolean**
```js
let booleanVar = true;
console.log(typeof booleanVar); // Output: "boolean"
```

**Null**
```js
let nullVar = null;
console.log(typeof nullVar); // Output: "object"
```

**Undefined**
```js
let undefinedVar;
console.log(typeof undefinedVar); // Output: "undefined"
```

**Function**
```js
let functionVar = function() {};
console.log(typeof functionVar); // Output: "function"
```

**Symbol**
```js
let symbolVar = Symbol("mySymbol");
console.log(typeof symbolVar); // Output: "symbol"
```

Keep in mind that the `typeof` operator is a powerful tool for dynamic type checking, but it has some quirks. For example, it returns "object" for arrays and null, and it doesn't distinguish between different objects (e.g., arrays and regular objects). Also, it returns "function" for functions.

```js
console.log(typeof []);      // Output: "object"
console.log(typeof null);    // Output: "object"
console.log(typeof function(){});  // Output: "function"
```

In many cases, using `typeof` is helpful, but for more precise type checking, you might want to consider other approaches, like the `instanceof` operator or additional checks.

###### Operators
JavaScript supports a variety of operators for performing operations on values. Here are examples of some common types of operators:

**Arithmetic Operators**
```js
let a = 5;
let b = 2;

console.log(a + b); // Addition: 7
console.log(a - b); // Subtraction: 3
console.log(a * b); // Multiplication: 10
console.log(a / b); // Division: 2.5
console.log(a % b); // Modulus: 1
console.log(a ** b); // Exponentiation: 25
```

**Comparison Operators**
```js
let x = 10;
let y = 5;

console.log(x === y); // Strict equality: false
console.log(x !== y); // Strict inequality: true
console.log(x > y);   // Greater than: true
console.log(x < y);   // Less than: false
console.log(x >= y);  // Greater than or equal: true
console.log(x <= y);  // Less than or equal: false
```

**Logical Operators**
```js
let isTrue = true;
let isFalse = false;

console.log(isTrue && isFalse); // Logical AND: false
console.log(isTrue || isFalse); // Logical OR: true
console.log(!isTrue);            // Logical NOT: false
```

**Assignment Operators**
```js
let num = 10;

num += 5; // Addition assignment: num = num + 5
console.log(num); // Output: 15

num -= 3; // Subtraction assignment: num = num - 3
console.log(num); // Output: 12

num *= 2; // Multiplication assignment: num = num * 2
console.log(num); // Output: 24

num /= 4; // Division assignment: num = num / 4
console.log(num); // Output: 6
```

**Unary Operators**
```js
let operand = 5;

console.log(-operand);  // Unary minus: -5
console.log(+operand);  // Unary plus: 5 (not necessary, but valid)
console.log(++operand); // Increment: 6
console.log(--operand); // Decrement: 5
```

**Conditional (Ternary) Operator**
```js
let age = 20;

let message = (age >= 18) ? 'You can vote' : 'You are too young to vote';
console.log(message); // Output depends on the condition
```

**String Concatenation Operator**
```js
let firstName = 'John';
let lastName = 'Doe';

let fullName = firstName + ' ' + lastName;
console.log(fullName); // Output: 'John Doe'
```

These examples cover a range of operators in JavaScript, and there are more specialized operators for bitwise operations, type conversion, and other purposes. Understanding and using these operators is fundamental for writing effective JavaScript code.

###### Control Flow
avaScript provides various control flow structures to manage the flow of execution in a program. Here are examples of control flow statements such as `if`, `else`, `switch`, and loops (`for` and `while`):

**If Statement** 
```js
let condition = true;

if (condition) {
    console.log('Condition is true');
} else {
    console.log('Condition is false');
}
```

**IF IF-Else Else Statement**
```js
let grade = 75;

if (grade >= 90) {
    console.log('A');
} else if (grade >= 80) {
    console.log('B');
} else if (grade >= 70) {
    console.log('C');
} else {
    console.log('D');
}
```

**Switch Statement**
```js
let day = 'Monday';

switch (day) {
    case 'Monday':
        console.log('It\'s the start of the week');
        break;
    case 'Friday':
        console.log('It\'s almost the weekend');
        break;
    default:
        console.log('It\'s a regular day');
}
```

**For Loop**
```js
for (let i = 0; i < 5; i++) {
    console.log(i);
}
```

**While Loop**
```js
let count = 0;

while (count < 5) {
    console.log(count);
    count++;
}
```

**Do-While Loop**
```js
let index = 0;

do {
    console.log(index);
    index++;
} while (index < 5);
```

**For...In Loop**
```js
const person = { name: 'John', age: 30, city: 'New York' };

for (let key in person) {
    console.log(`${key}: ${person[key]}`);
}
```

**For...Of Loop**
```js
const colors = ['red', 'green', 'blue'];

for (let color of colors) {
    console.log(color);
}
```

**Nested Loops**
```js
for (let i = 0; i < 3; i++) {
    for (let j = 0; j < 2; j++) {
        console.log(`i: ${i}, j: ${j}`);
    }
}
```

These examples demonstrate how to use control flow statements in JavaScript to make decisions (if, switch) and repeat actions (for, while, do-while, for...in, for...of). Control flow is essential for creating dynamic and responsive programs.

#### Syntax II

###### Function
Functions in JavaScript allow you to encapsulate a block of code, give it a name, and reuse it throughout your program. Here are examples of various types of JavaScript functions:

**Function Declaration**
```js
// Function Declaration
function greet(name) {
    console.log(`Hello, ${name}!`);
}

// Function Call
greet('John'); // Output: Hello, John!
```

**Function Expression**
```js
// Function Expression
const add = function (a, b) {
    return a + b;
};

// Function Call
const result = add(3, 4);
console.log(result); // Output: 7
```

**Arrow Function**
```js
// Arrow Function
const multiply = (x, y) => x * y;

// Function Call
const product = multiply(5, 6);
console.log(product); // Output: 30
```

**Function with Default Parameters**
```js
function power(base, exponent = 2) {
    return Math.pow(base, exponent);
}

console.log(power(3));    // Output: 9 (using default exponent)
console.log(power(2, 4));  // Output: 16
```

**Rest Parameters**
```js
function sum(...numbers) {
    return numbers.reduce((acc, num) => acc + num, 0);
}

console.log(sum(1, 2, 3, 4)); // Output: 10
```

**Function with Callback**
```js
function fetchData(callback) {
    // Simulating asynchronous operation
    setTimeout(() => {
        const data = 'Fetched data';
        callback(data);
    }, 1000);
}

fetchData(result => {
    console.log(result); // Output: Fetched data
});
```

**Function with Object Destructuring**
```js
function printPerson({ firstName, lastName }) {
    console.log(`${firstName} ${lastName}`);
}

const person = { firstName: 'John', lastName: 'Doe' };
printPerson(person); // Output: John Doe
```

**Recursive Function**
```js
function factorial(n) {
    if (n === 0 || n === 1) {
        return 1;
    } else {
        return n * factorial(n - 1);
    }
}

console.log(factorial(5)); // Output: 120
```

**Immediately Invoked Function Expression (IIFE)**
```js
(function () {
    console.log('This is an IIFE');
})();
// Output: This is an IIFE
```

**Generator Function**
```js
function* generateSequence() {
    yield 1;
    yield 2;
    yield 3;
}

const sequence = generateSequence();
console.log(sequence.next().value); // Output: 1
console.log(sequence.next().value); // Output: 2
console.log(sequence.next().value); // Output: 3
```

These examples showcase various aspects of JavaScript functions, including different syntax forms, parameters, default values, rest parameters, callbacks, and more. Functions are a fundamental part of JavaScript, providing modularity and reusability in code.

###### Array
Arrays in JavaScript are used to store and manipulate collections of values. Here are examples of common operations with JavaScript arrays:

**Array Creation**
```js
const fruits = ['apple', 'orange', 'banana'];
```

**Accessing Array Elements**
```js
console.log(fruits[0]); // Output: 'apple'
console.log(fruits[1]); // Output: 'orange'
console.log(fruits[2]); // Output: 'banana'
```

**Array Length**
```js
console.log(fruits.length); // Output: 3
```

**Adding Elements to the End**
```js
fruits.push('grape');
console.log(fruits); // Output: ['apple', 'orange', 'banana', 'grape']
```

**Removing the Last Element**
```js
fruits.pop();
console.log(fruits); // Output: ['apple', 'orange', 'banana']
```

**Adding Elements to the Beginning**
```js
fruits.unshift('kiwi');
console.log(fruits); // Output: ['kiwi', 'apple', 'orange', 'banana']
```

**Removing the First Element**
```js
fruits.shift();
console.log(fruits); // Output: ['apple', 'orange', 'banana']
```

**Finding the Index of an Element**
```js
const index = fruits.indexOf('orange');
console.log(index); // Output: 1
```

**Removing an Element by Index**
```js
fruits.splice(1, 1); // Remove one element starting from index 1
console.log(fruits); // Output: ['apple', 'banana']
```

**Slicing an Array**
```js
const slicedFruits = fruits.slice(1, 2); // Extract elements from index 1 to (2-1)
console.log(slicedFruits); // Output: ['banana']
```

**Iterating Over an Array**
```js
fruits.forEach(fruit => {
    console.log(fruit);
});
// Output:
// 'apple'
// 'orange'
// 'banana'
```

**Mapping an Array**
```js
const uppercaseFruits = fruits.map(fruit => fruit.toUpperCase());
console.log(uppercaseFruits);
// Output: ['APPLE', 'ORANGE', 'BANANA']
```

**Filtering an Array**
```js
const filteredFruits = fruits.filter(fruit => fruit.length > 5);
console.log(filteredFruits); // Output: ['orange', 'banana']
```

**Reducing an Array**
```js
const totalLength = fruits.reduce((acc, fruit) => acc + fruit.length, 0);
console.log(totalLength); // Output: 17
```

**Array Concatenation**
```js
const moreFruits = ['grape', 'kiwi'];
const combinedFruits = fruits.concat(moreFruits);
console.log(combinedFruits);
// Output: ['apple', 'orange', 'banana', 'grape', 'kiwi']
```

These examples demonstrate basic operations with JavaScript arrays, including creation, modification, iteration, and transformation. Arrays are versatile and widely used in JavaScript for managing collections of data.

###### Math
JavaScript provides a `Math` object with various methods for performing mathematical operations. Here are examples of using some of the `Math` object methods:

**Random Number**
```js
// Generate a random number between 0 (inclusive) and 1 (exclusive)
const randomNumber = Math.random();
console.log(randomNumber);
```

**Rounding Numbers**
```js
const numberToRound = 3.75;

// Round to the nearest integer
const roundedNumber = Math.round(numberToRound);
console.log(roundedNumber); // Output: 4

// Round down to the nearest integer
const floorNumber = Math.floor(numberToRound);
console.log(floorNumber); // Output: 3

// Round up to the nearest integer
const ceilNumber = Math.ceil(numberToRound);
console.log(ceilNumber); // Output: 4
```

**Absolute Value**
```js
const negativeNumber = -5;

const absoluteValue = Math.abs(negativeNumber);
console.log(absoluteValue); // Output: 5
```

**Power and Square Root**
```js
const base = 2;
const exponent = 3;

// Raise to the power
const powerResult = Math.pow(base, exponent);
console.log(powerResult); // Output: 8

// Square root
const squareRootResult = Math.sqrt(powerResult);
console.log(squareRootResult); // Output: 2.8284271247461903
```

**Trigonometric Functions**
```js
const angleInRadians = Math.PI / 4;

// Sine
const sineValue = Math.sin(angleInRadians);
console.log(sineValue); // Output: 0.7071067811865475

// Cosine
const cosineValue = Math.cos(angleInRadians);
console.log(cosineValue); // Output: 0.7071067811865476

// Tangent
const tangentValue = Math.tan(angleInRadians);
console.log(tangentValue); // Output: 0.9999999999999999
```

**Minimum and Maximum**
```js
const numbers = [2, 8, 5, 1, 4];

const minValue = Math.min(...numbers);
console.log(minValue); // Output: 1

const maxValue = Math.max(...numbers);
console.log(maxValue); // Output: 8
```

**Rounding to Decimal Places**
```js
const numberToRound = 3.14159;

const roundedToTwoDecimalPlaces = Number(numberToRound.toFixed(2));
console.log(roundedToTwoDecimalPlaces); // Output: 3.14
```

These examples showcase some of the commonly used `Math` object methods in JavaScript. The `Math` object provides a wide range of mathematical functions that can be useful in various scenarios.

###### RegExp
Regular expressions (RegExp) in JavaScript provide a powerful way to work with patterns in strings. Here are examples of using regular expressions in JavaScript:

**Creating a Regular Expression**
```js
// Using the RegExp constructor
const regex1 = new RegExp('pattern');

// Using a regex literal
const regex2 = /pattern/;
```

**Testing for a Match**
```js
const pattern = /apple/;
const text = 'This is an apple';

const isMatch = pattern.test(text);
console.log(isMatch); // Output: true
```

**Matching and Extracting**
```js
const text = 'The price is $25.99';

// Match and extract the price
const pricePattern = /\$\d+\.\d{2}/;
const matchResult = text.match(pricePattern);
console.log(matchResult[0]); // Output: $25.99
```

**Replacing Matches**
```js
const text = 'I love JavaScript! JavaScript is awesome.';

// Replace 'JavaScript' with 'TypeScript'
const replacedText = text.replace(/JavaScript/g, 'TypeScript');
console.log(replacedText);
// Output: I love TypeScript! TypeScript is awesome.
```

**Using Capture Groups**
```js
const text = 'Name: John Doe, Age: 30';

// Extract name and age using capture groups
const pattern = /Name: (\w+ \w+), Age: (\d+)/;
const matchResult = text.match(pattern);
console.log(matchResult[1]); // Output: John Doe
console.log(matchResult[2]); // Output: 30
```

**Anchors and Boundaries**
```js
const text = 'JavaScript is fun!';

// Test if the string starts with 'JavaScript'
const startsWithJS = /^JavaScript/.test(text);
console.log(startsWithJS); // Output: true

// Test if the string ends with 'fun!'
const endsWithFun = /fun!$/.test(text);
console.log(endsWithFun); // Output: true
```

**Modifiers (Case Insensitivity)**
```js
const text = 'JavaScript is case insensitive';

// Test for 'javascript' regardless of case
const caseInsensitiveMatch = /javascript/i.test(text);
console.log(caseInsensitiveMatch); // Output: true
```

**Quantifiers (Repeating Patterns)**
```js
const text = 'This is a repeated word word.';

// Match repeated word
const repeatedWordPattern = /\b(\w+)\s+\1\b/;
const hasRepeatedWord = repeatedWordPattern.test(text);
console.log(hasRepeatedWord); // Output: true
```

These examples cover some common use cases of regular expressions in JavaScript, including testing for matches, extracting information, replacing patterns, and working with anchors, boundaries, and modifiers. Regular expressions are a powerful tool for string manipulation and pattern matching.

###### Set
In JavaScript, a `Set` is a built-in object that allows you to store unique values of any type. Here are examples of using the `Set` object in JavaScript:

**Creating a Set**
```js
// Creating an empty set
const emptySet = new Set();

// Creating a set with initial values
const numberSet = new Set([1, 2, 3, 4, 5]);
const stringSet = new Set(['apple', 'banana', 'orange']);
```

**Adding and Deleting Elements**
```js
const mySet = new Set();

// Adding elements
mySet.add(1);
mySet.add('apple');
mySet.add({ key: 'value' });

// Deleting an element
mySet.delete(1);
```

**Checking for the Presence of Elements**
```js
const mySet = new Set(['apple', 'banana', 'orange']);

// Using forEach
mySet.forEach(item => {
    console.log(item);
});

// Using for...of loop
for (const item of mySet) {
    console.log(item);
}
```

**Getting the Size of a Set**
```js
const mySet = new Set([1, 2, 3, 4, 5]);

mySet.clear();
console.log(mySet.size); // Output: 0
```

**Converting Set to Array**
```js
const mySet = new Set(['apple', 'banana', 'orange']);

const arrayFromSet = Array.from(mySet);
console.log(arrayFromSet); // Output: ['apple', 'banana', 'orange']
```

**Set Operations (Union, Intersection, Difference)**
```js
const set1 = new Set([1, 2, 3, 4, 5]);
const set2 = new Set([3, 4, 5, 6, 7]);

// Union
const unionSet = new Set([...set1, ...set2]);

// Intersection
const intersectionSet = new Set([...set1].filter(value => set2.has(value)));

// Difference
const differenceSet = new Set([...set1].filter(value => !set2.has(value)));
```

These examples illustrate some common operations with JavaScript `Set` objects, including creation, adding and deleting elements, checking for presence, iterating, getting the size, clearing, converting to an array, and performing set operations. Sets are useful for managing unique values efficiently.

###### Map
In JavaScript, a `Map` is a built-in object that allows you to store key-value pairs. Here are examples of using the `Map` object in JavaScript:

**Creating a Map**
```js
// Creating an empty map
const emptyMap = new Map();

// Creating a map with initial key-value pairs
const myMap = new Map([
    ['key1', 'value1'],
    ['key2', 'value2'],
    ['key3', 'value3']
]);
```

**Adding and Deleting Entries**
```js
const myMap = new Map();

// Adding entries
myMap.set('name', 'John');
myMap.set('age', 30);
myMap.set('isStudent', false);

// Deleting an entry
myMap.delete('age');
```

**Getting and Checking for the Presence of Entries**
```js
const myMap = new Map([
    ['key1', 'value1'],
    ['key2', 'value2']
]);

console.log(myMap.get('key1')); // Output: 'value1'
console.log(myMap.has('key3')); // Output: false
```

**Iterating Over a Map**
```js
const myMap = new Map([
    ['name', 'John'],
    ['age', 30],
    ['isStudent', false]
]);

// Using forEach
myMap.forEach((value, key) => {
    console.log(`${key}: ${value}`);
});

// Using for...of loop
for (const [key, value] of myMap) {
    console.log(`${key}: ${value}`);
}
```

**Getting the Size of a Map**
```js
const myMap = new Map([
    ['key1', 'value1'],
    ['key2', 'value2'],
    ['key3', 'value3']
]);

console.log(myMap.size); // Output: 3
```

**Clearing a Map**
```js
const myMap = new Map([
    ['key1', 'value1'],
    ['key2', 'value2']
]);

myMap.clear();
console.log(myMap.size); // Output: 0
```

**Converting Map to Array**
```js
const myMap = new Map([
    ['name', 'John'],
    ['age', 30],
    ['isStudent', false]
]);

const arrayFromMap = Array.from(myMap);
console.log(arrayFromMap);
// Output: [['name', 'John'], ['age', 30], ['isStudent', false]]
```

**Map with Objects as Keys**
```js
const objectKeyMap = new Map();

const obj1 = { id: 1 };
const obj2 = { id: 2 };

objectKeyMap.set(obj1, 'Value associated with obj1');
objectKeyMap.set(obj2, 'Value associated with obj2');

console.log(objectKeyMap.get(obj1)); // Output: 'Value associated with obj1'
```

These examples illustrate various operations with JavaScript `Map` objects, including creation, adding and deleting entries, getting and checking for presence, iterating, getting the size, clearing, converting to an array, and using objects as keys. Maps are useful for storing key-value pairs and are particularly handy when the keys are of different types or when the order of insertion matters.

#### Syntax III
###### Modules
In JavaScript, modules provide a way to organize and structure code by encapsulating functionality into separate files. Here are examples of using JavaScript modules:

**Creating a Module**
```js
// math.js module
export const add = (a, b) => a + b;
export const subtract = (a, b) => a - b;
```

**Importing and Using a Module**
```js
// main.js
import { add, subtract } from './math';

const result1 = add(5, 3);
console.log(result1); // Output: 8

const result2 = subtract(10, 4);
console.log(result2); // Output: 6
```

**Default Export**
`logger.js`
```js
// logger.js module
const log = message => console.log(message);

export default log;


// main.js
import customLogger from './logger';

customLogger('This is a custom log message');
```

**Combining Multiple Exports**
```js
// utility.js module
export const square = x => x * x;
export const cube = x => x * x * x;


// main.js
import { square, cube } from './utility';

console.log(square(3)); // Output: 9
console.log(cube(3));   // Output: 27
```

**Importing the Entire Module**
```js
// main.js
import * as mathModule from './math';

const result = mathModule.add(7, 2);
console.log(result); // Output: 9
```

**Renaming Imported Members**
```js
// main.js
import { add as addition } from './math';

const result = addition(5, 3);
console.log(result); // Output: 8
```

**Dynamic Import (Code Splitting)**
```js
// main.js
const loadMathModule = async () => {
    const mathModule = await import('./math');
    const result = mathModule.add(4, 6);
    console.log(result); // Output: 10
};

loadMathModule();
```

These examples demonstrate how to create, import, and use JavaScript modules. Modularizing code helps maintainability, readability, and reusability in larger projects. Note that module syntax is widely used in modern JavaScript environments, especially in the context of ECMAScript modules (ESM).

###### Object
JavaScript objects are fundamental data structures that allow you to store and organize data as key-value pairs. Here are examples of working with JavaScript objects:

**Creating an Object**
```js
// Object literal syntax
const person = {
    firstName: 'John',
    lastName: 'Doe',
    age: 30,
    isStudent: false,
    greet: function() {
        console.log(`Hello, ${this.firstName} ${this.lastName}!`);
    }
};
```

**Accessing Object Properties**
```js
console.log(person.firstName); // Output: 'John'
console.log(person['lastName']); // Output: 'Doe'
```

**Adding and Modifying Properties**
```js
person.email = 'john.doe@example.com';
person.age = 31;
```

**Deleting Properties**
```js
delete person.isStudent;
```

**Object Methods**
```js
person.greet(); // Output: 'Hello, John Doe!'
```

**Object Destructuring**
```js
const { firstName, lastName } = person;
console.log(firstName, lastName); // Output: 'John Doe'
```

**Looping Through Object Properties**
```js
for (const key in person) {
    console.log(`${key}: ${person[key]}`);
}
```

**Object Constructor**
```js
function Car(make, model, year) {
    this.make = make;
    this.model = model;
    this.year = year;
}

const myCar = new Car('Toyota', 'Camry', 2022);
```

**Object Prototypes**
```js
Car.prototype.getFullInfo = function() {
    return `${this.year} ${this.make} ${this.model}`;
};

console.log(myCar.getFullInfo()); // Output: '2022 Toyota Camry'
```

**Object Define Property**
```js
Object.defineProperty(person, 'fullName', {
    get: function() {
        return `${this.firstName} ${this.lastName}`;
    },
    set: function(value) {
        const names = value.split(' ');
        this.firstName = names[0];
        this.lastName = names[1];
    }
});

console.log(person.fullName); // Output: 'John Doe'
person.fullName = 'Jane Smith';
console.log(person.fullName); // Output: 'Jane Smith'
```

**Object Assign**
```js
const defaults = { color: 'red', weight: '10kg' };
const myChair = { type: 'chair', color: 'blue' };

const combinedChair = Object.assign({}, defaults, myChair);
console.log(combinedChair);
// Output: { type: 'chair', color: 'blue', weight: '10kg' }
```

**Using Keys Values and Entries**
```js
console.log(Object.keys(person)); // Output: ['firstName', 'lastName', 'age', 'email']
console.log(Object.values(person)); // Output: ['John', 'Doe', 31, 'john.doe@example.com']
console.log(Object.entries(person));
// Output: [['firstName', 'John'], ['lastName', 'Doe'], ['age', 31], ['email', 'john.doe@example.com']]
```

These examples cover a range of operations with JavaScript objects, including creation, property access, modification, deletion, methods, object destructuring, iteration, constructor functions, prototypes, and additional object-related methods and techniques. Objects are a versatile and powerful feature in JavaScript for structuring and organizing data.

###### Date
In JavaScript, the `Date` object is used to work with dates and times. Here are examples of using the `Date` object:

**Creating a Date Object**
```js
const currentDate = new Date();
console.log(currentDate);
```

**Creating a Date Object with a Specific Date and Time**
```js
const specificDate = new Date('2022-12-31T12:30:00');
console.log(specificDate);
```

**Getting the Current Date and Time Components**
```js
const now = new Date();

const year = now.getFullYear();
const month = now.getMonth(); // Note: Months are zero-indexed (0-11)
const day = now.getDate();
const hours = now.getHours();
const minutes = now.getMinutes();
const seconds = now.getSeconds();
const milliseconds = now.getMilliseconds();

console.log(`${year}-${month + 1}-${day} ${hours}:${minutes}:${seconds}.${milliseconds}`);
```

**Setting Date Components**
```js
const futureDate = new Date();
futureDate.setFullYear(2023);
futureDate.setMonth(5); // Note: Months are zero-indexed (0-11)
futureDate.setDate(15);
futureDate.setHours(18);
futureDate.setMinutes(30);
futureDate.setSeconds(0);

console.log(futureDate);
```

**Formatting Dates**
```js
const eventDate = new Date('2023-08-25T19:00:00');

const options = { weekday: 'long', year: 'numeric', month: 'long', day: 'numeric', hour: 'numeric', minute: 'numeric', second: 'numeric', timeZoneName: 'short' };
const formattedDate = eventDate.toLocaleDateString('en-US', options);

console.log(formattedDate);
```

**Calculating Time Differences**
```js
const startDate = new Date('2023-01-01');
const endDate = new Date('2023-12-31');

const timeDifference = endDate - startDate;
const daysDifference = timeDifference / (1000 * 60 * 60 * 24);

console.log(`Days until the end of the year: ${Math.floor(daysDifference)}`);
```

**Working with Time Zones**
```js
const dateInUTC = new Date('2023-01-01T12:00:00Z');
const dateInLocalTime = new Date(dateInUTC.toLocaleString('en-US', { timeZone: 'America/New_York' }));

console.log(dateInUTC.toISOString()); // Output: '2023-01-01T12:00:00.000Z'
console.log(dateInLocalTime.toISOString()); // Output: '2023-01-01T17:00:00.000Z'
```

**Parsing Dates from Strings**
```js
const dateString = '2023-06-15T08:45:30';
const parsedDate = new Date(dateString);

console.log(parsedDate);
```

These examples cover a range of operations with the JavaScript `Date` object, including creating date objects, getting and setting date components, formatting dates, calculating time differences, working with time zones, and parsing dates from strings. The `Date` object provides comprehensive functionality for working with dates and times in JavaScript.

###### String
Certainly! JavaScript provides a variety of methods for working with strings. Here are examples of common string operations:

**Creating a String**
```js
const greeting = 'Hello, World!';
const multilineString = `This is
a multiline
string.`;
```

**Concatenating Strings**
```js
const firstName = 'John';
const lastName = 'Doe';

const fullName = firstName + ' ' + lastName;
console.log(fullName); // Output: 'John Doe'
```

**String Length**
```js
const message = 'This is a message.';

console.log(message.length); // Output: 18
```

**Accessing Characters in a String**
```js
const text = 'JavaScript';

console.log(text[0]); // Output: 'J'
console.log(text.charAt(4)); // Output: 'S'
```

**Substring**
```js
const sentence = 'The quick brown fox';

const subString1 = sentence.substring(4, 9);
console.log(subString1); // Output: 'quick'

const subString2 = sentence.substring(10);
console.log(subString2); // Output: 'brown fox'
```

**String Case Methods**
```js
const mixedCase = 'ThIs iS a MiXeD CaSe sTrInG';

console.log(mixedCase.toLowerCase());
// Output: 'this is a mixed case string'

console.log(mixedCase.toUpperCase());
// Output: 'THIS IS A MIXED CASE STRING'
```

**Trimming Whitespace**
```js
const paddedString = '   Trim me!   ';

console.log(paddedString.trim()); // Output: 'Trim me!'
```

**String Replacement**
```js
const sentence = 'This is a sentence';

const words = sentence.split(' ');
console.log(words); // Output: ['This', 'is', 'a', 'sentence']
```

**Checking if a String Contains a Substring**
```js
const text = 'Check if this text contains "if"';

console.log(text.includes('if')); // Output: true
```

**String Searching**
```js
const sentence = 'JavaScript is powerful.';

console.log(sentence.indexOf('is')); // Output: 11
console.log(sentence.lastIndexOf('a')); // Output: 17
```

**Converting to and from Unicode**
```js
const unicodeString = '\u0041\u0042\u0043';
console.log(unicodeString); // Output: 'ABC'

const unicodeCodePoint = '🚀'.codePointAt(0);
console.log(unicodeCodePoint); // Output: 128640
```

These examples cover a variety of string operations in JavaScript. Strings are essential for text manipulation and are widely used in JavaScript applications.

###### Number
Certainly! JavaScript provides various methods for working with numbers. Here are examples of common operations and methods related to numbers:

**Creating Numbers**
```js
const integerNumber = 42;
const floatNumber = 3.14;
const scientificNotation = 6.02e23; // 6.02 × 10^23
```

**Arithmetic Operations**
```js
const a = 10;
const b = 5;

const sum = a + b;
const difference = a - b;
const product = a * b;
const quotient = a / b;
const remainder = a % b;
const exponentiation = a ** 2; // a squared
```

**Increment and Decrement**
```js
let counter = 0;

counter++;
console.log(counter); // Output: 1

counter--;
console.log(counter); // Output: 0
```

**Math Object Methods**
```js
const x = 3.14159;

const roundedValue = Math.round(x);
console.log(roundedValue); // Output: 3

const absoluteValue = Math.abs(-7);
console.log(absoluteValue); // Output: 7

const squareRoot = Math.sqrt(16);
console.log(squareRoot); // Output: 4

const randomValue = Math.random();
console.log(randomValue); // Output: a random number between 0 (inclusive) and 1 (exclusive)
```

**Converting Strings to Numbers**
```js
const numericString = '42';

const numericValue = parseInt(numericString);
console.log(numericValue); // Output: 42

const floatValue = parseFloat('3.14');
console.log(floatValue); // Output: 3.14
```

**Checking for NaN (Not a Number)**
```js
const result = 'abc' / 2;

console.log(isNaN(result)); // Output: true
```

**Infinity and -Infinity**
```js
const positiveInfinity = Infinity;
const negativeInfinity = -Infinity;
```

**Number Methods**
```js
const num = 123.456;

console.log(num.toString()); // Output: '123.456'
console.log(num.toFixed(2)); // Output: '123.46'
console.log(num.toPrecision(4)); // Output: '123.5'
console.log(num.toLocaleString('en-US')); // Output: '123.456'
```

**Comparing Numbers**
```js
const x = 10;
const y = 20;

console.log(x > y); // Output: false
console.log(x < y); // Output: true
console.log(x === y); // Output: false
console.log(x !== y); // Output: true
```

These examples cover a variety of operations and methods related to numbers in JavaScript. Numbers are fundamental data types used for mathematical calculations and various other purposes in programming.

#### Syntax IIII
###### Fetch
The `fetch` function in JavaScript is used to make HTTP requests and handle responses. It is commonly used for fetching data from a server. Here are examples of using the `fetch` function:

**Basic GET Request**
```js
// Fetching data from a URL using a GET request
fetch('https://jsonplaceholder.typicode.com/posts/1')
    .then(response => response.json())
    .then(data => console.log(data))
    .catch(error => console.error('Error:', error))
```

**POST Request with JSON Data**
```js
// Sending a POST request with JSON data
const postData = {
    title: 'foo',
    body: 'bar',
    userId: 1
};

fetch('https://jsonplaceholder.typicode.com/posts', {
    method: 'POST',
    headers: {
        'Content-Type': 'application/json'
    },
    body: JSON.stringify(postData)
})
    .then(response => response.json())
    .then(data => console.log(data))
    .catch(error => console.error('Error:', error));
```

**Handling Headers and Response Status**
```js
// Fetching data and handling headers and response status
fetch('https://jsonplaceholder.typicode.com/posts/1')
    .then(response => {
        console.log('Status Code:', response.status);
        console.log('Headers:', response.headers.get('content-type'));
        return response.json();
    })
    .then(data => console.log(data))
    .catch(error => console.error('Error:', error));
```

**Adding Query Parameters to the URL**
```js
// Adding query parameters to the URL
const userId = 1;
fetch(`https://jsonplaceholder.typicode.com/posts?userId=${userId}`)
    .then(response => response.json())
    .then(data => console.log(data))
    .catch(error => console.error('Error:', error));
```

**Error Handling**
```js
// Handling errors with fetch
fetch('https://jsonplaceholder.typicode.com/posts/invalid')
    .then(response => {
        if (!response.ok) {
            throw new Error(`HTTP error! Status: ${response.status}`);
        }
        return response.json();
    })
    .then(data => console.log(data))
    .catch(error => console.error('Error:', error));
```

**Using async/await**
```js
// Using async/await with fetch
async function fetchData() {
    try {
        const response = await fetch('https://jsonplaceholder.typicode.com/posts/1');
        const data = await response.json();
        console.log(data);
    } catch (error) {
        console.error('Error:', error);
    }
}

fetchData();
```

These examples demonstrate various use cases of the `fetch` function, including making GET and POST requests, handling headers and response status, error handling, using async/await, and adding query parameters to the URL. Remember that the `fetch` function returns a Promise, and the `then` and `catch` methods are commonly used to handle the asynchronous nature of HTTP requests.

###### Errors
In JavaScript, errors can occur during the execution of code, and you can use the `try...catch` statement to handle these errors. Here are examples of different types of errors and how to handle them:

**Basic Error Handling with Try...Catch**
```js
try {
    // Code that may throw an error
    throw new Error('This is a custom error.');
} catch (error) {
    // Handling the error
    console.error('Caught an error:', error.message);
} finally {
    // Code that will be executed regardless of whether an error occurred or not
    console.log('Finally block executed.');
}
```

**Handling Specific Types of Errors**
```js
try {
    // Code that may throw a TypeError
    const undefinedVariable = undefined;
    console.log(undefinedVariable.property);
} catch (error) {
    if (error instanceof TypeError) {
        console.error('Caught a TypeError:', error.message);
    } else {
        console.error('Caught an error:', error.message);
    }
}
```

**Custom Error Classes**
```js
class CustomError extends Error {
    constructor(message) {
        super(message);
        this.name = 'CustomError';
    }
}

try {
    throw new CustomError('This is a custom error.');
} catch (error) {
    if (error instanceof CustomError) {
        console.error('Caught a CustomError:', error.message);
    } else {
        console.error('Caught an error:', error.message);
    }
}
```

**Throwing and Handling SyntaxError**
```js
try {
    throw new SyntaxError('There is a syntax error in the code.');
} catch (error) {
    console.error('Caught a SyntaxError:', error.message);
}
```

**Asynchronous Error Handling with Promises**
```js
async function asyncFunction() {
    return new Promise((resolve, reject) => {
        // Simulating an asynchronous operation that fails
        setTimeout(() => {
            reject(new Error('Async operation failed.'));
        }, 1000);
    });
}

async function handleAsyncError() {
    try {
        await asyncFunction();
    } catch (error) {
        console.error('Caught an asynchronous error:', error.message);
    }
}

handleAsyncError();
```

**Global Error Handling with Window On Error**
```js
window.onerror = function (message, source, lineno, colno, error) {
    console.error('Global error handler:', message);
};
```

These examples cover different aspects of error handling in JavaScript, including using `try...catch` statements, handling specific types of errors, creating custom error classes, throwing and handling `SyntaxError`, asynchronous error handling with Promises, and setting up a global error handler with `window.onerror`. Depending on the context and type of application, you may choose different error-handling approaches.

###### Async/Await & Promise
Async/await is a feature in JavaScript that simplifies working with asynchronous code, especially when dealing with Promises. Here are examples demonstrating the use of async/await:

**Basic Example**
```js
// Function returning a Promise
function fetchData() {
    return new Promise(resolve => {
        setTimeout(() => {
            resolve('Data fetched successfully!');
        }, 1000);
    });
}

// Async function using await
async function fetchDataAsync() {
    try {
        const data = await fetchData();
        console.log(data);
    } catch (error) {
        console.error('Error:', error);
    }
}

fetchDataAsync();
```

**Sequential Execution**
```js
async function sequentialAsyncOperations() {
    try {
        const result1 = await fetchData();
        console.log(result1);

        const result2 = await fetchData();
        console.log(result2);
    } catch (error) {
        console.error('Error:', error);
    }
}

sequentialAsyncOperations();
```

**Parallel Execution with Promise All**
```js
async function parallelAsyncOperations() {
    try {
        const [result1, result2] = await Promise.all([fetchData(), fetchData()]);
        console.log(result1, result2);
    } catch (error) {
        console.error('Error:', error);
    }
}

parallelAsyncOperations();
```

**Async Function as Promise**
```js
function asyncFunctionAsPromise() {
    return new Promise(async (resolve, reject) => {
        try {
            const result = await fetchData();
            resolve(result);
        } catch (error) {
            reject(error);
        }
    });
}

asyncFunctionAsPromise()
    .then(result => console.log(result))
    .catch(error => console.error('Error:', error));
```

**Error Handling with Try...Catch and Promise Reject**
```js
async function fetchDataWithError() {
    return new Promise((resolve, reject) => {
        setTimeout(() => {
            reject(new Error('Failed to fetch data!'));
        }, 1000);
    });
}

async function handleAsyncError() {
    try {
        await fetchDataWithError();
    } catch (error) {
        console.error('Caught an asynchronous error:', error.message);
    }
}

handleAsyncError();
```

**Async/Await in Class Methods**
```js
class DataService {
    async fetchData() {
        try {
            const result = await fetchData();
            console.log(result);
        } catch (error) {
            console.error('Error:', error);
        }
    }
}

const dataService = new DataService();
dataService.fetchData();
```

These examples showcase various use cases of async/await, including basic usage, sequential and parallel execution, using async functions as promises, error handling with try...catch, and integrating async/await into class methods. Async/await simplifies asynchronous code and makes it more readable and maintainable.

#### Implementation
###### DOM (Document Object Model)
The DOM is a programming interface for web documents. It represents the structure of a document as a tree of objects, allowing JavaScript to interact with and manipulate HTML or XML content dynamically.

**Get Element**
```js
// Returns a reference to the element with the specified ID.
const element = document.getElementById('myElement');

// Returns a live HTMLCollection containing all elements with the specified class name.
const elements = document.getElementsByClassName('myClass');

// Returns a live HTMLCollection containing all elements with the specified tag name.
const paragraphs = document.getElementsByTagName('p');
```

**Query Selector**
```js
// Returns the first element that matches the specified CSS selector.
const element = document.querySelector('#myElement');

// Returns a NodeList containing all elements that match the specified CSS selector.
const elements = document.querySelectorAll('.myClass');
```

**Custom Element**
```js
// Gets or sets the HTML content of an element.
const content = document.getElementById('myElement').innerHTML;

// Gets or sets the text content of an element.
const text = document.getElementById('myElement').textContent;

// Gets or sets the value of form elements (like input or select).
const inputValue = document.getElementById('myInput').value;

// Sets the value of an attribute on the specified element.
document.getElementById('myElement').setAttribute('data-custom', 'value');

// Gets the value of the specified attribute on the element
const customValue = document.getElementById('myElement').getAttribute('data-custom');

// Returns a live DOMTokenList representing the class attribute of the element.
const classes = document.getElementById('myElement').classList;

// Registers an event handler to be called when a particular event type occurs on the element.
document.getElementById('myButton').addEventListener('click', handleClick);

// Allows you to get or set inline styles on an element.
document.getElementById('myElement').style.color = 'red';

// Adds a new child node to the end of the list of children of the specified element.
const parent = document.getElementById('parentElement');
const newChild = document.createElement('div');
parent.appendChild(newChild);

// Removes a child node from the DOM.
const parent = document.getElementById('parentElement');
const childToRemove = document.getElementById('childElement');
parent.removeChild(childToRemove);
```

###### Event Listeners
Event listeners in JavaScript are used to listen for and respond to events triggered by user interactions or other events in the browser. Here are examples of using event listeners:

**Click Event**
```js
<button id="myButton">Click me</button>

<script>
  const button = document.getElementById('myButton');

  // Adding a click event listener
  button.addEventListener('click', function() {
    alert('Button clicked!');
  });
</script>
```

**Mouse Over and Mouse Out Events**
```js
<div id="myDiv" style="width: 100px; height: 100px; background-color: lightblue;"></div>

<script>
  const myDiv = document.getElementById('myDiv');

  // Mouse over event
  myDiv.addEventListener('mouseover', function() {
    myDiv.style.backgroundColor = 'lightgreen';
  });

  // Mouse out event
  myDiv.addEventListener('mouseout', function() {
    myDiv.style.backgroundColor = 'lightblue';
  });
</script>
```

**Input Event (for Text Input)**
```js
<input type="text" id="myInput" placeholder="Type something">

<script>
  const myInput = document.getElementById('myInput');

  // Input event listener
  myInput.addEventListener('input', function() {
    console.log('Input value:', myInput.value);
  });
</script>
```

**Form Submission Event**
```js
<form id="myForm">
  <input type="text" name="username" placeholder="Username">
  <input type="password" name="password" placeholder="Password">
  <button type="submit">Submit</button>
</form>

<script>
  const myForm = document.getElementById('myForm');

  // Form submission event listener
  myForm.addEventListener('submit', function(event) {
    event.preventDefault(); // Prevents the default form submission behavior
    alert('Form submitted!');
  });
</script>
```

**Window Resize Event**
```js
<script>
  // Window resize event listener
  window.addEventListener('resize', function() {
    console.log('Window resized!');
  });
</script>
```

**Event Delegation**
```js
<ul id="myList">
  <li>Item 1</li>
  <li>Item 2</li>
  <li>Item 3</li>
</ul>

<script>
  const myList = document.getElementById('myList');

  // Event delegation on the parent element
  myList.addEventListener('click', function(event) {
    if (event.target.tagName === 'LI') {
      alert(`Clicked on ${event.target.innerText}`);
    }
  });
</script>
```

These examples demonstrate the use of event listeners for various events, including click, mouseover, mouseout, input, form submission, window resize, and event delegation. Event listeners play a crucial role in building interactive and dynamic web applications.

###### BOM (Browser Object Model)
The BOM represents the browser as an object and provides an interface for interacting with browser features, such as opening new windows, managing history, and accessing screen information, beyond the document structure handled by the DOM.

**Window Object**
```js
// Displays an alert dialog with the specified message.
window.alert(message)

// Displays a dialog box with a specified message and OK and Cancel buttons.
window.confirm(message)

// Displays a dialog box that prompts the user for input.
window.prompt(message, default)

// Opens a new browser window or a new tab.
window.open(url, target, features)

// Closes the current browser window.
window.close()

// Represents the current URL and allows you to navigate to a new one.
console.log(window.location.href); // Get current URL
window.location.href = 'https://example.com'; // Navigate to a new URL

// Provides information about the browser and its capabilities.
console.log(window.navigator.userAgent); // Get user agent string

// Represents the browsing history of the window.
window.history.back(); // Go back one page
window.history.forward(); // Go forward one page

// Allows you to store key/value pairs in the browser.
window.localStorage.setItem('key', 'value'); // Set an item
const storedValue = window.localStorage.getItem('key'); // Get an item

// Scroll the document to a particular position or by a certain amount.
window.scrollTo(0, 0); // Scroll to the top
window.scrollBy(0, 100); // Scroll down by 100 pixels
```

**Screen Object & Others**
```js
// Provides information about the user's screen.
console.log(window.screen.width); // Screen width in pixels
console.log(window.screen.height); // Screen height in pixels

// Get the inner width and height of the browser window.
console.log(window.innerWidth); // Inner width of the window
console.log(window.innerHeight); // Inner height of the window
```

###### JSON (JavaScript Object Notation)
JSON is a lightweight data interchange format that is easy for humans to read and write, and easy for machines to parse and generate. It is widely used for representing structured data in web development.

**JSON Stringify**
Converts a JavaScript object to a JSON string.
```js
const myObject = { key1: 'value1', key2: 'value2' };
const jsonString = JSON.stringify(myObject);
```

**JSON Parse**
Parses a JSON string and returns a JavaScript object.
```js
const jsonString = '{"key1":"value1","key2":"value2"}';
const parsedObject = JSON.parse(jsonString);
```

**JSON Stringify with Replacer Function**
The `replacer` parameter can be used to filter and transform the values before stringification.
```js
const myObject = { name: 'John', age: 30, city: 'New York' };
const jsonString = JSON.stringify(myObject, (key, value) => {
    if (key === 'age') {
        return value * 2; // Double the age
    }
    return value;
});
```

**JSON Stringify with Space Parameter**
The `space` parameter can be used to add indentation to the output, making it more readable.
```js
const myObject = { key1: 'value1', key2: 'value2' };
const jsonString = JSON.stringify(myObject, null, 2);
```

**Handling JSON Errors**
When parsing JSON, it's good practice to handle potential errors.
```js
try {
    const parsedObject = JSON.parse('invalid JSON');
} catch (error) {
    console.error('Error parsing JSON:', error.message);
}
```



#javascript #phase-1 #assignment #syntax