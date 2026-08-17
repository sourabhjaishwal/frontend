# Advance JavaScript

> **Purpose:** This section contains OOP, `this`, asynchronous JavaScript, callbacks, promises, fetch, error handling, debouncing, throttling, JSON, and built-in functions/methods.

# 1. Object-Oriented Programming (OOP)

OOP helps organize JavaScript code using:

- Objects
- Classes
- Constructors
- Prototypes
- Inheritance

---

## Objects

An object stores **data and behavior together**.

```js
const user = {
  name: "Anubhav",
  age: 24,

  greet() {
    console.log(`Hello, I am ${this.name}`);
  },
};

user.greet();
```

---

# 2. Classes

A **class** is a blueprint for creating objects.

```js
class Car {
  constructor(brand, price) {
    this.brand = brand;
    this.price = price;
  }

  drive() {
    console.log(`${this.brand} is driving...`);
  }
}

const car1 = new Car("BMW", 5000000);

car1.drive();
```

### Remember

```text
Class  → Blueprint
Object → Instance created from class
```

---

# 3. Constructor

A constructor initializes object properties.

```js
class Student {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }
}

const s1 = new Student("Anubhav", 24);
```

The constructor automatically runs when `new` is used.

---

# 4. Prototype

JavaScript uses prototypes to share methods between objects.

```js
function Person(name) {
  this.name = name;
}

Person.prototype.sayHi = function () {
  console.log(`Hi, I am ${this.name}`);
};

const p1 = new Person("Anubhav");

p1.sayHi();
```

### Why prototypes?

Instead of creating a separate copy of a method for every object, objects can share the same method through the prototype.

---

# 5. Class Expression

Classes can also be created using expressions.

### Anonymous Class

```js
const Person = class {
  constructor(name) {
    this.name = name;
  }
};

const p = new Person("Anubhav");
```

### Named Class Expression

```js
const Car = class CarClass {
  constructor(model) {
    this.model = model;
  }
};

const c = new Car("BMW");
```

---

# 6. Class Hoisting

Classes are **not hoisted** like function declarations.

```js
const obj = new Student();

class Student {
  constructor() {}
}
```

This produces a `ReferenceError`.

The class must be declared before it is used.

---

# 7. Inheritance

Inheritance allows one class to use properties and methods from another class.

```js
class Animal {
  speak() {
    console.log("Animal speaks");
  }
}

class Dog extends Animal {
  bark() {
    console.log("Dog barks");
  }
}

const d = new Dog();

d.speak();
d.bark();
```

### Important Keywords

```text
extends → inherits from another class
super() → calls parent constructor
```

---

# 8. Getter and Setter

Getters read a property through a method-like syntax.

Setters control how a property is changed.

```js
class User {
  constructor(name) {
    this._name = name;
  }

  get name() {
    return this._name.toUpperCase();
  }

  set name(value) {
    this._name = value;
  }
}

const user = new User("anubhav");

console.log(user.name);

user.name = "Jha";

console.log(user.name);
```

---

# 9. Constructor Functions

Before ES6 classes, constructor functions were commonly used for creating objects.

```js
function Animal(name) {
  this.name = name;
}

const animal = new Animal("Kitty");
```

Methods can be added through prototypes.

```js
Animal.prototype.speak = function () {
  console.log(this.name + " makes a sound");
};
```

---

# 10. `this` Keyword

`this` refers to a value determined by **how a function is called**.

```js
const obj = {
  name: "Anubhav",

  show() {
    console.log(this.name);
  },
};

obj.show();
```

Output:

```text
Anubhav
```

---

## `this` in Different Situations

### Global Scope

In a browser's classic script:

```js
console.log(this);
```

Usually refers to:

```text
window
```

> Note: behavior differs in ES modules and strict mode.

---

### Normal Function

In non-strict browser code:

```js
function show() {
  console.log(this);
}

show();
```

`this` is generally `window`.

In strict mode, `this` is `undefined`.

---

### Object Method

```js
const obj = {
  name: "Anubhav",

  show() {
    console.log(this);
  },
};

obj.show();
```

Here, `this` refers to `obj`.

---

### Arrow Function

Arrow functions do not create their own `this`.

```js
const obj = {
  name: "Anubhav",

  show: () => {
    console.log(this);
  },
};
```

The arrow function takes `this` from its surrounding lexical scope.

---

### Nested Function

