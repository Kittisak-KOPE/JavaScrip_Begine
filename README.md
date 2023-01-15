## JavaScrip Continued

### String Properties and Methods

```
let text = " Peter Jordan";

let result = text.length;
console.log(result);

console.log(text.length);
console.log(text.toLowerCase());
console.log(text.toUpperCase());
console.log(text.charAt(12));
console.log(text.charAt(text.length - 1));
console.log(text.indexOf("p"));
console.log(text.indexOf("P"));

console.log(text);
console.log(text.trim());
console.log(text.startsWith(" Peter"));
console.log(text.trim().toLowerCase().startsWith("peter"));
console.log(text.includes("eter"));
console.log(text.slice(0, 3));
console.log(text.slice(-3));
```

### Template Literals

Template Literals - ES6+
Backtick characters `` - above tab (left form one)
Interpolation ${} - insert expression(value)

```
const name = "John";
const age = 25;

const sentence = "Hey it's " + name + " and he is " + age + " years old";
console.log(sentence);

const value = `Hey it's ${name} and he is ${age} years old. And here is some simple math ${
  4 + 4
}`;
console.log(value);
```

### String Challenge

1. Create function fullName
2. Accept two parameters "firstName", "lastName"
3. Add them together (concat) and return result in uppercase
4. invoke fullName and pass some values
5. log result
6. change the order of arguments
7. refactor to object parameter

```
function fullName(firstName, lastName) {
  const fullName = `${firstName} ${lastName}`;
  return fullName.toUpperCase();
}

console.log(fullName("john", "smith"));
console.log(fullName("jordan", "peter"));
```

...

```
function fullName({ firstName, lastName }) {
  const fullName = `${firstName} ${lastName}`;
  return fullName.toUpperCase();
}

console.log(fullName({ lastName: "jordan", firstName: "peter" }));
```

### Array Properties and Methods

```
let names = ["john", "bobo", "barry", "olga", "ben"];

//length
console.log(names.length);
console.log(names[4]);
console.log(names[names.length - 1]);

//concat
const lastNames = ["pepper", "onion", "banana"];
const allNames = names.concat(lastNames);
console.log(allNames);

//reverse
console.log(allNames.reverse());

//unshift
allNames.unshift("susy");
console.log(allNames);

//shift
allNames.shift();
console.log(allNames);

//push
allNames.push("susy");
console.log(allNames);

//;pop
allNames.pop();
console.log(allNames);

//splice - mutates original array
const specificName = allNames.splice(2, 1);
console.log(specificName);
console.log(allNames);
```

### Exercise - Full Name

```
const names = ["anna", "susy", "bob"];
const lastName = "shakeandbake";
let newArray = [];

//for loop
for (let i = 0; i < names.length; i++) {
  console.log(i);
  console.log(names[i]);

  newArray.push(`${names[i]} ${lastName}`);
}

console.log(names);
console.log(newArray);
```

### Exercise - Calculate Total

functions, return, if, arrays, for loop

```
const gas = [10, 40, 100, 30];
const food = [10, 40, 50];

function calculateTotal(arr) {
  let total = 0;
  for (let i = 0; i < arr.length; i++) {
    // console.log(arr[i]);
    total += arr[i];
  }
  if (total > 100) {
    console.log(`Whoa! You are spending way too much`);
    return total;
  }
  console.log(`You are good total is less than 100`);
  return total;
}

const gasTotal = calculateTotal(gas);
const foodTotal = calculateTotal(food);
const randomTotal = calculateTotal([200, 4000, 500, 1]);

console.log({
  gas: gasTotal,
  food: foodTotal,
  random: randomTotal,
});
```

### Value vs Reference

Primitive Data Types
String, Number, Symbol, Boolean, Undefined, Null,
Arrays, Functions, Objects = object
typeof

when assigning primitive data type value to a variable any changes are made directly to that value, without affecting original value

when assigning non-primitive data type value to a variable is done by reference so any changes will affect all the references.

