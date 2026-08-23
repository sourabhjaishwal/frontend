# CSS

> **Purpose:** These notes cover the main CSS concepts.

## 1. CSS

### Definition

**CSS (Cascading Style Sheets)** is used to control the appearance and layout of HTML elements.

### Example

HTML creates a button; CSS controls its **color, size, spacing, and position**.

```text
HTML → Structure
CSS  → Design & Layout
```

### Key Points

- Styles HTML elements.
- Controls colors, fonts, and spacing.
- Creates layouts and responsive designs.
- Separates design from content.

---

## 2. Types of CSS

### Definition

CSS can be added to HTML using **inline, internal, or external CSS**.

### Example

```html
<!-- Inline -->
<h1 style="color: red;">Hello</h1>

<!-- Internal -->
<style>
  h1 {
    color: blue;
  }
</style>

<!-- External -->
<link rel="stylesheet" href="style.css" />
```

### Key Points

- **Inline:** Written directly inside an element.
- **Internal:** Written inside `<style>`.
- **External:** Written in a separate `.css` file.
- External CSS is preferred for larger projects.

---

## 3. CSS Syntax

### Definition

A CSS rule consists of a **selector** and one or more **property-value declarations**.

### Example

```css
h1 {
  color: blue;
  font-size: 2rem;
}
```

### Visual

```text
h1          → Selector
color       → Property
blue        → Value
```

### Key Points

- Selectors choose elements.
- Properties define what to change.
- Values define how it should look.
- Multiple declarations can exist inside `{}`.

---

## 4. CSS Selectors

### Definition

A **CSS selector** targets HTML elements so styles can be applied to them.

### Example

```css
p {
  color: blue;
} /* Element */
.title {
  color: red;
} /* Class */
#header {
  color: green;
} /* ID */
```

### Key Points

- Element selector targets tags.
- Class selector uses `.`.
- ID selector uses `#`.
- Selectors can target specific elements or groups.

---

## 5. Class vs ID

### Definition

A **class** can be reused on multiple elements, while an **ID** should uniquely identify one element within a document.

### Example

```html
<div class="card"></div>
<div class="card"></div>

<header id="main-header"></header>
```

### Key Points

- Classes are reusable.
- IDs should be unique per document.
- Classes are commonly used for styling.
- IDs can also be useful for anchors and scripting.

---

## 6. CSS Cascade & Specificity

### Definition

The **cascade** decides which CSS rule wins when multiple rules target the same element.

### Example

```css
p {
  color: blue;
}

.text {
  color: red;
}
```

An element with `class="text"` will usually become red because a class selector is more specific.

### Key Points

- More specific rules usually win.
- Later rules can override earlier rules when specificity is equal.
- Inline styles have high priority.
- Avoid excessive use of `!important`.

---

## 7. CSS Units

### Definition

CSS units define the size or measurement of elements and properties.

### Example

```css
.box {
  width: 300px;
  font-size: 2rem;
  width: 80%;
}
```

### Key Points

- `px` → fixed pixel unit.
- `%` → relative to another value, often the parent.
- `rem` → relative to the root font size.
- `vw` and `vh` → relative to viewport dimensions.

---

## 8. The CSS Box Model

### Definition

Every HTML element is treated as a rectangular box consisting of **content, padding, border, and margin**.

### Visual

```text
+---------------------------+
|          Margin           |
|  +---------------------+  |
|  |       Border        |  |
|  |  +---------------+  |  |
|  |  |    Padding    |  |  |
|  |  |  +---------+  |  |  |
|  |  |  | Content |  |  |  |
|  |  |  +---------+  |  |  |
|  |  +---------------+  |  |
|  +---------------------+  |
+---------------------------+
```

### Key Points

- **Content** holds text or media.
- **Padding** adds inner spacing.
- **Border** surrounds padding and content.
- **Margin** adds outer spacing.

---

## 9. `box-sizing`

### Definition

`box-sizing` controls how an element's total width and height are calculated.

### Example

```css
* {
  box-sizing: border-box;
}
```

### Key Points

- `content-box` is the default model.
- `border-box` includes padding and border within the declared size.
- Makes layouts easier to calculate.
- Commonly applied globally.