```js
const obj = {
  name: "Anubhav",

  outer() {
    function inner() {
      console.log(this);
    }

    inner();
  },
};
```

The normal nested function has its own `this` behavior.

---

### Arrow Function Inside Method

```js
const obj = {
  name: "Anubhav",

  outer() {
    const inner = () => {
      console.log(this);
    };

    inner();
  },
};

obj.outer();
```

The arrow function inherits `this` from `outer()`.

---

# 11. `call()`

`call()` executes a function with a specified `this` value.

```js
function hello() {
  console.log(`Hello ${this.name}`);
}

hello.call({ name: "Anubhav" });
```

Arguments are passed individually.

```js
function sum(a, b) {
  console.log(this.name, a + b);
}

sum.call({ name: "Total:" }, 10, 20);
```

---

# 12. `apply()`

`apply()` is similar to `call()`.

The main difference is that arguments are passed as an array.

```js
function sum(a, b) {
  console.log(this.name, a + b);
}

sum.apply({ name: "Total:" }, [10, 20]);
```

### Difference

```text
call(object, arg1, arg2)

apply(object, [arg1, arg2])
```

---

# 13. `bind()`

`bind()` returns a new function with a fixed `this`.

```js
function welcome() {
  console.log("Welcome", this.user);
}

const newFn = welcome.bind({
  user: "Anubhav",
});

newFn();
```

Useful when a function needs to be executed later.

---

# 14. Synchronous JavaScript

Synchronous JavaScript executes code in order.

```js
console.log("A");
console.log("B");
console.log("C");
```

Output:

```text
A
B
C
```

---

# 15. Asynchronous JavaScript

Asynchronous operations allow JavaScript to continue running while waiting for certain tasks.

Common examples:

```text
setTimeout()
fetch()
DOM events
```

Example:

```js
console.log("A");

setTimeout(() => {
  console.log("B");
}, 2000);

console.log("C");
```

Output:

```text
A
C
B
```

---

# 16. `setTimeout()`

Runs a function once after a specified delay.

```js
setTimeout(() => {
  console.log("Executed after 2 seconds");
}, 2000);
```

### Canceling a Timeout

```js
const timer = setTimeout(() => {
  console.log("Will not run");
}, 3000);

clearTimeout(timer);
```

---

# 17. `setInterval()`

Repeatedly executes a function after a fixed interval.

```js
const interval = setInterval(() => {
  console.log("Hello");
}, 1000);
```

---

# 18. `clearInterval()`

Stops an interval.

```js
let count = 1;

const id = setInterval(() => {
  console.log(count);

  count++;

  if (count === 5) {
    clearInterval(id);
  }
}, 1000);
```

---

# 19. Callbacks

A callback is a function passed to another function.

```js
function greet(name, callback) {
  console.log("Hello " + name);

  callback();
}

greet("Anubhav", () => {
  console.log("Welcome!");
});
```

---

# 20. Callback Hell

Callback hell occurs when callbacks become deeply nested.

```js
getData(function (data1) {
  getMoreData(data1, function (data2) {
    getMoreMoreData(data2, function (data3) {
      getFinalData(data3, function (result) {
        console.log(result);
      });
    });
  });
});
```

Problems:

- Hard to read
- Difficult to debug
- Difficult to maintain
- Creates deeply nested code

Promises and `async/await` help solve this problem.

---

# 21. Promises

A Promise represents the eventual result of an asynchronous operation.

### States

```text
pending
fulfilled
rejected
```

### Creating a Promise

```js
const myPromise = new Promise((resolve, reject) => {
  const success = true;

  if (success) {
    resolve("Operation Successful!");
  } else {
    reject("Operation Failed!");
  }
});
```

---

# 22. `.then()` and `.catch()`

```js
myPromise
  .then((result) => {
    console.log(result);
  })
  .catch((error) => {
    console.error(error);
  });
```

### Basic Flow

```text
Promise
   ↓
.then()  → success
.catch() → failure
```

---

# 23. Promise with `setTimeout()`

```js
function waitForMe() {
  return new Promise((resolve) => {
    setTimeout(() => {
      resolve("2 seconds completed!");
    }, 2000);
  });
}

waitForMe().then((msg) => {
  console.log(msg);
});
```

---

# 24. `async`

An `async` function always returns a Promise.

```js
async function example() {
  return "Hello";
}

example().then(console.log);
```

---

# 25. `await`

