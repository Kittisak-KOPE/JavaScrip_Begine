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
