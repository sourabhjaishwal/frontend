# JavaScript Basics

> **Purpose:** Quick revision of core JavaScript concepts without unnecessary detail.

# 1. Introduction to JavaScript

**Definition:** JavaScript is a programming language used to make web pages interactive and dynamic.

**Real-world example:** Popups, form validation, dropdown menus, animations, calculators, and interactive buttons use JavaScript.

```js
alert("Hello from JavaScript!");
console.log(document.title);
```

### HTML + CSS + JS

- **HTML** → Structure / skeleton
- **CSS** → Design / clothes
- **JavaScript** → Behavior / actions

---

# 2. Linking JavaScript with HTML

**Definition:** JavaScript can be connected to HTML using the `<script>` tag.

```html
<script src="app.js"></script>
```

```js
// app.js
console.log("Connected!");
```

### `defer`

**Definition:** `defer` makes the script execute after the HTML has been parsed.

```html
<script defer src="app.js"></script>
```

**Example:** Useful when JavaScript needs to access HTML elements without blocking page loading.

---

# 3. Browser Console

**Definition:** The browser console allows us to execute JavaScript and view output or errors directly.

```js
2 + 2; // 4
alert("Hi");
prompt("Your name?");
```

**Example:** Developers use the console to test small pieces of JavaScript while debugging a website.

---

# 4. Variables — `var`, `let`, `const`

**Definition:** Variables are containers used to store data.

```js
var name = "Harsh";
let age = 25;
const country = "India";
```

| Keyword | Reassign | Scope    |
| ------- | -------- | -------- |
| `var`   | Yes      | Function |
| `let`   | Yes      | Block    |
| `const` | No       | Block    |

```js
let city = "Bhopal";
city = "Delhi"; // Allowed

const pi = 3.14;
// pi = 4; // Error
```

**Real-world example:** `const` can store a fixed API URL, while `let` can store a changing shopping-cart count.

---

# 5. `console`, `alert`, and `prompt`

**Definition:** These are basic browser tools for output and user interaction.

```js
console.log("Hello");
console.info("Information");
console.warn("Warning");

alert("Welcome!");

let name = prompt("Enter your name:");
console.log(name);
```

**Example:** A website can use `prompt()` to ask for a user's name and `alert()` to display a welcome message.

> **Important:** `prompt()` always returns user input as a **string**.

```js
let age = prompt("Enter age:");
console.log(age + 5);
```

If the user enters `20`, the result is `"205"` because the input is a string.

---

# 6. Statements and Semicolons

**Definition:** A statement is an instruction that JavaScript executes; semicolons usually mark the end of statements.

```js
let name = "Harsh";
console.log(name);
```

JavaScript's automatic semicolon insertion means semicolons are often optional.

---

# 7. Comments

**Definition:** Comments are notes in code that JavaScript ignores during execution.

```js
// Single-line comment

/*
  Multi-line
  comment
*/
```

**Example:** Developers use comments to explain code or temporarily disable a line.

---

# 8. Expressions vs Statements

**Expression:** Code that produces a value.

```js
5 + 10; // 15
```

**Statement:** Code that performs an action or declares something.

```js
let x = 10;
```

**Easy way to remember:**
**Expression → gives a value**
**Statement → performs an instruction**

---

# 9. Data Types

**Definition:** Data types describe the kind of value stored in a variable.

### Primitive Types

```js
let age = 25; // number
let name = "Harsh"; // string
let student = true; // boolean
let x = null; // null
let y; // undefined
let id = Symbol("id"); // symbol
let big = 123456789n; // bigint
```

### Reference Type

```js
let skills = ["JS", "HTML"]; // array
let user = { city: "Bhopal" }; // object
```

Check a type using:

```js
console.log(typeof age);
console.log(typeof name);
```

---

# 10. Special Values

**Definition:** JavaScript has special values that represent unusual or invalid results.

```js
console.log(1 / 0); // Infinity
console.log(0 / 0); // NaN
console.log(Number("abc")); // NaN
console.log(undefined + 1); // NaN
```

### `null` vs `undefined`

- `undefined` → value has not been assigned.
- `null` → intentionally empty value.

```js
let username;
let selectedUser = null;
```

---

# 11. Primitive vs Reference Values

**Definition:** Primitive values are copied by value, while objects and arrays are copied by reference.

### Primitive

