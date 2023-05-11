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

```js
let car = {
  make: 'Toyota',
  model: 'Camry',
  year: 2018
};

delete car.year;

console.log(car); // Outputs: { make: 'Toyota', model: 'Camry' }
```

## Methods in Objects

```js
let car = {
  make: 'Toyota',
  model: 'Camry',
  year: 2018,
  startEngine: function() {
    console.log('Engine started');
  }
};

car.startEngine(); // Outputs: 'Engine started'
```

## Nested Objects

```js
let person = {
  name: 'John',
  age: 30,
  address: {
    street: '123 Main St',
    city: 'New York',
    country: 'USA'
  }
};

console.log(person.address.street); // Outputs: '123 Main St'
```

## Iterating Over Object Properties

```js
let car = {
  make: 'Toyota',
  model: 'Camry',
  year: 2018
};

for (let key in car) {
  console.log(`${key}: ${car[key]}`);
}

// Outputs:
// 'make: Toyota'
// 'model: Camry'
// 'year: 2018'
```

## Object Destructuring

```js
let car = {
  make: 'Toyota',
  model: 'Camry',
  year: 2018
};

let {make, model, year} = car;

console.log(make); // Outputs: 'Toyota'
console.log(model); // Outputs: 'Camry'
console.log(year); // Outputs: 2018
```

## Checking for Property Existence

```js
let car = {
  make: 'Toyota',
  model: 'Camry',
  year: 2018
};

console.log('make' in car); // Outputs: true
console.log('color' in car); // Outputs: false
```

# General Notes

<p> 

- 2 different notations to access objects <br> dot notation and square bracket notation 

- const inspect = require('util').inspect; // this line prints the key pair value 
</p>