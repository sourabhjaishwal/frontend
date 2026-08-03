# HTML

## 1. HTML

### Definition

**HTML (HyperText Markup Language)** is the standard markup language used to structure and give meaning to content on web pages.

### Example

Like the skeleton of a human body, HTML provides the basic structure of a webpage.

### Key Points

- Structures text, images, links, and media.
- Provides meaning to webpage content.
- Helps with accessibility and SEO.
- Works with CSS for styling and JavaScript for behavior.

---

## 2. HTML Boilerplate

### Definition

An **HTML boilerplate** is the standard basic structure used as the starting point for an HTML document.

### Visual

```html
<!DOCTYPE html>
<html>
  <head>
    <!-- Metadata -->
  </head>
  <body>
    <!-- Visible Content -->
  </body>
</html>
```

### Key Points

- `<!DOCTYPE html>` declares HTML5.
- `<head>` contains metadata and resources.
- `<body>` contains visible webpage content.
- `viewport` meta tag helps with responsive layouts.

---

## 3. `<!DOCTYPE html>`

### Definition

`<!DOCTYPE html>` tells the browser that the document uses the HTML5 standard.

### Example

```html
<!DOCTYPE html>
```

### Key Points

- Must appear at the beginning of an HTML document.
- Ensures standards mode in browsers.
- It is a declaration, not an HTML element.

---

## 4. `<html>` Element

### Definition

The `<html>` element is the root element that contains the entire HTML document.

### Example

```html
<html lang="en"></html>
```

### Key Points

- Wraps the complete HTML document.
- Contains `<head>` and `<body>`.
- `lang` specifies the document's language.
- Helps accessibility and search engines.

---

## 5. `<head>` Element

### Definition

The `<head>` contains metadata and resources that provide information about the webpage but are generally not displayed as page content.

### Example

```html
<head>
  <meta charset="UTF-8" />
  <title>My Website</title>
</head>
```

### Key Points

- Contains metadata.
- Defines the page title.
- Can include CSS and other resources.
- Contains SEO-related metadata.

---

## 6. `<body>` Element

### Definition

The `<body>` contains the visible and interactive content displayed on a webpage.

### Example

```html
<body>
  <h1>Hello World</h1>
  <p>Welcome to my website.</p>
</body>
```

### Key Points

- Contains visible webpage content.
- Includes text, images, links, forms, and media.
- Usually contains the main page structure.
- Comes after the `<head>`.

---

## 7. Meta Charset

### Definition

`<meta charset="UTF-8">` defines the character encoding used by the webpage.

### Example

```html
<meta charset="UTF-8" />
```

### Key Points

- UTF-8 supports a wide range of characters.
- Supports languages, symbols, and emojis.
- Helps prevent character display issues.
- Commonly placed inside `<head>`.

---

## 8. Viewport Meta Tag

### Definition

The viewport meta tag controls how a webpage is displayed and scaled on different screen sizes.

### Example

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
```

### Key Points

- Important for responsive websites.
- Makes the layout adapt to device width.
- Commonly used in mobile-friendly websites.
- Usually included in the HTML boilerplate.

---

## 9. `<title>`

### Definition

The `<title>` element defines the title of the webpage shown in the browser tab.

### Example

```html
<title>My Portfolio</title>
```

### Key Points

- Appears in the browser tab.
- Helps identify the page.
- Important for SEO.
- Should describe the page clearly.

---

## 10. Headings: `<h1>` to `<h6>`

### Definition

Heading elements define titles and hierarchical sections of webpage content.

### Example

```html
<h1>Main Title</h1>
<h2>Section Title</h2>
<h3>Subsection</h3>
```

### Key Points

- `<h1>` is the highest-level heading.
- `<h6>` is the lowest-level heading.
- Create a logical content hierarchy.
- Important for accessibility and SEO.

---

## 11. Paragraph: `<p>`

### Definition

The `<p>` element represents a paragraph of text.

### Example

```html
<p>HTML is used to structure web pages.</p>
```

### Key Points

- Used for blocks of text.
- Creates meaningful content structure.
- Commonly used for descriptions and information.
- Browsers normally display paragraphs as separate blocks.

---

## 12. Text Formatting

### Definition

HTML provides elements that can add meaning or visual emphasis to text.

### Example

```html
<b>Bold</b>
<i>Italic</i>
<u>Underline</u>
<mark>Highlighted</mark>
```

### Key Points

- `<b>` draws attention to text without implying importance.
- `<i>` represents text in an alternate voice or mood.
- `<u>` represents text with a non-textual annotation.
- `<mark>` highlights relevant text.

---

## 13. Superscript and Subscript

### Definition

`<sup>` displays text above the normal baseline, while `<sub>` displays text below it.

### Example

```html
x<sup>2</sup> H<sub>2</sub>O
```

### Key Points

- `<sup>` is used for exponents and superscript text.
- `<sub>` is used for chemical formulas and subscripts.
- Useful for mathematical and scientific content.
- They change the text's visual position.

---

## 14. Lorem Ipsum

### Definition

**Lorem Ipsum** is placeholder text used during design and development before real content is available.

### Example

```text
Lorem ipsum dolor sit amet...
```

### Key Points

- Used as temporary content.
- Helps test layouts and typography.
- Should be replaced with real content.
- Common during UI development.

---

## 15. Ordered List: `<ol>`

### Definition

An **ordered list** displays items in a specific sequence, usually using numbers.

### Example

```html
<ol>
  <li>Open the browser</li>
  <li>Enter the URL</li>
  <li>Visit the website</li>
