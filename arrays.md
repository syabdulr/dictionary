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

## Using Array Methods

```js 
const myArray = [1, 2, 3];

// Map over array and double each element
const doubledArray = myArray.map(element => element * 2); // [2, 4, 6]

// Filter array to include only even elements
const evenArray = myArray.filter(element => element % 2 === 0); // [2]
```

# Iterating through Multi-Dimensional Arrays

```js
const myArray = [
  [1, 2, 3],
  [4, 5, 6],
  [7, 8, 9]
];

// Iterate through 2D array and log each element to console
for (let i = 0; i < myArray.length; i++) {
  for (let j = 0; j < myArray[i].length; j++) {
    console.log(myArray[i][j]);
  }
}

// Output:
// 1
// 2
// 3
// 4
// 5
// 6
// 7
// 8
// 9
```

# Using a single for loop and the flat() method to iterate through a 2D Array

```js
const myArray = [
  [1, 2, 3],
  [4, 5, 6],
  [7, 8, 9]
];

// Use flat() method to flatten 2D array and iterate over it
const flattenedArray = myArray.flat();

for (let i = 0; i < flattenedArray.length; i++) {
  console.log(flattenedArray[i]);
}

// Output:
// 1
// 2
// 3
// 4
// 5
// 6
// 7
// 8
// 9
```

# Using a single for loop and forEach() method to iterate through a 2D array

```js
const myArray = [
  [1, 2, 3],
  [4, 5, 6],
  [7, 8, 9]
];

// Use forEach() method to iterate over 2D array
myArray.forEach(row => {
  row.forEach(element => {
    console.log(element);
  });
});

// Output:
// 1
// 2
// 3
// 4
// 5
// 6
// 7
// 8
// 9
```

# How Iteration Works

## How the script iterates

```js
for (let i = 0; i < myArray.length; i++) {
  for (let j = 0; j < myArray[i].length; j++) {
    console.log(myArray[i][j]);
  }
}


// First iteration  i  j
console.log(myArray[0][0]); // 1
console.log(myArray[0][1]); // 2
console.log(myArray[0][2]); // 3

// Second iteration 
console.log(myArray[1][0]); // 4
console.log(myArray[1][1]); // 5
console.log(myArray[1][2]); // 6

// Third iteration
console.log(myArray[2][0]); // 7
console.log(myArray[2][1]); // 8
console.log(myArray[2][2]); // 9
```

## transpose a 2d array in JavaScript

```javascript
const myArray = [
[1, 2, 3],
[4, 5, 6],
[7, 8, 9]
];


// Use the first sub-array of the 2D array to determine the number of columns
const numCols = myArray[0].length;

// Use the number of columns to initialize an empty 2D array
const transposedArray = Array.from({ length: numCols }, () => []);

// Iterate over the original 2D array and populate the transposed array
for (let i = 0; i < numCols; i++) {
  for (let j = 0; j < myArray.length; j++) {
    // Access the element at (j, i) in the original 2D array and add it to the transposed array
    transposedArray[i][j] = myArray[j][i];
  }
}

// Log the transposed array to the console
console.log(transposedArray);

[    ] Outer
[    ]
[    ] 

['1' , '2' , '3'] inner

[ 0  ,  1  ,  2 ] array[index]

```

## Searching for a word diagonally in JavaScript

```js
// Function to search for a word diagonally in a 2D array
const searchWordDiagonal = (letters, word) => {
  const numRows = letters.length; // Number of rows in the 2D array
  const numCols = letters[0].length; // Number of columns in the 2D array

  // Iterate over each cell in the 2D array
  for (let i = 0; i < numRows; i++) {
    for (let j = 0; j < numCols; j++) {
      if (letters[i][j] === word[0]) {
        // If the first letter of the word matches the current cell
        // Check if the word exists diagonally starting from this cell

        // Variables to track the current position in the diagonal direction
        let row = i;
        let col = j;
        let k = 0; // Index to track the current letter in the word

        // Loop while there are remaining letters in the word
        while (k < word.length) {
          // If the current cell's letter does not match the word's letter
          // or the current position goes beyond the boundaries of the array
          // break the loop and move on to the next cell
          if (
            row < 0 ||
            row >= numRows ||
            col < 0 ||
            col >= numCols ||
            letters[row][col] !== word[k]
          ) {
            break;
          }

          // Move to the next cell diagonally
          row++;
          col++;
          k++;
        }

        // If the entire word was found diagonally, return true
        if (k === word.length) {
          return true;
        }
      }
    }
  }

  // Word not found diagonally in the array
  return false;
};

// Example usage
const letters = [
  ['A', 'W', 'C', 'F', 'Q', 'U', 'A', 'L'],
  ['S', 'E', 'I', 'N', 'F', 'E', 'L', 'D'],
  ['Y', 'F', 'C', 'F', 'Q', 'U', 'A', 'L'],
  ['H', 'M', 'J', 'T', 'E', 'V', 'R', 'G'],
  ['W', 'H', 'C', 'S', 'Y', 'E', 'R', 'L'],
  ['B', 'F', 'R', 'E', 'N', 'E', 'Y', 'B'],
  ['U', 'B', 'T', 'W', 'A', 'P', 'A', 'I'],
  ['O', 'D', 'C', 'A', 'K', 'U', 'A', 'S'],
  ['E', 'Z', 'K', 'F', 'Q', 'U', 'A', 'L'],
];

const word = 'SEINFELD';

const isWordPresent = searchWordDiagonal(letters, word);
console.log(isWordPresent);
```

## Search Vertically

```js
const searchVertical = (letters, word) => {
  // Iterate through each column
  for (let i = 0; i < letters[0].length; i++) {
    let column = ''; // Initialize an empty string to store the current column

    // Concatenate the letters in the current column into a string
    for (let j = 0; j < letters.length; j++) {
      column += letters[j][i];
    }

    // Check if the column string contains the word we're looking for
    if (column.includes(word)) {
      return true;
    }
  }

  // If the word is not found vertically, return false
  return false;
};
```

# tranpose, 
## row become col, col become row

#### before transpose, 'c' is at [2][2]
```js      
  ['A', 'B', 'C'],
  ['D', 'E', 'F'],
  ['G', 'H', 'I']
```
#### after transpose, 'c' is at [2]
```js
  ['A', 'D', 'G'],
  ['B', 'E', 'H'],
0 ['C', 'F', 'I']
```

