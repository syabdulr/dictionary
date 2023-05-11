# Basic Syntax Fundamentals

## Variables and Constants

Variables are used to store and manipulate data. They are declared using the var, let, or const keyword.
var is the older way to declare variables, while let and const were introduced in ES6 (ECMAScript 2015).
Variables declared with let can be reassigned, while variables declared with const are read-only and cannot be reassigned.

Example:
```js
let age = 25;
const name = 'John';
```

## 7 Data Types
```js
let age = 25; 
// Number: represents numeric values.

let name = 'John'; 
// String: represents textual data.

let isStudent = true; 
// Boolean: represents true or false.

let numbers = [1, 2, 3]; 
// Array: represents an ordered collection of values

let person = { name: 'Alice', age: 30 }; 
// represents a collection of key-value pairs.

let emptyValue = null; 
// represents the intentional absence of any object value.

let undefinedValue;
// represents an uninitialized variable.
```

## Operators
JavaScript supports various operators for performing operations on data, such as arithmetic, assignment, comparison, logical, and more.
```js
let x = 10;
let y = 5;
let sum = x + y; // Arithmetic operator (+)
let isGreater = x > y; // Comparison operator (>)
let logicalResult = (x > 5) && (y < 10); // Logical operator (&&)
```

## Control Flow
Control flow statements help control the execution order of code based on conditions.
Common control flow statements include if...else, switch, for, while, and do...while.

```js
let hour = 12;
if (hour < 12) {
  console.log('Good morning!');
} else if (hour < 18) {
  console.log('Good afternoon!');
} else {
  console.log('Good evening!');
}
```

## Functions

Functions are reusable blocks of code that perform a specific task.
They can be defined using the function keyword or as arrow functions (() => {}).
Functions can accept parameters and return values.

```js
function greet(name) {
  console.log('Hello, ' + name + '!');
}
greet('John'); // Output: Hello, John!
```
# Advanced Syntax Fundamentals in JavaScript

## Arrow Functions:
Arrow functions provide a concise syntax for writing function expressions.
They are particularly useful for writing shorter functions and for maintaining lexical scoping of this.
```js
const add = (a, b) => a + b;
```

## Template Literals:
Template literals (also known as template strings) allow embedding expressions within string literals using backticks ( ).
They support multi-line strings and variable interpolation using ${}.
```js
const name = 'John';
const message = `Hello, ${name}!`;
```

## Destructuring Assignment:
Destructuring assignment allows you to extract values from arrays or objects into distinct variables.
It provides a concise way to unpack values.

```js
const numbers = [1, 2, 3];
const [a, b, c] = numbers;
```

## Spread Syntax:
The spread syntax allows you to expand elements from an array or object into another array, function arguments, or object literals.
It provides a concise way to combine or copy arrays and objects.
```js
const arr1 = [1, 2, 3];
const arr2 = [4, 5, 6];
const combined = [...arr1, ...arr2];
```

## Promises:
Promises are objects representing the eventual completion or failure of an asynchronous operation and its resulting value.
They provide a better way to handle asynchronous code than using callbacks.
Promises have methods such as then() and catch() to handle the fulfillment or rejection of the promise.

```js
const fetchData = () => {
  return new Promise((resolve, reject) => {
    // Asynchronous operation
    if (success) {
      resolve(data);
    } else {
      reject(error);
    }
  });
};
```

## async/await:
async and await keywords provide syntactic sugar for working with Promises and making asynchronous code appear more synchronous.
They allow you to write asynchronous code in a more sequential and readable manner.

```js
const fetchData = async () => {
  try {
    const result = await asyncOperation();
    // Handle result
  } catch (error) {
    // Handle error
  }
};
```