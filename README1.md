## JavaScrip Basics

### inline Javascript

```
<button onclick="alert('hello world')">click me</button>
```

### Internal Javascript

```
btn.btn*7{random button}
```

```
<button class="btn">random button</button>
<button class="btn">random button</button>
<button class="btn">random button</button>
<button class="btn">random button</button>
<button class="btn">random button</button>
<button class="btn">random button</button>
<button class="btn">random button</button>
<script>
    document.querySelectorAll(".btn").forEach((item) => {
        item.addEventListener("click", () => {
          alert("this is good");
        });
      });
</script>
```

### External Javascript

app.js

```
document.querySelectorAll(".btn").forEach((item) => {
  item.addEventListener("click", () => {
    alert("this is good");
  });
});
```

about.html

```
<a href="index.html">home</a>
    <h4>about page</h4>
    <button class="btn">random button</button>
    <button class="btn">random button</button>
    <button class="btn">random button</button>
    <button class="btn">random button</button>
    <button class="btn">random button</button>
    <button class="btn">random button</button>
    <button class="btn">random button</button>
    <script src="./app.js"></script>
```

### Helper Methods

app.js

```
document.write("hello world");
alert("hello people");
console.log("hello world");
```

```
document.write({ name: "john" });
alert({ name: "john" });
console.log({ name: "john" });
```

### Variables

// Variable - Most Basic Building Block
// Variables - Store, Access, Modify === Value
// Declare, Assignment Operator, Assign Value

### Assign Variable Value Later

// assign value later, modify existing

### Variable Naming Rules

can contain digits, letters, underscore, $
must start wit letter, $ ro \_
no keyword
cannot start with number
case sensitive - fullname vs Fullname
camelCase or underscore

### const, let, var

const can't re-assign

### Variables Challanges

Variables 1

1. create "firstName" and "last_name" variables
2. assign your values
3. create "address" variable and assign "main street" value to it
4. re-assign address to "first street" later
5. log all values in the console

```
const firstName = "john";
const last_name = "smilga";

let address = "main street";
address = "first street";
console.log(address);
```

### Quotation Masks

"" or ''

### String Concatenation

String Concatenation - combine string values
`` - backticks (template strings) easier option.

```
const name = 'john';
const lastName = 'shakeandbake';
let fullName = name + ' ' + lastName;

console.log('Hello there your full name is : ' + fullName);
```

### String Concat Challenge

1. Create "street" and "country" variables
2. assign your values
3. create "fullMailingAddress" variable and assign the result of "street + country"
4. remember about the space
5. log "fullMailingAddress" in the console

```
const street = 'main street';
const country = 'USA';

const fullMailingAddress = street + ' ' + country;
console.log(fullMailingAddress);
```

### Numbers Basics

Loosely Typed = don't declare type

```
const number = 34;
let pants = 2.466;
pants = 'are great';

console.log(number);
console.log(pants);
```

### Numbers - Additional Features

+=, -=, /=, \*=, ++, --, %
Modulus (%) operator returns the remainder after integer division

### Numbers Challenge

1. Create "score1", "score2", "score3" variables and assign values (0-100)
2. calculate total score and average score, and assign them to the variables.
3. log total score and average score
4. create "plates" variable and assign 20
5. create "people" variable and assign 7
6. calculate remaining plates and assign to the variable
7. add one to remaining plates
8. create message variable and display 'There are (your value goes here) plates available' -string concatenation
9. log message

```
const score1 = 98;
const score2 = 75;
const score3 = 45;

const totalScore = score1 + score2 + score3;
const avgScore = totalScore / 3;
console.log(totalScore, avgScore);

const plates = 20;
const people = 7;
let remainingPlates = plates % 7;
remainingPlates++;

const message = 'There are' + remainingPlates + 'plates available';
console.log(remainingPlates);

```

### Implicit Type Conversion

```
const name = 'john';
const lastName = 'jordan';

const value = name - lastName;
console.log(value);
```

index.html

```
<h1>javascript tutorial</h1>
<form class="form">
  <label for="amount">Enter Number</label>
  <input type="number" id="amount" />
  <button type="submit">Submit</button>
</form>
<script src="./app.js"></script>
```

app.js

```
const randomNumber = 13;
document.querySelector(".form").addEventListener("submit", function (e) {
  e.preventDefault();
  let value = document.getElementById("amount").value;
  //   value = parseInt(value);
  console.log("Input Value Type");
  console.log(value);
  console.log("Sum of Two Values");
  console.log(randomNumber + value);
});
```

### Data Types

Data Types = 7 total
Primitive - String, Number, Boolean, Null, Undefined, Symbol
Object - Arrays, Functions, Objects

typeof - operator (typeof variable) (typeof value)

String

Number

Boolean

Null <--- type object

Undefined

Symbol (ES6)

### Array

Arrays, Functions and Objects
Arrays - [], 0 index based

### Array Challenge

1.  Create "fruits" array and store some fruit values
2.  setup the last item as number (random)
3.  assign first fruit to the variable
4.  re-assign last array item to the actual fruit
5.  log both first fruit variable and entire fruits array

```
const fruits = ['apple', 'banana', 'orange', 45];

const firstFruit = fruits[1];
fruits[3] = 'lemon';
console.log(firstFruit);
```

### Functions - Declare, Invoke

