# Objects

## Creating Objects
```js
// Object Literal
let obj1 = {};

// Object Constructor
let obj2 = new Object();
```

## Adding Properties to Objects
```js 
let car = {
  make: 'Toyota',
  model: 'Camry',
  year: 2018
};

// Using dot notation
car.color = 'Red';

// Using bracket notation
car['price'] = 30000;

console.log(car); 
// Outputs: { make: 'Toyota', model: 'Camry', year: 2018, color: 'Red', price: 30000 }

```

## Accessing Properties
```js
let car = {
  make: 'Toyota',
  model: 'Camry',
  year: 2018
};

// Using dot notation
console.log(car.make); // Outputs: 'Toyota'

// Using bracket notation
console.log(car['model']); // Outputs: 'Camry'

```

## Deleting Properties
```



const inspect = require('util').inspect; // this line prints the key pair value 

<p> 2 different notations to access objects <br> dot notation and square bracket notation </p>