```js
let x = 5;
let y = x;

y = 10;

console.log(x); // 5
console.log(y); // 10
```

### Reference

```js
let obj1 = { name: "Harsh" };
let obj2 = obj1;

obj2.name = "Sheryians";

console.log(obj1.name); // Sheryians
```

**Real-world example:** Two variables pointing to the same object behave like two people sharing access to the same document.

---

# 12. Strings

**Definition:** A string is a sequence of characters used to represent text.

```js
let msg = "I love Sheryians";
```

### Common String Methods

```js
msg.slice(2, 6);
msg.split(" ");
msg.replace("love", "study at");
msg.includes("love");
```

### Template Literals

**Definition:** Template literals allow variables to be inserted directly into strings using backticks.

```js
let name = "Harsh";

console.log(`Hey ${name}, welcome to JS!`);
```

**Real-world example:** Creating dynamic messages such as `"Welcome, Rahul!"`.

---

# 13. `do...while` Loop

**Definition:** A `do...while` loop executes the code at least once before checking the condition.

```js
let i = 1;

do {
  console.log(i);
  i++;
} while (i <= 3);
```

**Real-world example:** An ATM menu may need to appear at least once before asking whether the user wants another transaction.

---

# 14. Functions

**Definition:** A function is a reusable block of code designed to perform a specific task.

```js
function add(a, b) {
  return a + b;
}

console.log(add(5, 10));
```

**Real-world example:** A payment application can have a reusable `calculateTotal()` function.

---

# 15. Parameters and Arguments

**Definition:** Parameters are variables defined by a function, while arguments are the actual values passed to it.

```js
function greet(name) {
  // name = parameter
  console.log(`Hello ${name}`);
}

greet("Rahul"); // "Rahul" = argument
```

### Default Parameter

```js
function greet(name = "Guest") {
  console.log(`Hi ${name}`);
}

greet(); // Hi Guest
```

### Rest Parameter

**Definition:** Rest parameters collect multiple remaining arguments into an array.

```js
function add(...numbers) {
  return numbers.reduce((sum, n) => sum + n, 0);
}

console.log(add(10, 20, 30));
```

### Destructured Parameter

```js
function showUser({ name, age }) {
  console.log(name, age);
}

showUser({ name: "Rahul", age: 22 });
```

---

# 16. Function Hoisting

**Definition:** Function declarations are hoisted, so they can be called before their definition.

```js
sayHello();

function sayHello() {
  console.log("Hello");
}
```

Function expressions and arrow functions should not be called before their initialization.

---

# 17. Variable Hoisting

**Definition:** Hoisting means declarations are processed before code execution.

### `var`

```js
console.log(x); // undefined

var x = 10;
```

### `let` and `const`

```js
console.log(x); // ReferenceError

let x = 10;
```

`let` and `const` remain in the **Temporal Dead Zone (TDZ)** until their declaration is executed.

---

# 18. Arguments Object

**Definition:** The `arguments` object contains the arguments passed to a normal function.

```js
function show() {
  console.log(arguments);
}

show("A", "B", "C");
```

> Arrow functions do not have their own `arguments` object.

---

# 19. Normal Function vs Arrow Function

### Normal Function

```js
function add(a, b) {
  return a + b;
}
```

### Arrow Function

```js
const add = (a, b) => a + b;
```

**Definition:** Arrow functions provide shorter syntax and do not have their own `this` or `arguments`.

**Real-world example:** Arrow functions are commonly used as callbacks with array methods.

```js
const nums = [1, 2, 3];

nums.map((n) => n * 2);
```

---

# 20. Nested Functions and Scope Chain

**Definition:** A nested function is a function inside another function, and the scope chain lets JavaScript search for variables from local scope toward outer scopes.

```js
function outer() {
  let name = "Harsh";

  function inner() {
    console.log(name);
  }

  inner();
}

outer();
```

**Scope search:**

```text
Local → Outer → Global
```

---

# 21. IIFE

**Definition:** An IIFE (Immediately Invoked Function Expression) is a function that executes immediately after being created.

```js
(function () {
  console.log("I run instantly!");
})();
```

**Real-world example:** IIFEs were commonly used to create private scope before ES6 modules.

---

# 22. Types of Functions

### Anonymous Function

A function without a name.

```js
setTimeout(function () {
  console.log("Done");
}, 1000);
```

### Callback Function

