# Arrays

## Creating an Array

```js
// Empty array
const myArray = [];

// Array with elements
const myOtherArray = [1, 2, 3];
```

## Accessing elements in an array

```js
const myArray = ['apple', 'banana', 'orange'];

// Access first element
const firstElement = myArray[0]; // 'apple'

// Access last element
const lastElement = myArray[myArray.length - 1]; // 'orange'
```

## Adding elements to an array

```js
const myArray = ['apple', 'banana'];

// Add element to end of array
myArray.push('orange'); // ['apple', 'banana', 'orange']

// Add element to beginning of array
myArray.unshift('kiwi'); // ['kiwi', 'apple', 'banana', 'orange']
```

## Removing elements from an array

```js
const myArray = ['apple', 'banana', 'orange'];

// Remove last element from array
myArray.pop(); // ['apple', 'banana']

// Remove first element from array
myArray.shift(); // ['banana', 'orange']
```

## Iterating over an array using a loop

```js
const myArray = [1, 2, 3];

// Iterate over array and log each element to console
for (let i = 0; i < myArray.length; i++) {
  console.log(myArray[i]);
}

// Output:
// 1
// 2
// 3

```