# Functions

## Asynchonous, Anonymous and Callback function

```js
function fetchData(url, callback) {
  // Simulating an asynchronous operation
  setTimeout(() => {
    const data = { name: 'John', age: 25 };
    callback(null, data); // Invoke the callback with the result
  }, 2000);
}

// Anonymous function used as a callback
fetchData('https://example.com/api', (error, result) => {
  if (error) {
    console.error('Error:', error);
  } else {
    console.log('Data:', result);
  }
});
```
# JavaScript Functions

## String Functions

```javascript

// String Functions
const stringFunctions = {
  concat: 'Joins two or more strings together.',
  includes: 'Determines whether a string contains a specific substring.',
  indexOf: 'Returns the position of the first occurrence of a specified value in a string.',
  replace: 'Replaces all occurrences of a specified value in a string with another value.',
  slice: 'Extracts a section of a string and returns a new string.',
  split: 'Splits a string into an array of substrings.',
  substr: 'Extracts a specified number of characters from a string.',
  toLowerCase: 'Converts a string to lowercase letters.',
  toUpperCase: 'Converts a string to uppercase letters.',
  trim: 'Removes whitespace from both ends of a string.'

  
};
```
## Number Functions

```js
const numberFunctions = {
  toFixed: 'Formats a number with a fixed number of digits after the decimal point.',
  toString: 'Converts a number to a string.',
}
```

## Array Functions

```js
const arrayFunctions = {
  concat: 'Joins two or more arrays together.',
  filter: 'Creates a new array with all elements that pass the test implemented by the provided function.',
  forEach: 'Executes a provided function once for each array element.',
  includes: 'Determines whether an array includes a certain element.',
  indexOf: 'Returns the first index at which a given element can be found in the array.',
  join: 'Joins all elements of an array into a string.',
  map: 'Creates a new array with the results of calling a provided function on every element in the array.',
  pop: 'Removes the last element from an array and returns that element.',
  push: 'Adds one or more elements to the end of an array and returns the new length of the array.',
  shift: 'Removes the first element from an array and returns that element.',
  slice: 'Extracts a section of an array and returns a new array.',
  splice: 'Changes the contents of an array by removing or replacing existing elements and/or adding new elements.',
  unshift: 'Adds one or more elements to the beginning of an array and returns the new length of the array.',
}
```

## Object Functions

```js
const objectFunctions = {
  assign: 
  'Copies the values of all enumerable own properties from one or more source objects to a target object.',
  create: 'Creates a new object with the specified prototype object and properties.',
  defineProperty: 'Defines a new property directly on an object, or modifies an existing property on an object.',
  entries: 'Returns an array of a given object\'s own enumerable property [key, value] pairs.',
  freeze: 'Freezes an object: other code can\'t delete or change any properties.',
  keys: 'Returns an array of a given object\'s own enumerable property names.',
  values: 'Returns an array of a given object\'s own enumerable property values.',
}
```

## Other Functions

```js
const otherFunctions = {
  setTimeout: 'Sets a timer which executes a function or specified piece of code once after the timer expires.',
  setInterval: 'Repeats the execution of a function or specified piece of code at a specified interval.',
  clearTimeout: 'Clears the delay set by setTimeout().',
  clearInterval: 'Clears the interval set by setInterval().',
}
```

## Export the functions for use in other modules

```js
module.exports = {
  stringFunctions,
  numberFunctions,
  arrayFunctions,
  objectFunctions,
  otherFunctions,
};
```