---

## 10. Margin

### Definition

**Margin** creates space outside an element.

### Example

```css
.card {
  margin: 20px;
}
```

### Key Points

- Creates external spacing.
- Can be applied to individual sides.
- `margin: auto` can help center block elements.
- Useful for separating elements.

---

## 11. Padding

### Definition

**Padding** creates space between an element's content and its border.

### Example

```css
button {
  padding: 10px 20px;
}
```

### Key Points

- Creates internal spacing.
- Increases the clickable area of buttons.
- Can be set individually for each side.
- Affects element size depending on `box-sizing`.

---

## 12. Border & Border Radius

### Definition

A **border** surrounds an element, while `border-radius` creates rounded corners.

### Example

```css
.card {
  border: 1px solid black;
  border-radius: 10px;
}
```

### Key Points

- Borders can be solid, dashed, or dotted.
- `border-radius` rounds corners.
- `50%` can create a circle for a square element.
- Commonly used for cards, buttons, and images.

---

# Backgrounds

## 13. `background-color`

### Definition

`background-color` sets the background color of an element.

### Example

```css
section {
  background-color: lightblue;
}
```

### Key Points

- Supports named colors and color values.
- Commonly used for sections and components.
- Can improve visual hierarchy.
- Works with other background properties.

---

## 14. CSS Gradients

### Definition

A **CSS gradient** creates a smooth transition between two or more colors.

### Example

```css
background: linear-gradient(to right, red, blue);
```

### Key Points

- `linear-gradient()` creates a directional gradient.
- `radial-gradient()` spreads from a center point.
- `conic-gradient()` rotates colors around a center.
- Useful for backgrounds and visual effects.

---

## 15. Background Image

### Definition

`background-image` places an image behind an element's content.

### Example

```css
.hero {
  background-image: url("hero.jpg");
  background-size: cover;
  background-position: center;
}
```

### Key Points

- Commonly used for hero sections.
- `cover` fills the container.
- `contain` keeps the complete image visible.
- `background-position` controls placement.

---

## 16. `background-repeat`

### Definition

`background-repeat` controls whether and how a background image repeats.

### Example

```css
background-repeat: no-repeat;
```

### Key Points

- `repeat` is the default.
- `repeat-x` repeats horizontally.
- `repeat-y` repeats vertically.
- `no-repeat` displays the image once.

---

# Display & Positioning

## 17. `display`

### Definition

The `display` property controls how an element behaves and occupies space in a layout.

### Example

```css
.block {
  display: block;
}
.inline {
  display: inline;
}
.flex {
  display: flex;
}
.grid {
  display: grid;
}
```

### Key Points

- `block` starts on a new line.
- `inline` takes only the required content width.
- `inline-block` stays inline but allows sizing.
- `flex` and `grid` create layout containers.

---

## 18. CSS Positioning

### Definition

The `position` property controls how an element is placed and positioned on a webpage.

### Visual

```text
static   → Normal document flow
relative → Moves from original position
absolute → Positioned relative to an ancestor
fixed    → Positioned relative to viewport
sticky   → Scrolls, then sticks
```

### Key Points

- `static` is the default.
- `relative` keeps its original space.
- `absolute` is useful for overlays and badges.
- `fixed` and `sticky` are useful for persistent UI.

---

## 19. `position: relative`

### Definition

`relative` positions an element relative to its normal position.

### Example

```css
.box {
  position: relative;
  top: 20px;
  left: 30px;
}
```

### Key Points

- Keeps its original space in the layout.
- Can be moved using `top`, `left`, etc.
- Often acts as a reference for absolute children.
- Useful for small position adjustments.

---

## 20. `position: absolute`

### Definition

`absolute` removes an element from normal flow and positions it relative to its nearest positioned ancestor.

### Example

```css
.parent {
  position: relative;
}

.badge {
  position: absolute;
  top: 0;
  right: 0;
}
```

### Key Points

- Does not reserve normal layout space.
- Uses a positioned ancestor as reference.
- Useful for badges and overlays.
- If no suitable ancestor exists, positioning may use the initial containing block.

---

## 21. `position: fixed`

### Definition

`fixed` positions an element relative to the viewport so it stays in place while scrolling.