A function passed to another function to be executed later.

```js
setTimeout(() => {
  console.log("Done");
}, 1000);
```

### Higher-Order Function

A function that accepts another function or returns a function.

```js
function runTwice(fn) {
  fn();
  fn();
}

runTwice(() => console.log("Hello"));
```

### First-Class Function

**Definition:** JavaScript treats functions like values, so they can be stored, passed, and returned.

```js
const greet = function () {
  console.log("Hello");
};

greet();
```

---

# 23. Pure and Impure Functions

### Pure Function

**Definition:** A pure function produces the same output for the same input and does not modify external data.

```js
function add(a, b) {
  return a + b;
}
```

### Impure Function

**Definition:** An impure function depends on or changes data outside itself.

```js
let count = 0;

function increase() {
  count++;
  return count;
}
```

**Real-world example:** A pure function can calculate a product price, while an impure function can update a global cart count.

---

# 24. Closures

**Definition:** A closure occurs when an inner function remembers and accesses variables from its outer function even after the outer function has finished.

```js
function outer() {
  let count = 0;

  return function () {
    count++;
    console.log(count);
  };
}

const counter = outer();

counter(); // 1
counter(); // 2
```

**Easy formula:**

```text
Closure = Function + Lexical Scope
```

---

# 25. Arrays

**Definition:** An array is a collection used to store multiple values in one variable.

```js
let fruits = ["Apple", "Banana", "Mango"];
```

Another way:

```js
let numbers = new Array(10, 20, 30);
```

### Accessing Elements

```js
console.log(fruits[0]); // Apple
```

---

# 26. Common Array Methods

| Method       | Purpose                           |
| ------------ | --------------------------------- |
| `push()`     | Adds to end                       |
| `pop()`      | Removes from end                  |
| `shift()`    | Removes from beginning            |
| `unshift()`  | Adds to beginning                 |
| `indexOf()`  | Finds index                       |
| `reverse()`  | Reverses array                    |
| `sort()`     | Sorts array                       |
| `join()`     | Converts to string with separator |
| `toString()` | Converts to string                |

```js
let arr = [1, 2, 3];

arr.push(4); // [1, 2, 3, 4]
arr.pop(); // [1, 2, 3]
arr.unshift(0); // [0, 1, 2, 3]
arr.shift(); // [1, 2, 3]
```

---

# 27. Array Destructuring

**Definition:** Array destructuring extracts values from an array into separate variables.

```js
const numbers = [10, 20, 30];

const [a, b, c] = numbers;

console.log(a, b, c);
```

---

# 28. Spread Operator

**Definition:** The spread operator (`...`) expands the elements of an array or object.

```js
const arr = [1, 2, 3];

const newArr = [...arr, 4];

console.log(newArr); // [1, 2, 3, 4]
```

**Real-world example:** Creating a new shopping cart array while keeping the original cart unchanged.

---

# 29. Array Iteration

### `for` Loop

```js
const students = ["Rahul", "Priya", "Rohit"];

for (let i = 0; i < students.length; i++) {
  console.log(students[i]);
}
```

### `forEach()`

**Definition:** `forEach()` executes a function once for every array element.

```js
students.forEach((name) => {
  console.log(name);
});
```

---

# 30. `map()`

**Definition:** `map()` creates a new array by transforming every element.

```js
const nums = [1, 2, 3];

const squared = nums.map((n) => n * n);

console.log(squared); // [1, 4, 9]
```

**Real-world example:** Converting a list of product prices into prices including tax.

---

# 31. `filter()`

**Definition:** `filter()` creates a new array containing only elements that satisfy a condition.

```js
const nums = [1, 2, 3, 4];

const even = nums.filter((n) => n % 2 === 0);

console.log(even); // [2, 4]
```

**Real-world example:** Filtering products to show only those under ₹1000.

---

# 32. `reduce()`

**Definition:** `reduce()` combines all array elements into a single result.

```js
const salaries = [1000, 2000, 3000];

const total = salaries.reduce((sum, salary) => {
  return sum + salary;
}, 0);

console.log(total); // 6000
```

**Real-world example:** Calculating the total price of items in a shopping cart.

---

# 33. `some()` and `every()`

### `some()`

**Definition:** Returns `true` if at least one element satisfies the condition.

```js
[1, 3, 4].some((n) => n % 2 === 0);
// true
```

