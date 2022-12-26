# JavaScrip Basics

## inline Javascript

```
<button onclick="alert('hello world')">click me</button>
```

## Internal Javascript

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

## External Javascript

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

## Helper Methods

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

## Variables

// Variable - Most Basic Building Block
// Variables - Store, Access, Modify === Value
// Declare, Assignment Operator, Assign Value

## Assign Variable Value Later

// assign value later, modify existing

## Variable Naming Rules

can contain digits, letters, underscore, $
must start wit letter, $ ro \_
no keyword
cannot start with number
case sensitive - fullname vs Fullname
camelCase or underscore

## const, let, var

const can't re-assign

## Variables Challange

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
```

## Quotation Masks

"" or ''

## String Concatenation

String Concatenation - combine string values
`` - backticks (template strings) easier option.

```
const name = 'john';
const lastName = 'shakeandbake';
let fullName = name + ' ' + lastName;

console.log('Hello there your full name is : ' + fullName);
```

## k