### Example

```css
.chat-button {
  position: fixed;
  bottom: 20px;
  right: 20px;
}
```

### Key Points

- Stays visible while scrolling.
- Positioned relative to the viewport.
- Useful for chat buttons.
- Commonly used for persistent controls.

---

## 22. `position: sticky`

### Definition

`sticky` behaves normally until a scroll threshold is reached, then sticks within its scroll container.

### Example

```css
header {
  position: sticky;
  top: 0;
}
```

### Key Points

- Combines relative and fixed-like behavior.
- Requires an offset such as `top`.
- Useful for headers and sidebars.
- Its behavior depends on the scroll container and ancestors.

---

# Flexbox

## 23. Flexbox

### Definition

**Flexbox** is a one-dimensional layout system used to arrange items in a row or column.

### Example

```css
.container {
  display: flex;
}
```

### Visual

```text
[ Item 1 ] [ Item 2 ] [ Item 3 ]
```

### Key Points

- Arranges items along one main axis.
- Excellent for alignment.
- Supports rows and columns.
- Useful for responsive layouts.

---

## 24. `flex-direction`

### Definition

`flex-direction` defines the direction in which flex items are placed.

### Example

```css
.container {
  display: flex;
  flex-direction: column;
}
```

### Key Points

- `row` is the default.
- `column` stacks items vertically.
- `row-reverse` reverses horizontal order.
- `column-reverse` reverses vertical order.

---

## 25. `justify-content`

### Definition

`justify-content` aligns flex items along the **main axis**.

### Example

```css
.container {
  display: flex;
  justify-content: space-between;
}
```

### Key Points

- `flex-start` places items at the start.
- `center` centers items.
- `space-between` distributes space between items.
- The direction depends on `flex-direction`.

---

## 26. `align-items`

### Definition

`align-items` aligns flex items along the **cross axis**.

### Example

```css
.container {
  display: flex;
  align-items: center;
}
```

### Key Points

- `flex-start` aligns to the start.
- `center` centers items.
- `flex-end` aligns to the end.
- `stretch` is commonly the default behavior.

---

## 27. `gap`

### Definition

`gap` adds consistent space between Flexbox or Grid items.

### Example

```css
.container {
  display: flex;
  gap: 20px;
}
```

### Key Points

- Creates space between items.
- Avoids adding margins to every item.
- Works with Flexbox and Grid.
- Makes layouts easier to maintain.

---

## 28. `flex-wrap`

### Definition

`flex-wrap` controls whether flex items stay on one line or move onto multiple lines.

### Example

```css
.container {
  display: flex;
  flex-wrap: wrap;
}
```

### Key Points

- `nowrap` keeps items on one line.
- `wrap` moves overflowing items to the next line.
- Useful for responsive card layouts.
- Prevents excessive horizontal overflow in suitable layouts.

---

## 29. `flex-shrink`

### Definition

`flex-shrink` controls how much a flex item can shrink when there is not enough available space.

### Example

```css
.logo {
  flex-shrink: 0;
}
```

### Key Points

- Default value is typically `1`.
- Higher values allow more shrinking relative to siblings.
- `0` prevents shrinking.
- Useful for logos and fixed-size items.

---

# CSS Grid

## 30. CSS Grid

### Definition

**CSS Grid** is a two-dimensional layout system used to arrange elements in rows and columns.

### Example

```css
.container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 20px;
}
```

### Visual

```text
+-------+-------+-------+
|   1   |   2   |   3   |
+-------+-------+-------+
|   4   |   5   |   6   |
+-------+-------+-------+
```

### Key Points

- Works with rows and columns.
- Useful for complex layouts.
- Supports responsive grids.
- `fr` divides available space into fractions.

---

## 31. `grid-template-columns`

### Definition

`grid-template-columns` defines the number and size of grid columns.

### Example

```css
grid-template-columns: repeat(3, 1fr);
```

### Key Points

- Defines column structure.
- `1fr` represents one fraction of available space.
- `repeat()` reduces repetition.
- Can mix fixed and flexible sizes.

---

## 32. `minmax()` and Responsive Grid

### Definition

`minmax()` defines a minimum and maximum size for a Grid track.

