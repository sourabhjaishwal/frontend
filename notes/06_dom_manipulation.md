# DOM (Document Object Model)

> **Purpose:** Quick revision of DOM manipulation.

## DOM Introduction

### 1. What is the DOM?

The **DOM (Document Object Model)** is a structured representation of an HTML document.

JavaScript uses the DOM to:

- Select HTML elements
- Change HTML content
- Change CSS
- Create new elements
- Add/remove elements
- Handle user interactions
- Add event listeners

---

## 2. Selecting Elements

### `getElementById()`

Selects an element using its `id`.

```js
const title = document.getElementById("heading");
```

---

### `getElementsByClassName()`

Selects elements using a class name.

Returns an **HTMLCollection**.

```js
const boxes = document.getElementsByClassName("box");
```

---

### `getElementsByTagName()`

Selects elements using their tag name.

```js
const allDivs = document.getElementsByTagName("div");
```

---

### `querySelector()`

Selects the **first matching element**.

Uses CSS selectors.

```js
const firstPara = document.querySelector("p");

const heading = document.querySelector("#heading");

const box = document.querySelector(".box");
```

---

### `querySelectorAll()`

Selects **all matching elements**.

Returns a **NodeList**.

```js
const allParas = document.querySelectorAll("p");
```

Can be used with `forEach()`:

```js
allParas.forEach((para) => {
  console.log(para);
});
```

### Key Point

For modern JavaScript, `querySelector()` and `querySelectorAll()` are commonly preferred because they support CSS selectors.

---

# 3. Changing HTML Content

## `innerText`

Changes or reads visible text.

```js
msg.innerText = "Hello World";
```

---

## `textContent`

Gets or sets the text content of an element.

```js
msg.textContent = "Hello World";
```

Unlike `innerText`, it can include text that is hidden through CSS.

It does **not parse HTML**.

```js
const p = document.createElement("p");

p.textContent = "<b>Hello</b>";
```

Output:

```text
<b>Hello</b>
```

---

## `innerHTML`

Gets or sets HTML content.

```js
msg.innerHTML = "<b>Hello World</b>";
```

The browser interprets the HTML.

### Important

Use `innerHTML` carefully when working with user-generated content because inserting untrusted HTML can create security problems such as XSS.

---

# 4. Changing CSS with JavaScript

JavaScript can directly modify an element's inline styles using `.style`.

```js
const btn = document.getElementById("btn");

btn.style.backgroundColor = "black";
btn.style.color = "white";
btn.style.padding = "10px";
```

### Key Point

For larger styling changes, it is usually better to add/remove CSS classes instead of modifying many individual `.style` properties.

---

# 5. Creating Elements

## `document.createElement()`

Creates a new HTML element dynamically.

### Syntax

```js
document.createElement("tagName");
```

### Example

```js
const div = document.createElement("div");

console.log(div);
```

Output:

```html
<div></div>
```

### Common Uses

- Dynamic cards
- Lists
- Modals
- Notifications
- Todo items
- Dynamic UI components

---

# 6. `appendChild()`

Adds a node to the end of a parent element.

### Syntax

```js
parent.appendChild(child);
```

### Example

```js
const ul = document.createElement("ul");
const li = document.createElement("li");

li.textContent = "Item 1";

ul.appendChild(li);

document.body.appendChild(ul);
```

### Important Points

- Accepts a Node
- Adds the child at the end
- Can move an existing element
- Returns the appended node

---

# 7. Creating Dynamic Elements

`createElement()`, `textContent`, and `appendChild()` can be combined.

```js
const list = document.createElement("ul");

for (let i = 1; i <= 3; i++) {
  const li = document.createElement("li");

  li.textContent = "Item " + i;

  list.appendChild(li);
}

document.body.appendChild(list);
```

---

# 8. Event Listeners

An event listener waits for an event and executes a callback function when that event occurs.

### Syntax

```js
element.addEventListener("eventName", callbackFunction);
```

### Example

```js
const button = document.getElementById("clickMe");

button.addEventListener("click", function () {
  console.log("Button clicked");
});
```

---

# 9. Common Mouse Events

### `click`

```js
button.addEventListener("click", () => {
  console.log("Clicked");
});
```

Triggered when an element is clicked.

---

### `dblclick`

```js
box.addEventListener("dblclick", () => {
  console.log("Double clicked");
});
```

Triggered on double click.

---

### `mousedown`

```js
box.addEventListener("mousedown", () => {
  console.log("Mouse button pressed");
});
```

Triggered when the mouse button is pressed.

---

### `mouseup`

```js
box.addEventListener("mouseup", () => {
  console.log("Mouse button released");
});
```

Triggered when the mouse button is released.

---

### `mouseenter`

Triggered when the pointer enters an element.

```js
box.addEventListener("mouseenter", () => {
  box.style.background = "blue";
});
```

`mouseenter` does not bubble.

---

### `mouseleave`

Triggered when the pointer leaves an element.

```js
box.addEventListener("mouseleave", () => {
  box.style.background = "red";
});
```

---

### `mouseover`

Triggered when the pointer moves over an element or its children.

```js
box.addEventListener("mouseover", () => {
  console.log("Mouse over");
});
```

`mouseover` bubbles.

---

### `mousemove`

Triggered whenever the mouse moves.

```js
document.addEventListener("mousemove", (e) => {
  console.log(e.clientX, e.clientY);
});
```

---

# 10. Keyboard Events

## `keydown`

Triggered when a key is pressed.

```js
document.addEventListener("keydown", (e) => {
  console.log(e.key);
});
```

---

## `keyup`

Triggered when a key is released.

```js
document.addEventListener("keyup", (e) => {
  console.log("Key released:", e.key);
});
```

---

# 11. Other Common Events

```text
click
dblclick
mousedown
mouseup
mouseenter
mouseleave
mouseover
mousemove
keydown
keyup
submit
change
```

---

# 12. DOM Practice — Counter

Create a counter with:

- Increase button
- Decrease button
- Reset button
- Counter value displayed on screen

Concepts used:

```text
DOM Selection
Event Listeners
Changing text
JavaScript variables
```

---
