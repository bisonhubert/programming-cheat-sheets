# ES6 Cheat Sheet

- [Helper Functions](#helper-funcitons)
- [Rest & Spread](#rest-and-spread)
- [Destructuring](#destructuring)
- [Intro to Classes & Inheritance](#intro-to-classes-&-inheritance)

### Helper Functions
```javascript
// ES6 fat arrow function
const add = (a, b) => a + b;
add(1, 2);

// vs ES5 function expression
subtract = function(a, b) { return a - b; }
subtract(1, 2);

// vs ES5 function declaration
function multiply(a, b) { return a * b; }
multiply(1, 2);

// vs ES6 fat arrow function
const divide = (a, b) => a / b;
divide(1, 2);
```

### Rest and Spread
```javascript
// rest operator captures * list of arguments as an array
function addNumbers(...numbers) {
  return numbers.reduce((sum, number) => {
    return sum + number;
  }, 0);
}
addNumbers(1, 2, 3, 4, 5) // 15

// spread operator takes separate, linked values and joins them together
const defaultColors = ['red', 'green'];
const userFavoriteColors = ['orange', 'yellow'];
[...defaultColors, ...userFavoriteColors, 'blue']; // ['red', 'green', 'orange', 'yellow', 'blue'];

// mix and match the two
const MathLibrary = {
  calculateProduct(...rest) {
    console.log('Please use the multiply method instead');
    return this.multiply(...rest);
  },
  multiply(a, b) => a * b
}
```

### Destructuring
```javascript
// object destructuring
const expense = {
  type: 'Business',
  amount: '$45 USD'
};
// ES6
const { type, amount } = expense;
// ES5
const type = expense.type
const amount = expense.amount;
```

```javascript
// file summary example
let savedFile = {
  extension: 'jpg',
  name: 'repost',
  size: 14040
}
// ES5 function that prints out information about saved file
function fileSummaryES5(file) {
  return `The file ${file.name}.${file.extension} is of size ${file.size}`;
}
fileSummary(savedFile);
// ES6 destructuring within parameter list
function fileSummaryES6({ name, extension, size }) {
  return `The file ${name}.${extension} is of size ${size}`
}
```

```javascript
// destructuring arrays
const companies = [
  'Pillow Homes', 'Customer Lobby', 'Mad Science', 'Black Point Cafe', 'Whole Foods', 'GamePro'
];
const [ current, mostRecent, beforeThat ] = companies;
current; // 'Pillow Homes',
mostRecent; // 'Customer Lobby'
beforeThat; // 'Mad Science'
```

```javascript
// arrays and rest operator
const [ current, ...previous ] = companies;
current; // 'Pillow Homes'
previous; // ['Customer Lobby', 'Mad Science', 'Black Point Cafe', 'Whole Foods', 'GamePro']
```

```javascript
// destructuring arguments
const profile = {
  title: 'Engineer',
  department: 'Engineering'
};
function isEngineer({title, department}) {
//    const { title, department } = profile;
  return title === 'Engineer' && department === 'Engineering';

};
isEngineer(profile);
```

```javascript
// USE CASE: destructuring while mapping to new data structures
const classes = [
  [ 'Chemistry', '9AM', 'Mr. Darnick' ],
  [ 'Physics', '10:15AM', 'Mrs. Lithun'],
  [ 'Math', '11:30AM', 'Mrs. Vitalis' ]
];
const classesAsObject = classes.map(([subject, time, teacher]) => {
  return { subject, time, teacher };
});
classesAsObject; // returns [{"subject": "Chemistry", "time": "9AM", "teacher": "Mr. Darnick"}, {"subject": "Physics", "time": "10:15AM", "teacher": "Mrs. Lithun"}, {"subject": "Math", "time": "11:30AM", "teacher": "Mrs. Vitalis"}]
```

### Intro to Classes & Inheritance
// ES5 prototype inheritance
function Car(options) {
  this.title = options.title;
}
Car.prototype.drive = function() {
  return 'vroom';
}
function Car(options) {
  this.title = options.title;
}
function Toyota(options) {
  Car.call(this, options);
  this.color = options.color;
}
Toyota.prototype = Object.create(Car.prototype);
Toyota.prototype.constructur = Toyota;
Toyota.prototype.honk = function() {
  return 'beep';
}
const toyota = new Toyota({ color: 'red', title: 'Daily Driver' });
toyota;
toyota.honk();

// refactored for ES6
class Car {
  constructor({title}) {
    this.title = title;
  }
  drive() {
    return 'vroom'
  }
};
class Toyota extends Car {
  constructor(options) {
    super(options);
    this.color = options.color;
  }
  honk() {
    return 'beep';
  }
}
const toyota = new Toyota({ color: 'red' , title: 'Daily Driver'});
toyota.honk();
toyota.color;
toyota.drive();
