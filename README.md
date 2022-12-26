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

###