```
const number = 1;
let number2 = number;
number2 = 7;

console.log(`the first value is ${number}`);
console.log(`the second value is ${number2}`);

let person = { name: "bob" };

// let person2 = person;
let person2 = { ...person };

person2.name = "susy";
console.log(`the name of the first person is ${person.name}`);
console.log(`the name of the second person is ${person2.name}`);
```

### Null and Undefined

both represent "no value"

undefined - "javascript can not find value for this"

variable without value
missing function arguments
missing object properties

null - "deverloper sets the value"

```
let number = 20 + null; // 20 + 0
console.log(number);
let number2 = 20 + undefined; // 20 + 0;
console.log(number2);
```

## Truthy and Falsy

"", '', ``, 0, -0, NaN, False, null, undefine

```
// "", '', ``, 0, -0, NaN, False, null, undefine
const bool1 = true;
const bool2 = 2 > 1;

const text = undefined;

if (text) {
  console.log("hey the value Truthy");
} else {
  console.log("hey the value Falsy");
}
```

### Ternary Operator

```
// unary operator - typeof
let text = "some text";
console.log(typeof text); //operand

// binary operator - assignment
let number = 3;
let number2 = 2 + 5;

// ternary operator
// condition ? (runs if true) : (runs if false)
const value = 2 > 1;

value ? console.log("value is true") : console.log("value is false");
```

### Global Scope

any variable outside code block {} is said to be in global Scope can be access anywhere in the program Gotchas : name collisions, modify by mistake

```
let name = "bobo";
name = "peter";

function calculate() {
  // some other code ...
  console.log(name);
  name = "orange";
  function inner() {
    name = "inner name value";
    console.log(`this is from inner function ${name}`);
  }
  inner();
}

calculate();

if (true) {
  //some other code ...
  console.log(name);
  name = "pants";
}

console.log(`my name is ${name} and I'm awesome`);
```

### Local Scope

can not access from outside code blocks
if - NOT VAR

```
let name = "bobo";

function calculate() {
  const name = "john";
}

calculate();

if (true) {
  const name = "john";
}

console.log(`my name is ${name} and I'm awesome`);
```

```
let name = "bobo";

function calculate() {
  const name = "john";
  const age = 25;
  // code goes here
  becomesGlobal = "global variable";
}

calculate();
// console.log(age);
console.log(becomesGlobal);

if (true) {
  const name = "john";
}

console.log(`my name is ${name} and I'm awesome`);
```

### Variable Lookup

{} = code block

```
const globalNumber = 5;

function add(num1, num2) {
  //   const globalNumber = 20;
  const result = num1 + num2 + globalNumber;
  function multiply() {
    // const globalNumber = 100;
    const multiplyResult = result * globalNumber;
    console.log(multiplyResult);
  }
  //   console.log(multiplyResult);

  multiply();
  return result;
}

console.log(add(3, 4));
```

## Calback Functions, Higher Order Functions

- Functions are first class objects - stored in a variable (expression), passed as an argument to another function, return from the function (closure).
- Higher Order function - accepts another function as an argument or returns another function as a result.
- Callback Function - passed to a another function as an argument and executed inside that function

```
// function greeMorning(name) {
//   const myName = "john";
//   console.log(`Good morning ${name}, my name is ${myName}`);
// }

// greeMorning("bobo");

// ---------------------------------------------------------------

// function morning() {
//   console.log("Good morning Bob");
//   return "Good morning Bob";
// }

// function greet(name, cb) {
//   const myName = "john";
//   console.log(`${name}, my name is ${myName}`);
//   cb();
// }

// ---------------------------------------------------------------

function morning(name) {
  return `Good morning ${name.toUpperCase()}`;
}

function afternoon(name) {
  return `Good afternoon ${name.repeat(3)}`;
}

function greet(name, cb) {
  const myName = "john";
  console.log(`${cb(name)}, my name is ${myName}`);
}

greet("bobo", morning);

greet("peter", afternoon);
```