</ol>
```

### Key Points

- Uses `<ol>` as the container.
- Uses `<li>` for list items.
- Items are usually numbered.
- Useful for steps and instructions.

---

## 16. Unordered List: `<ul>`

### Definition

An **unordered list** displays items without a required sequence, usually using bullet points.

### Example

```html
<ul>
  <li>HTML</li>
  <li>CSS</li>
  <li>JavaScript</li>
</ul>
```

### Key Points

- Uses `<ul>` as the container.
- Uses `<li>` for list items.
- Items are usually displayed with bullets.
- Useful for features and general lists.

---

## 17. Anchor: `<a>`

### Definition

The `<a>` element creates hyperlinks that allow users to navigate to another page, location, or resource.

### Example

```html
<a href="https://example.com">Visit Website</a>
```

### Key Points

- `href` specifies the destination.
- Can link to pages, files, sections, or URLs.
- `target="_blank"` opens a link in a new browsing context.
- Essential for website navigation.

---

## 18. Image: `<img>`

### Definition

The `<img>` element embeds an image into a webpage.

### Example

```html
<img src="profile.jpg" alt="Profile photo" />
```

### Key Points

- `src` specifies the image source.
- `alt` provides alternative text.
- `alt` improves accessibility and helps when images cannot load.
- `width` and `height` can help reserve layout space.

---

## 19. `alt` Attribute

### Definition

The `alt` attribute provides alternative text that describes an image.

### Example

```html
<img src="cat.jpg" alt="A white cat sitting on a chair" />
```

### Key Points

- Important for screen reader users.
- Displayed when an image cannot load.
- Should describe meaningful images accurately.
- Decorative images can use an empty `alt=""`.

---

## 20. `<br>` and `<hr>`

### Definition

`<br>` creates a line break, while `<hr>` represents a thematic break between sections of content.

### Example

```html
<p>Hello<br />World</p>
<hr />
```

### Key Points

- `<br>` moves content to a new line.
- `<hr>` represents a thematic separation.
- Both are void elements.
- Avoid using `<br>` repeatedly for layout spacing; use CSS instead.

---

## 21. HTML Comments

### Definition

HTML comments are notes in the code that browsers do not display as webpage content.

### Example

```html
<!-- This is a navigation section -->
```

### Key Points

- Written using `<!-- -->`.
- Useful for explaining code.
- Can help organize HTML.
- Comments are visible in the page source/dev tools, so don't store secrets in them.

---

## 22. Void Elements

### Definition

**Void elements** are HTML elements that do not contain content and do not require a closing tag.

### Example

```html
<img src="image.jpg" alt="Example" />
<br />
<hr />
```

### Key Points

- Do not have closing tags.
- Cannot contain child elements.
- Common examples: `<img>`, `<br>`, `<hr>`, `<meta>`, `<link>`.
- Often incorrectly called "self-closing tags" in HTML.

---

# HTML Semantics

## 23. Semantic HTML

### Definition

**Semantic HTML** means using HTML elements that clearly describe the meaning and purpose of their content.

### Example

```html
<header>Website Header</header>
<nav>Navigation</nav>
<main>Main Content</main>
<footer>Footer</footer>
```

### Key Points

- Improves accessibility.
- Helps search engines understand content.
- Makes code easier to read and maintain.
- Prefer meaningful elements over unnecessary `<div>` elements.

---

## 24. `<header>`

### Definition

The `<header>` element represents introductory content for a page or section.

### Example

```html
<header>
  <h1>My Portfolio</h1>