### Example

```css
grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
```

### Key Points

- Helps create flexible grids.
- Useful for responsive card layouts.
- Prevents columns from becoming too small.
- Can reduce the need for media queries.

---

## 33. Grid Template Areas

### Definition

`grid-template-areas` allows you to create layouts using named visual regions.

### Example

```css
.container {
  display: grid;
  grid-template-areas:
    "header header"
    "sidebar main"
    "footer footer";
}
```

### Visual

```text
+-------------------+
|      HEADER       |
+---------+---------+
| SIDEBAR |  MAIN   |
+---------+---------+
|      FOOTER       |
+-------------------+
```

### Key Points

- Makes layouts easier to visualize.
- Uses named areas.
- Great for page-level layouts.
- Can be changed easily at different screen sizes.

---

# Transform & Effects

## 34. `transform`

### Definition

`transform` visually moves, rotates, scales, or skews an element without changing its normal document layout.

### Example

```css
.card {
  transform: scale(1.05);
}
```

### Key Points

- `translate()` moves elements.
- `scale()` changes size.
- `rotate()` rotates elements.
- `skew()` tilts elements.

---

## 35. `translate()`

### Definition

`translate()` moves an element along the X and/or Y axis.

### Example

```css
.box {
  transform: translate(50px, 20px);
}
```

### Key Points

- `translateX()` moves horizontally.
- `translateY()` moves vertically.
- Negative values move in the opposite direction.
- Useful for animations and visual positioning.

---

## 36. `scale()`, `rotate()` & `skew()`

### Definition

These transform functions resize, rotate, or tilt an element.

### Example

```css
.box {
  transform: scale(1.1) rotate(5deg);
}
```

### Key Points

- `scale()` changes visual size.
- `rotate()` rotates an element.
- `skew()` tilts an element.
- Multiple transforms can be combined.

---

## 37. `:hover`

### Definition

`:hover` is a pseudo-class that applies styles when a pointing device hovers over an element.

### Example

```css
button:hover {
  transform: scale(1.05);
}
```

### Key Points

- Adds visual feedback.
- Commonly used for buttons and links.
- Can change color, size, or other properties.
- Should not be the only way important functionality is accessible.

---

## 38. `transition`

### Definition

`transition` creates a smooth change between CSS property values.

### Example

```css
button {
  transition: background-color 0.3s ease;
}
```

### Key Points

- Controls how property changes animate.
- `duration` controls the animation time.
- `timing-function` controls the speed curve.
- Commonly combined with `:hover`.

---

## 39. `perspective`

### Definition

`perspective` creates a sense of 3D depth for transformed child elements.

### Example

```css
.scene {
  perspective: 800px;
}
```

### Key Points

- Used with 3D transforms.
- Applied to a parent or through transform functions depending on the effect.
- Smaller values create a stronger perspective effect.
- Useful for card flips and 3D UI effects.

---

# Responsive Design

## 40. Responsive Design

### Definition

**Responsive design** makes a website adapt its layout and content to different screen sizes and devices.

### Example

```text
Mobile → Stacked Layout
Tablet → Flexible Layout
Desktop → Multi-column Layout
```

### Key Points

- Start with a flexible layout.
- Use Flexbox and Grid.
- Use responsive units where appropriate.
- Test across different screen sizes.

---

## 41. Mobile-First Approach

### Definition

**Mobile-first CSS** starts with styles for smaller screens and progressively adds enhancements for larger screens.

### Example

```css
.card {
  font-size: 1rem;
}

@media (min-width: 768px) {
  .card {
    font-size: 1.25rem;
  }
}
```

### Key Points

- Start with the smallest layout.
- Add larger-screen styles using `min-width`.
- Often results in simpler CSS.
- Encourages focused responsive design.

---

## 42. Media Queries

### Definition

**Media queries** apply CSS only when specific conditions, such as viewport width, are met.

### Example

```css
@media (min-width: 768px) {
  .container {
    flex-direction: row;
  }
}
```

### Key Points

- Adapt layouts for different screen sizes.
- Commonly use `min-width` or `max-width`.
- Should support layout needs rather than arbitrary device names.
- Useful alongside Flexbox and Grid.