`await` waits for a Promise to settle inside an `async` function.

```js
function delay(ms) {
  return new Promise((resolve) => {
    setTimeout(() => {
      resolve("Done waiting!");
    }, ms);
  });
}

async function run() {
  console.log("Waiting...");

  const result = await delay(2000);

  console.log(result);
}

run();
```

---

# 26. `fetch()`

`fetch()` is a browser API used for making HTTP requests.

It returns a Promise.

```js
fetch(url)
  .then((response) => response.json())
  .then((data) => {
    console.log(data);
  })
  .catch((error) => {
    console.error(error);
  });
```

---

## Fetch with `async/await`

```js
async function getUser() {
  try {
    const response = await fetch(
      "https://jsonplaceholder.typicode.com/users/1",
    );

    const data = await response.json();

    console.log(data);
  } catch (error) {
    console.error("Error:", error);
  }
}

getUser();
```

---

# 27. `response.json()`

`response.json()` reads the response body and converts JSON data into a JavaScript value.

```js
const response = await fetch(url);

const data = await response.json();

console.log(data);
```

---

# 28. Error Handling

Error handling helps applications deal with unexpected problems.

Main tools:

```text
try
catch
finally
throw
Error
```

---

# 29. `try...catch`

```js
try {
  let result = x + 5;
} catch (error) {
  console.log("Error:", error.message);
}
```

The `catch` block executes when an exception occurs inside `try`.

---

# 30. `finally`

`finally` executes whether an error occurs or not.

```js
try {
  console.log("Opening...");
  throw new Error("Something went wrong");
} catch (error) {
  console.log(error.message);
} finally {
  console.log("Closing...");
}
```

---

# 31. `throw`

`throw` manually creates an exception.

```js
function divide(a, b) {
  if (b === 0) {
    throw new Error("Cannot divide by zero");
  }

  return a / b;
}

try {
  console.log(divide(10, 0));
} catch (error) {
  console.log(error.message);
}
```

---

# 32. Custom Errors

Custom error classes can provide meaningful error types.

```js
class ValidationError extends Error {
  constructor(message) {
    super(message);
    this.name = "ValidationError";
  }
}

function registerUser(age) {
  if (age < 18) {
    throw new ValidationError("User must be 18+");
  }

  return "User registered";
}

try {
  registerUser(15);
} catch (error) {
  console.log(error.name);
  console.log(error.message);
}
```

---

# 33. Types of JavaScript Errors

### Syntax Error

Invalid JavaScript syntax.

```js
if (true {
  console.log("Hello");
}
```

---

### Runtime Error

Occurs while the program is running.

```js
console.log(a);
```

---

### Logical Error

Program runs but produces incorrect results.

```js
function multiply(a, b) {
  return a + b;
}
```

The code runs, but the logic is incorrect.

---

# 34. Error Object

Common properties:

```js
error.name;
error.message;
error.stack;
```

Example:

```js
try {
  const obj = undefined;

  obj.name;
} catch (error) {
  console.log(error.name);
  console.log(error.message);
  console.log(error.stack);
}
```

---

# 35. Debouncing

Debouncing delays function execution until the user stops triggering an event for a specific period.

### Simple Definition

> Run the function only after the last event.

### Implementation

```js
function debounce(fn, delay) {
  let timer;

  return function (...args) {
    clearTimeout(timer);

    timer = setTimeout(() => {
      fn.apply(this, args);
    }, delay);
  };
}
```

### Example

```js
function fetchResults(query) {
  console.log("API Request:", query);
}

const debouncedSearch = debounce(fetchResults, 500);

searchInput.addEventListener("input", (e) => {
  debouncedSearch(e.target.value);
});
```

### Common Uses

- Search inputs
- Form validation
- API requests
- Resize events
- Filters

---

# 36. Throttling

Throttling limits a function to execute at most once during a specified time interval.

### Simple Definition

> Run the function at fixed intervals.

### Implementation

```js
function throttle(fn, limit) {
  let lastCall = 0;

  return function (...args) {
    const now = Date.now();

    if (now - lastCall >= limit) {
      lastCall = now;

      fn.apply(this, args);
    }
  };
}
```

### Example

```js
function handleScroll() {
  console.log(window.scrollY);
}

window.addEventListener("scroll", throttle(handleScroll, 200));
```

### Common Uses

- Scroll events
- Mouse movement
- Dragging
- Resize events
- Rapid button clicks