</header>
```

### Key Points

- Can contain headings and introductory content.
- Often contains logos or navigation.
- Can appear at page or section level.
- Does not necessarily mean the entire page header.

---

## 25. `<nav>`

### Definition

The `<nav>` element represents a section containing major navigation links.

### Example

```html
<nav>
  <a href="/">Home</a>
  <a href="/about">About</a>
</nav>
```

### Key Points

- Used for important navigation links.
- Helps screen readers identify navigation.
- Commonly contains links.
- Not every group of links needs `<nav>`.

---

## 26. `<main>`

### Definition

The `<main>` element represents the primary content of a webpage.

### Example

```html
<main>
  <h1>Our Services</h1>
  <p>Explore our services.</p>
</main>
```

### Key Points

- Contains the page's main content.
- Should not contain repeated site-wide content.
- Helps assistive technologies navigate the page.
- Typically used once per page.

---

## 27. `<section>`

### Definition

The `<section>` element groups thematically related content into a meaningful section.

### Example

```html
<section>
  <h2>Our Services</h2>
  <p>We provide web development services.</p>
</section>
```

### Key Points

- Groups related content.
- Usually has a heading.
- Helps organize page structure.
- Useful for distinct sections of a page.

---

## 28. `<article>`

### Definition

The `<article>` element represents a self-contained piece of content that can stand independently.

### Example

A blog post, news article, or forum post can be an `<article>`.

### Key Points

- Represents independent content.
- Can be reused or distributed separately.
- Common in blogs and news websites.
- Can contain its own headings and structure.

---

## 29. `<aside>`

### Definition

The `<aside>` element represents content related to the main content but not part of its primary flow.

### Example

A blog sidebar containing related posts or advertisements.

### Key Points

- Used for secondary content.
- Commonly used for sidebars.
- Can contain related links or additional information.
- Its content should be related to the surrounding content.

---

## 30. `<footer>`

### Definition

The `<footer>` element represents footer information for a page or section.

### Example

```html
<footer>
  <p>&copy; 2026 My Website</p>
</footer>
```

### Key Points

- Often contains copyright information.
- Can include contact information or related links.
- Can belong to a page or individual section.
- Usually appears at the bottom of content.

---

## 31. `<figure>` and `<figcaption>`

### Definition

`<figure>` groups self-contained media or content, while `<figcaption>` provides its caption.

### Example

```html
<figure>
  <img src="mountain.jpg" alt="Mountain landscape" />
  <figcaption>Mountain landscape</figcaption>
</figure>
```

### Key Points

- Used for images, diagrams, charts, or illustrations.
- `<figcaption>` describes the figure.
- Improves semantic structure.
- Figure content can be moved without affecting the main flow.

---

## 32. `<time>`

### Definition

The `<time>` element represents a specific date, time, or duration.

### Example

```html
<time datetime="2026-08-03">August 3, 2026</time>
```

### Key Points

- Represents machine-readable dates or times.
- `datetime` provides a machine-readable value.
- Useful for articles and event information.
- Helps browsers and other tools interpret dates.

---

## 33. `<address>`

### Definition

The `<address>` element represents contact information related to a person, organization, or webpage.

### Example

```html
<address>Email: hello@example.com</address>
```

### Key Points

- Used for contact information.
- Can contain email or physical address details.
- Often used inside `<footer>`.
- Should represent contact information, not arbitrary postal text.

---

# Semantic HTML Structure

## 34. Semantic Page Layout

### Definition

A semantic page layout uses meaningful HTML elements to organize different parts of a webpage.

### Visual

```text
<body>
│
├── <header>
│     └── Logo / Intro
│
├── <nav>
│     └── Navigation Links
│
├── <main>
│     ├── <section>
│     └── <article>
│
├── <aside>
│     └── Related Content
│
└── <footer>
      └── Contact / Copyright