---

## 43. `clamp()`

### Definition

`clamp()` creates a responsive value with a defined minimum and maximum.

### Example

```css
font-size: clamp(1rem, 3vw, 3rem);
```

### Key Points

- First value is the minimum.
- Middle value is the preferred fluid value.
- Last value is the maximum.
- Useful for responsive typography.

---

## 44. CSS Variables

### Definition

**CSS variables**, also called custom properties, store reusable CSS values.

### Example

```css
:root {
  --primary-color: blue;
  --spacing: 20px;
}

button {
  background: var(--primary-color);
}
```

### Key Points

- Start with `--`.
- Access values using `var()`.
- Improve consistency.
- Make global changes easier.

---

## 45. Wrapper / Container

### Definition

A **wrapper** limits and centers content so it does not stretch excessively on large screens.

### Example

```css
.wrapper {
  max-width: 1200px;
  margin: 0 auto;
}
```

### Key Points

- Limits content width.
- Centers content horizontally.
- Improves readability on large screens.
- Commonly used inside full-width sections.

---

# Other Useful CSS Concepts

## 46. `background-clip`

### Definition

`background-clip` controls how far an element's background extends.

### Example

```css
.text {
  background: linear-gradient(red, blue);
  background-clip: text;
  color: transparent;
}
```

### Key Points

- Can clip to `border-box`.
- Can clip to `padding-box`.
- Can clip to `content-box`.
- `text` can be used for gradient text with appropriate browser support.

---

## 47. Text Stroke

### Definition

`-webkit-text-stroke` adds an outline around text.

### Example

```css
h1 {
  -webkit-text-stroke: 1px black;
}
```

### Key Points

- Creates outlined text.
- Uses a WebKit-prefixed property.
- Useful for visual effects.
- Browser support should be considered.

---

## 48. CSS Boilerplate

### Definition

A **CSS boilerplate** contains common starting styles that create a more predictable styling base.

### Example

```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html,
body {
  width: 100%;
  min-height: 100%;
}
```

### Key Points

- Removes unwanted default spacing.
- Uses consistent box sizing.
- Provides a clean starting point.
- Can be customized based on the project.

---

# SCSS

## 49. SCSS

### Definition

**SCSS** is a CSS syntax that adds features such as nesting, variables, and mixins, then compiles into regular CSS.

### Example

```scss
$primary: blue;

button {
  background: $primary;
}
```

### Key Points

- Makes large stylesheets easier to organize.
- Supports variables and mixins.
- Supports nested syntax.
- Must be processed into CSS for browsers.

---

## 50. SCSS Nesting

### Definition

**Nesting** allows related selectors to be written inside each other in SCSS.

### Example

```scss
nav {
  ul {
    list-style: none;
  }
}
```

### Key Points

- Can improve readability when used carefully.
- Reflects relationships between selectors.
- Excessive nesting can create overly specific CSS.
- Use shallow nesting for maintainability.

---

## 51. SCSS Partials & Imports

### Definition

**Partials** split SCSS into smaller reusable files that can be combined during compilation.

### Example

```text
_header.scss
_footer.scss
_variables.scss
```

### Key Points

- Helps organize large projects.
- Partials commonly begin with `_`.
- Modern Sass generally recommends `@use` and `@forward` instead of legacy `@import`.
- Compiled output becomes regular CSS.

---

## 52. SCSS Mixins

### Definition

A **mixin** is a reusable block of SCSS that can be included in multiple selectors.

### Example

```scss
@mixin flex-center {
  display: flex;
  justify-content: center;
  align-items: center;
}

.container {
  @include flex-center;
}
```

---

# CSS Quick Workflow

```text
HTML
  ↓
CSS Selectors
  ↓
Colors + Typography
  ↓
Box Model
  ↓
Layout
 ├── Flexbox
 └── Grid
  ↓
Responsive Design
 ├── Fluid Units
 ├── clamp()
 └── Media Queries
  ↓
Effects
 ├── Transform
 ├── Transition
 └── Hover
```

---

### Key Points

- Reduces repeated code.
- Can accept arguments.
- Useful for reusable patterns.
- Should be used when reuse provides real value.