---

# 37. Debouncing vs Throttling

| Debouncing                | Throttling                          |
| ------------------------- | ----------------------------------- |
| Waits until events stop   | Runs at controlled intervals        |
| Executes after inactivity | Executes during continuous activity |
| Good for search           | Good for scrolling                  |
| Reduces API calls         | Controls continuous events          |

### Easy Memory Trick

```text
Debounce → "Wait until user stops"

Throttle → "Run at a controlled rate"
```

---

# 38. Built-in JavaScript Functions & Methods

---

## `split()`

Converts a string into an array.

```js
const str = "apple,banana,grapes";

const result = str.split(",");

console.log(result);
```

Output:

```js
["apple", "banana", "grapes"];
```

### Example

```js
const sentence = "I love JavaScript";

console.log(sentence.split(" "));
```

Output:

```js
["I", "love", "JavaScript"];
```

---

# 39. `join()`

Converts an array into a string.

```js
const arr = ["Hello", "World"];

console.log(arr.join(" "));
```

Output:

```text
Hello World
```

### Example

```js
const digits = [1, 2, 3, 4];

console.log(digits.join(""));
```

Output:

```text
1234
```

---

# 40. `Math.random()`

Generates a random number from:

```text
0 inclusive → 1 exclusive
```

```js
console.log(Math.random());
```

---

# 41. `Math.floor()`

Rounds a number down to the nearest integer.

```js
console.log(Math.floor(4.9)); // 4
console.log(Math.floor(4.1)); // 4
```

---

# 42. Random Number Between Min and Max

Combining `Math.random()` and `Math.floor()`:

```js
function getRandom(min, max) {
  return Math.floor(Math.random() * (max - min + 1)) + min;
}

console.log(getRandom(5, 15));
```

---

# 43. `JSON.stringify()`

Converts a JavaScript value into a JSON string.

```js
const user = {
  name: "Anubhav",
  age: 24,
};

const json = JSON.stringify(user);

console.log(json);
```

Output:

```json
{ "name": "Anubhav", "age": 24 }
```

### Common Uses

- LocalStorage
- Sending data to APIs
- Converting objects into strings
- Data serialization

---

# 44. `JSON.parse()`

Converts a JSON string back into a JavaScript value.

```js
const json = '{"name":"Anubhav","age":24}';

const user = JSON.parse(json);

console.log(user.name);
```

---

# 45. `JSON.stringify()` vs `JSON.parse()`

| Method             | Conversion               |
| ------------------ | ------------------------ |
| `JSON.stringify()` | JavaScript → JSON string |
| `JSON.parse()`     | JSON string → JavaScript |

### Easy Memory Trick

```text
stringify → make a string

parse → read a string back into JS
```

---

# 46. LocalStorage + JSON

LocalStorage stores values as strings.

Therefore, objects need `JSON.stringify()` before storing.

```js
const data = {
  score: 100,
};

localStorage.setItem("game", JSON.stringify(data));
```

Retrieve it:

```js
const game = JSON.parse(localStorage.getItem("game"));

console.log(game.score);
```

---

# 47. Sending JSON to an API

```js
fetch("/api", {
  method: "POST",

  headers: {
    "Content-Type": "application/json",
  },

  body: JSON.stringify({
    id: 1,
    title: "Hello",
  }),
});
```

---

# 48. Important Built-in Functions / APIs Covered

```text
document.getElementById()
document.getElementsByClassName()
document.getElementsByTagName()
document.querySelector()
document.querySelectorAll()

document.createElement()
appendChild()

setTimeout()
clearTimeout()

setInterval()
clearInterval()

Math.random()
Math.floor()

split()
join()

JSON.stringify()
JSON.parse()

fetch()

Promise
Promise.all()

call()
apply()
bind()
```

---

# 49. Advanced JavaScript Learning Flow

```text
Objects
   ↓
OOP
   ↓
Classes
   ↓
Constructors
   ↓
Prototypes
   ↓
Inheritance
   ↓
this
   ↓
call / apply / bind
   ↓
Synchronous JavaScript
   ↓
Asynchronous JavaScript
   ↓
Callbacks
   ↓
Callback Hell
   ↓
Promises
   ↓
async / await
   ↓
fetch()
   ↓
Error Handling
   ↓
Debouncing
   ↓
Throttling
   ↓
JSON
   ↓
Real-world API Projects
```