```

### Key Points

- Gives structure and meaning to content.
- Improves accessibility.
- Helps search engines understand page structure.
- Makes HTML easier to maintain.

---

# 35. `<div>` vs Semantic Elements

### Definition

`<div>` is a generic container, while semantic elements describe the purpose of the content they contain.

### Example

```html
<div class="header">...</div>
```

```html
<header>...</header>
```

### Key Points

- Use `<div>` when no semantic element fits.
- Prefer `<header>`, `<nav>`, `<main>`, etc. when appropriate.
- Semantic HTML improves code readability.
- Semantic elements provide meaningful structure to browsers and assistive technologies.

---

# 36. HTML Accessibility

### Definition

**HTML accessibility** means structuring webpages so that people with different abilities can access and use the content.

### Example

Using `<label>` with form inputs and meaningful `alt` text for images.

### Key Points

- Use semantic HTML.
- Provide meaningful `alt` text for images.
- Associate labels with form controls.
- Ensure interactive content is keyboard accessible.

---

# 37. HTML and SEO

### Definition

HTML supports **SEO (Search Engine Optimization)** by providing search engines with meaningful information and structure about webpage content.

### Example

```html
<title>Web Development Course</title>
<h1>Learn HTML</h1>
```

### Key Points

- Use meaningful page titles.
- Maintain logical heading hierarchy.
- Use semantic HTML.
- Provide descriptive content and image `alt` text where appropriate.

---

# 38. HTML Media Elements

### Definition

HTML provides built-in elements for embedding media such as video and audio directly into webpages.

### Example

```html
<video controls>
  <source src="video.mp4" type="video/mp4" />
</video>
```

### Key Points

- `<video>` embeds video content.
- `<audio>` embeds audio content.
- `controls` provides playback controls.
- Captions using `<track>` improve video accessibility.

---

# 39. `<video>` Attributes

### Definition

Video attributes control how an HTML video behaves and is displayed.

### Example

```html
<video controls muted loop poster="thumbnail.jpg">
  <source src="video.mp4" type="video/mp4" />
</video>
```

### Key Points

- `controls` displays playback controls.
- `muted` starts the video without sound.
- `loop` repeats the video.
- `poster` displays an image before playback.

---

# 40. `<iframe>`

### Definition

An `<iframe>` embeds another HTML document or external content inside the current webpage.

### Example

Embedding a YouTube video or a Google Maps location.

### Key Points

- Embeds external or separate web content.
- `title` helps accessibility.
- `sandbox` can restrict embedded content capabilities.
- Use trusted sources and appropriate security settings.

---

# 41. HTML Forms

### Definition

An HTML **form** collects user input and sends the data for processing.

### Example

```html
<form action="/submit" method="POST">
  <input type="text" name="username" />
  <button type="submit">Submit</button>
</form>
```

### Key Points

- `<form>` groups input controls.
- `action` specifies where data is sent.
- `method` defines how data is submitted.
- `name` identifies form data for processing.

---

# 42. Form Attributes

### Definition

Form attributes control how user input is collected, validated, and submitted.

### Example

```html
<input type="email" name="email" required autocomplete="email" />
```

### Key Points

- `required` makes a field mandatory.
- `pattern` applies a validation pattern.
- `autocomplete` helps browsers fill known information.
- `name` provides the key used when submitting form data.

---

# 43. `<label>`

### Definition

The `<label>` element provides a descriptive label for a form control.

### Example

```html
<label for="email">Email</label> <input id="email" type="email" />
```

### Key Points

- Improves form accessibility.
- Connects to an input using `for` and `id`.
- Helps users understand what to enter.
- Clicking the label can focus or activate the associated control.

---

# 44. `<select>`, `<option>`, and `<optgroup>`

### Definition

These elements create dropdown menus, with `<select>` as the control, `<option>` as choices, and `<optgroup>` for grouping choices.

### Example

```html
<select name="country">
  <optgroup label="Asia">
    <option>India</option>
    <option>Japan</option>
  </optgroup>
</select>
```

### Key Points

- `<select>` creates the dropdown.
- `<option>` defines choices.
- `<optgroup>` groups related options.
- `multiple` allows multiple selections.

---

# 45. HTML Best Practices

### Definition

HTML best practices are guidelines for writing accessible, semantic, maintainable, and efficient HTML.

### Example

Use `<button>` for actions instead of using a clickable `<div>`.

### Key Points

- Prefer semantic HTML.
- Always provide appropriate image `alt` text.
- Use `<label>` with form controls.
- Avoid unnecessary `<div>` elements and oversized unoptimized images.