### `every()`

**Definition:** Returns `true` only if all elements satisfy the condition.

```js
[2, 4, 6].every((n) => n % 2 === 0);
// true
```

**Real-world example:** `some()` checks whether any student passed; `every()` checks whether all students passed.

---

# 34. Objects

**Definition:** An object stores related data as **key-value pairs**.

```js
const student = {
  name: "Anubhav",
  age: 24,
  course: "B.Tech",
};
```

**Real-world example:** A user account can be represented as an object containing name, email, age, and address.

---

# 35. Creating Objects

### Object Literal

```js
const user = {
  name: "Shery",
  age: 22,
};
```

### Object Constructor

```js
const person = new Object();

person.name = "Rohan";
person.age = 25;
```

---

# 36. Accessing Object Properties

**Definition:** Object properties can be accessed using dot notation or bracket notation.

```js
const car = {
  brand: "BMW",
  color: "Black",
};

console.log(car.brand);
console.log(car["color"]);
```

---

# 37. Nested Objects

**Definition:** A nested object is an object stored inside another object.

```js
const user = {
  name: "Anubhav",
  address: {
    city: "Delhi",
    pin: 110001,
  },
};

console.log(user.address.city);
```

### Nested Destructuring

```js
const {
  address: { city },
} = user;

console.log(city);
```

---

# 38. Deleting Object Properties

**Definition:** The `delete` operator removes a property from an object.

```js
const car = {
  brand: "BMW",
  color: "Black",
};

delete car.color;

console.log(car);
```

---

# 39. `Object.freeze()` and `Object.seal()`

### `Object.freeze()`

**Definition:** `freeze()` prevents adding, deleting, or modifying object properties.

```js
const user = Object.freeze({
  name: "Rahul",
});

user.name = "Aman"; // No change
```

### `Object.seal()`

**Definition:** `seal()` prevents adding or deleting properties but allows existing properties to be modified.

```js
const user = Object.seal({
  name: "Rahul",
});

user.name = "Aman"; // Allowed
```

**Easy difference:**

```text
freeze → Cannot add, delete, or modify
seal   → Cannot add/delete, but can modify
```

---

# 40. Quick Revision — Functions

| Concept               | Remember                                |
| --------------------- | --------------------------------------- |
| Function              | Reusable block of code                  |
| Parameter             | Variable in function definition         |
| Argument              | Actual value passed                     |
| Default Parameter     | Fallback value                          |
| Rest Parameter        | Collects multiple arguments             |
| IIFE                  | Runs immediately                        |
| Callback              | Function passed to another function     |
| Higher-Order Function | Takes/returns a function                |
| Closure               | Function remembers outer scope          |
| Pure Function         | Same input → same output                |
| Impure Function       | Uses/changes external state             |
| Hoisting              | Declarations processed before execution |

---

# 41. Quick Revision — Arrays

| Method / Concept | Purpose                   |
| ---------------- | ------------------------- |
| `push()`         | Add at end                |
| `pop()`          | Remove from end           |
| `shift()`        | Remove from start         |
| `unshift()`      | Add at start              |
| `map()`          | Transform elements        |
| `filter()`       | Select elements           |
| `reduce()`       | Produce one result        |
| `forEach()`      | Iterate elements          |
| `some()`         | At least one matches      |
| `every()`        | All match                 |
| Destructuring    | Extract values            |
| Spread `...`     | Expand/copy values        |
| `sort()`         | Sort elements             |
| `reverse()`      | Reverse elements          |
| `join()`         | Join elements into string |

---

# 42. Quick Revision — Important Differences

### `var` vs `let` vs `const`

```text
var   → Function scoped, can reassign
let   → Block scoped, can reassign
const → Block scoped, cannot reassign
```

### `map()` vs `forEach()`

```text
map()     → Returns a new array
forEach() → Mainly used for iteration
```

### `filter()` vs `find()`

```text
filter() → Returns all matching elements
find()   → Returns the first matching element
```

### Normal Function vs Arrow Function

```text
Normal Function → Own `this` and `arguments`
Arrow Function  → Does not have its own `this` or `arguments`
```

### Primitive vs Reference

```text
Primitive  → Copied by value
Object/Array → Copied by reference
```

### `freeze()` vs `seal()`

```text
freeze() → Nothing can be changed
seal()   → Existing values can be changed
```