```
function hello(){
  console.log('Hello There Bob');
  console.log('Hello There John');
  console.log('Hello There Susy');
}

hello();
```

### Functions - Parameters, Arguments

```
function helloBob(){
  console.log('Hello There Bob');
}
function helloJohn(){
  console.log('Hello There John');
}

helloBob();
helloJohn();
```

...

```
function greet(name){
  console.log('Hello there ' +name);
}

greet(4);
greet('Bob');
greet('Anna')
```

### Function - Return

Arrays, Functoions and Objects
return
default undefined, shortcuts, ignores after
1 inch 2.54 cm

```
const wallHeight = 80;

function calculate(value){
  return value * 2.54;
  console.log('hello');
}

calculate(200);
const width = calculate(100);
const height = calculate(wallHeight);

const dimensions = [width, height];
console.log(dimensions);
```

### Function Expressions

Arrays, Functions and Objects
expressions - another way define a function
create a variable, assign to FUNCTION (not value), use var
diff - hoisting, use - arrow func, libraries,

```
//function definition/declaration
function addValues(num1, num2){
  return num1 + num2;
}
const firstValue = addValues(3, 4);
const secondValue = addValues(12, 34);

//function expression
const add = function(num1, num2){
  return num1 + num2;
};
const thirdValue = add(5, 6);


const values1 = [firstValue, secondValue, thirdValue];
const values2 = [add(5, 6)];
console.log(values2);

const multiply = (num1, num2) => num1 * num2;

exports.nameOfMethod = function(){

}
```

### function Challenge

1. create "calculateTotal" function
2. add two parameters subTotal, tax
3. return sum of parameters
4. create 3 vars "order1", "order2", "order3"
5. call calculateResult, pass in some values and assign result to each order
6. log all three orders
7. refactor "calculateTotal" to function expression

```
const calculateTotal = function (subTotal, tax){
  return subTotal + tax;
}

const order1 = calculateTotal(100, 10);
const order2 = calculateTotal(50, 5);
const order3 = calculateTotal(25, 5);

console.log(order1, order2, order3);
```

### Objects

Arrays, Functions and Objects
Objects - key/value pairs methods
dot natation

```
const person = {
  name: 'john',
  lastName: 'peters',
  age: 40,
  education: false,
  married: true,
  siblings: ['anna', 'susan', 'peter],
  greeting: function (){
    console.log('Hello my name is JOHN');
  },
};

const age = person.age;
console.log(age);

person.name = 'bob';
console.log(person.name);

console.log(person.sibling[2]);

person.greeting();
```

### Object Challenge

1. create car object
2. add make, model, year, colors (array),
   hybrid (boolean) keys
3. add tow methods (drive and stop)
4. in the function body setup log with random text
5. log make
6. log first color
7. invoke both methods

```
const car = {
  make: "Dodge",
  model: "Challenger",
  year: 1970,
  colors: ["black", "red"],
  hybrid: false,

  drive: function () {
    console.log("driving...");
  },

  stop() {
    console.log("stopped!!!");
  },
};

console.log(car.make);
console.log(car.colors[0]);
car.drive();
car.stop();
```

### Conditional Statements - Basics

" >, <, >=, <=, == , === , != , !=== "

```
const value = 2 > 1;

const value2 = 1 > 2;
if (value) {
  console.log("hello world");
} else {
  console.log("hello people");
}
```

```
const num1 = 6;
const num2 = 6;
const result = num1 >= num2;

const value = false;

if (!value) {
  console.log("value is false");
}
```

### Equality

== check only value
=== checks value and type

```
const num1 = 6;
const num2 = '6';

const value = num1 == num2;
const value2 = num1 === num2;

console.log(value);
console.log(value2);
```

### Logical Operators

(|| - OR), (&& - AND), !

```
const name = "bob";
const age = 26;

if (name === "bob" || age === 24) {
  //if (name !== "bob" && age === 24) {
  console.log("hello there user");
} else {
  console.log("wrong values");
}
```

### Switch Statement

dice values : 1 - 6

```
const dice = 3;

switch (dice) {
  case 1:
    console.log("you got one");
    break;
  case 2:
    console.log("you got two");
    break;
  case 3:
    console.log("you got three");
    break;
  default:
    console.log("you did not roll the dice");
}
```

### Conditionals Challenge

1. create two objects "person1", "person2"
2. setup name, age (15-25),
   status ('resident', 'tourist') keys
3. setup if else, condition where age must be bigger than 18 and status must be equal to 'resident'
4. test with both objects

```
const person1 = {
  name: "susan",
  age: 25,
  status: "resident",
};

const person2 = {
  name: "bobo",
  age: 30,
  status: "tourist",
};

if (person2.age >= 18 && person2.status === "resident") {
  console.log("you can cast a vote");
} else {
  console.log("you are not eligible");
}
```

### while loops

repeatedly run a block of code while condition is true
while loop
TURN OF AUTOSAVE

```
let amount = 10;

while(amount > 0){
  console.log('I have ' + amount + "dollars and I'm going to the mall");
  amount--;
}
```

### do while loops

code block first, condition second
runs at least

```
let money = 12;
do {
  console.log("You have " + money + " dollars");
  money++;
} while (money < 10);
```

### for loop

```
for(let number = 11; number >= 0; number--){
  console.log('and the number is : ' + number);
}
```
