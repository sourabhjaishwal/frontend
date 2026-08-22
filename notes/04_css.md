Day - 8
Sheryians
Coding School
HTML Notes
Day - 10
Sheryians
Coding School
 CSS Basics Notes
S H E R Y I A N S C O D I N G S C H O O L
 What is CSS?
Why Do We Use CSS?
 HTML = resume content, CSS = fonts, colors, layout.
 Example:
 Inline CSS
 Internal CSS
 CSS Basics Notes
CSS (Cascading Style Sheets) → Styles HTML pages.

Cascading → order of rules decides priority.

Style Sheets → rules applied to many pages.
Make websites beautiful
Control layout
Save time (one CSS file → many pages)

Responsive design
Better user experience
 3. Types of CSS
S H E R Y I A N S C O D I N G S C H O O L
 CSS Basics Notes
rel="stylesheet" → tells browser

href → file path
Linking External CSS
 CSS Syntax
 External CSS
 Best for large projects
S H E R Y I A N S C O D I N G S C H O O L
 CSS Basics Notes
Selecting Elements
Universal → * { margin: 0; padding: 0; }

Tag → h1 { color: blue; }

Class → .highlight { color: green; }

ID → #special { color: red; }
 Text & Color Properties
Example:
 Use class (reusable), ID (unique).
S H E R Y I A N S C O D I N G S C H O O L
 CSS Basics Notes
Fonts
Google Fonts
@font-face (local font)
 ID vs Class
S H E R Y I A N S C O D I N G S C H O O L
 CSS Basics Notes
 Div in CSS
 Div = empty container. CSS gives it shape & style.


Day - 11
Sheryians
Coding School
CSS Notes: 

Div, Backgrounds, and Box Model
S H E R Y I A N S C O D I N G S C H O O L
 What is <div> and Its Uses
 Common Uses:
Example:
Example:
 CSS Notes
<div> = generic container (groups elements together).

No visual effect by default → styled using CSS.

Acts like a box we can paint, resize, and fill.
Page sections (header, footer, sidebar, content).

Wrapping text, images, and buttons.

Making cards, banners, layouts.
Making a Box with <div>
 Used for profile cards, product listings, banners, etc.
S H E R Y I A N S C O D I N G S C H O O L
 CSS Notes
 3. Background Properties
3.1 Background Color
3.2 Linear Gradient
3.3 Radial Gradient
 Buttons, headers, sections.
 Navigation bars, gradient effects.
 Spotlight / circular highlights.
S H E R Y I A N S C O D I N G S C H O O L
 CSS Notes
3.4 Conic Gradient
3.5 Background Image
3.6 Background Size
3.7 Background Position
 Pie-chart style designs.
 Hero sections with big images.
 Positions image (top, left, right, center).
cover → fills whole area.

contain → fits inside element.

Custom (e.g., 100px 200px).
S H E R Y I A N S C O D I N G S C H O O L
 CSS Notes
3.8 Background Repeat
4.1 Margin
4.2 Padding
repeat (default), repeat-x, repeat-y, no-repeat.
 CSS Box Model
Every element is a box:
Content → text, images.

Padding → inside spacing.

Border → outline.

Margin → outside spacing.
 Adds space outside elements.
 Adds spacing inside (useful for buttons).
S H E R Y I A N S C O D I N G S C H O O L
 CSS Notes
4.3 Border
4.4 Border-Radius
 Styles: solid, dashed, dotted, double.
 Profile pictures, badges.
Rounded corners.

border-radius: 50% → makes a circle.



Day - 11
Sheryians
Coding School
CSS Notes: 

Div, Backgrounds, and Box Model
S H E R Y I A N S C O D I N G S C H O O L
 What is <div> and Its Uses
 Common Uses:
Example:
Example:
 CSS Notes
<div> = generic container (groups elements together).

No visual effect by default → styled using CSS.

Acts like a box we can paint, resize, and fill.
Page sections (header, footer, sidebar, content).

Wrapping text, images, and buttons.

Making cards, banners, layouts.
Making a Box with <div>
 Used for profile cards, product listings, banners, etc.
S H E R Y I A N S C O D I N G S C H O O L
 CSS Notes
 3. Background Properties
3.1 Background Color
3.2 Linear Gradient
3.3 Radial Gradient
 Buttons, headers, sections.
 Navigation bars, gradient effects.
 Spotlight / circular highlights.
S H E R Y I A N S C O D I N G S C H O O L
 CSS Notes
3.4 Conic Gradient
3.5 Background Image
3.6 Background Size
3.7 Background Position
 Pie-chart style designs.
 Hero sections with big images.
 Positions image (top, left, right, center).
cover → fills whole area.

contain → fits inside element.

Custom (e.g., 100px 200px).
S H E R Y I A N S C O D I N G S C H O O L
 CSS Notes
3.8 Background Repeat
4.1 Margin
4.2 Padding
repeat (default), repeat-x, repeat-y, no-repeat.
 CSS Box Model
Every element is a box:
Content → text, images.

Padding → inside spacing.

Border → outline.

Margin → outside spacing.
 Adds space outside elements.
 Adds spacing inside (useful for buttons).
S H E R Y I A N S C O D I N G S C H O O L
 CSS Notes
4.3 Border
4.4 Border-Radius
 Styles: solid, dashed, dotted, double.
 Profile pictures, badges.
Rounded corners.

border-radius: 50% → makes a circle.

Day - 12 & 13
Sheryians
Coding School
CSS Notes: Positioning (Absolute,
Relative, Fixed, Sticky)
S H E R Y I A N S C O D I N G S C H O O L
What is CSS Positioning?
 CSS Notes
The position property controls how elements are placed on a webpage and
how they interact with surrounding elements.
Positions an element relative to its original position in the normal document
flow.
It helps in controlling exact element location within the layout.
static (default) • relative • absolute • fixed • sticky
 Common Values:
 Example:
2. position: relative
 Moves the element 20px down and 30px right from its normal
position.
S H E R Y I A N S C O D I N G S C H O O L
 CSS Notes
 3. position: absolute
Positions the element relative to its nearest positioned ancestor (i.e., an
element with position other than static).

 If no ancestor is positioned, it’s relative to the viewport.
Slightly adjusting icons, badges, or text alignment inside buttons.
 Real-life Use:
 Example:
 The child box is placed 50px from top and left of the parent.
S H E R Y I A N S C O D I N G S C H O O L
 CSS Notes
Used for pop-ups, dropdown menus, tooltips, and overlays.
Perfect for sticky chat buttons, navigation bars, or “Back to Top” links.
Positions the element relative to the browser window (viewport).

 It stays in place even when the page is scrolled.
 Real-life Use:
 Real-life Use:
4. position: fixed
 Example:
 The button stays fixed at the bottom-right corner, even when scrolling.
S H E R Y I A N S C O D I N G S C H O O L
 CSS Notes
 5. position: sticky
Acts like relative until a defined scroll position is reached,

 then becomes “stuck” like fixed.
Used for sticky headers, navbars, or side panels to enhance user navigation.
 Example:
 The header sticks to the top while scrolling and returns when
scrolled back.
 Real-life Use:
S H E R Y I A N S C O D I N G S C H O O L
 CSS Notes
relative
absolute
fixed
sticky
Moves element relative
to its original spot
Positioned inside
nearest positioned
parent
Stays fixed to viewport
during scroll
Acts like relative, then
sticks during scroll
Fine-tuning icon
or text placement
Pop-ups, tooltips,
overlays
Chat buttons,
sticky headers
Navbars, sidebars,
headers
Position Type Description Real-life Use
 Summary Table
S H E R Y I A N S C O D I N G S C H O O L
 CSS Notes
flex-shrink
:hover
Controls how items shrink
Adds interactivity to elements



Day - 14
Sheryians
Coding School
CSS Notes: Flexbox, Icons, and
GitHub Hosting
S H E R Y I A N S C O D I N G S C H O O L
 Display Flex
 Common Values
 CSS Notes
Flexbox is a CSS layout mode used to arrange elements inside a container.

 It’s very powerful for building responsive layouts easily.
The align-items property controls the vertical alignment of flex items inside
the container.
flex-start Align items at the top
flex-end Align items at the bottom
center Align items in the vertical center
 Align Items
 Result: Items now appear next to each other in a single row.
Value Description
S H E R Y I A N S C O D I N G S C H O O L
 CSS Notes
stretch (Default) Items stretch to fill container height
Example:
 Use Case: Vertically centering buttons or icons inside a navigation
bar.
3. Justify Content
The justify-content property controls the horizontal alignment of flex items.
 Common Values
flex-start Align items to the left
flex-end Align items to the right
center Align items in the center
space-between Equal space between items
space-around Equal space around items
space-evenly Equal space everywhere
Value Description
S H E R Y I A N S C O D I N G S C H O O L
 CSS Notes
Example:
Example:
 Steps to Use
 Use Case: Spacing out navigation menu items evenly.
Add the Remix Icon CSS link inside your HTML <head>:
Gap
Using Remix Icon
The gap property adds space between flex items — no need for margins!
Remix Icon is a free icon library that’s easy to use and lightweight.
 Use Case: Creating spacing between cards in a gallery layout.
S H E R Y I A N S C O D I N G S C H O O L
 CSS Notes
Use icons with the <i> tag:
Example:
 Step 1: Create a GitHub Account
 Step 2: Create a Repository
<i class="ri-github-fill"></i> → Displays the GitHub logo.
6. Hosting Website on GitHub Pages
Go to GitHub

Sign up and verify your email.
Click New Repository

Name it (e.g., my-website)

Keep it Public

Click Create Repository
S H E R Y I A N S C O D I N G S C H O O L
 CSS Notes
 Step 3: Upload Your Files
 Step 4: Enable GitHub Pages
 Real-life Example
Open your repository

Click Upload files

Drag and drop your index.html, style.css, etc.

Click Commit changes
Go to Settings → Pages

Under Source, select main branch

Save it

GitHub will provide a live link like this:

 https://yourusername.github.io/my-website/
 Result: Your website is now live for free!
Developers often use GitHub Pages to host portfolio websites, resumes, and
project demos without paying for hosting.
 Summary
S H E R Y I A N S C O D I N G S C H O O L
 CSS Notes
display: flex
align-items
justify-content
gap
Remix Icon
GitHub Pages
Arranges items in
a row or column
Controls vertical
alignment
Controls horizontal
alignment
Adds spacing
between items
Free icon library
Free hosting service
for websites
display: flex;
align-items:
center;
justify-content:
space-between;
gap: 20px;
<i class="rigithub-fill"></i>
GitHub → Settings
→ Pages
Concept / Property Description Example

Day - 15
Sheryians
Coding School
 CSS Notes: Transform, Flexbox
(Detailed), and Hover Effects
S H E R Y I A N S C O D I N G S C H O O L
Transform: translateX() and translateY()
1.1 translateX
 1.2 translateY
 CSS Notes
The transform property lets you move, rotate, scale, or skew elements
without affecting the normal layout.
Moves an element left or right along the X-axis.
Moves an element up or down along the Y-axis.
 Moves the element 100px to the right.

 Use negative values to move it left.
 Moves the element 50px downward.

 Use negative values to move it upward.
 Real-life Example: Adjusting button or image positions in animations.
S H E R Y I A N S C O D I N G S C H O O L
 CSS Notes
2. Centering an Element with Position and Transform
 3. Display Flex (Detailed
You can center an element both horizontally and vertically using position:
absolute and transform: translate.
Flexbox helps align and distribute elements efficiently inside a container.
 Example
 The box is perfectly centered inside the parent.
 Real-life Use: Popups, modals, or loading screens.
 Basic Setup
S H E R Y I A N S C O D I N G S C H O O L
 CSS Notes
 All items appear in a single horizontal row.
 Why Use Flexbox?
Simplifies responsive layouts

Easily aligns items both vertically and horizontally

Eliminates need for float or complex margins
 4. Align Items
Controls vertical alignment of flex items.
flex-start Align items at the top
flex-end Align items at the bottom
center Align items in the vertical center
stretch Items stretch to fill container (default)
Value Description
S H E R Y I A N S C O D I N G S C H O O L
 CSS Notes
 Example
 Commonly used for buttons, icons, or card alignment.
5. Justify Content
Controls horizontal alignment of items.
flex-start Align left
flex-end Align right
center Centered
space-between Equal space between items
space-around Equal space around items
space-evenly Equal space everywhere
Value Description
S H E R Y I A N S C O D I N G S C H O O L
 CSS Notes
 Use Case: Navigation bar links spaced evenly.
 6. Flex Direction
 Example
 Example
Defines the direction in which flex items are placed.
row Horizontal (default)
row-reverse Reversed horizontally
column Vertical stacking
column-reverse Reversed vertical order
Value Description
S H E R Y I A N S C O D I N G S C H O O L
 CSS Notes
 7. Flex Wrap
 8. Flex Shrink
Allows items to wrap onto multiple lines when space runs out.
Defines how much an item shrinks when space is limited.
nowrap (default) All items on one line
wrap Items move to next line if needed
wrap-reverse Wraps in reverse order
Value Description
 Example
 Example
 Use Case: Product cards wrapping on smaller screens.
Simplifies responsive layouts

Easily aligns items both vertically and horizontally

Eliminates need for float or complex margins
S H E R Y I A N S C O D I N G S C H O O L
 CSS Notes
Simplifies responsive layouts

Easily aligns items both vertically and horizontally

Eliminates need for float or complex margins
 Use Case: Preventing logos or images from shrinking.
 Use Case: Buttons that change color and size when hovered.
9. Hover Effects
The :hover pseudo-class lets you style elements on mouse hover, adding
interactivity.
 Example
S H E R Y I A N S C O D I N G S C H O O L
 CSS Notes
 Summary
transform
translateX / Y
display: flex
align-items
justify-content
flex-direction
flex-wrap
Moves or scales elements
visually
Shifts element along X or Y
axis
Organizes items in flexible
layouts
Controls vertical alignment
Controls horizontal alignment
Defines arrangement
direction
Allows wrapping of elements
Concept Description
S H E R Y I A N S C O D I N G S C H O O L
 CSS Notes
flex-shrink
:hover
Controls how items shrink
Adds interactivity to elements

Day - 16
Sheryians
Coding School
CSS Notes: Boilerplate, Transform,
Perspective, Hover, and Transition
S H E R Y I A N S C O D I N G S C H O O L
 CSS Boilerplate
Transform (All Properties)
2.1 translate()
 CSS Notes
A CSS boilerplate resets browser defaults for consistent layouts and easier
styling.
 Like starting with a clean canvas before painting!
 Explanation
* { margin: 0; padding: 0; } → Removes unwanted spacing across browsers.

box-sizing: border-box; → Includes padding & borders within total size.

html, body { height: 100%; width: 100%; } → Ensures full page layout.
The transform property changes how elements appear — move, scale,
rotate, or skew — without affecting layout flow.
S H E R Y I A N S C O D I N G S C H O O L
 CSS Notes
Moves an element along the X & Y axes.
 Moves element 50px right & 100px down.
 Enlarges by 1.5×.
2.2 scale()
Resizes the element.
You can also use:
S H E R Y I A N S C O D I N G S C H O O L
 CSS Notes
2.3 rotate()
2.4 skew()
2.5 matrix()
Rotates the element clockwise.
Tilts the element.
Combines multiple transforms together.
 Complex & rarely used directly.
S H E R Y I A N S C O D I N G S C H O O L
 CSS Notes
 Common use: animations — rotating icons, enlarging buttons,
sliding images.
 Smaller perspective = stronger 3D effect.

3. Perspective
4. Hover
Adds 3D depth for transforms.
 Apply to the parent element.
The :hover pseudo-class styles elements on mouse hover.
 Use case: 3D card flips, cube rotations.
S H E R Y I A N S C O D I N G S C H O O L
 CSS Notes
 Use case: interactive buttons, icons, links.
5. Transition
Makes property changes smooth & animated.
Syntax:
Example:
S H E R Y I A N S C O D I N G S C H O O L
 CSS Notes
Common Properties:
transition-property → What to animate

transition-duration → How long it takes

transition-timing-function → Ease, linear, etc.

transition-delay → Wait before start
 Use case: cards, modals, buttons — for smooth UI motion.
S H E R Y I A N S C O D I N G S C H O O L
 CSS Notes
Boilerplate
Transform
Perspective
Hover
Transition
Resets default styles
Move, rotate, scale,
skew
Adds 3D depth
Triggers on mouse hover
Smooth effect change
Clean layout base
Animation effects
3D card flip
Button color
change
Animated hover
button
Concept Description Real-life Example
Summary

Day - 17
Sheryians
Coding School
 CSS Notes: Display, Background Clip,
Text Stroke, and Scrollbar Removal
S H E R Y I A N S C O D I N G S C H O O L
 Display Property
1.1 display: block
1.2 display: inline
 CSS Notes
The display property controls how elements are arranged and how they
occupy space in a layout.
Takes the full width of the parent container.

Always starts on a new line.
Takes only as much width as its content.

Does not start on a new line.
 Examples: <div>, <p>, <h1> are block-level elements.
 Examples: <span>, <a>, <b>, <i>
S H E R Y I A N S C O D I N G S C H O O L
 CSS Notes
 Use Case: Inline elements are perfect for styling or emphasizing
text inside a paragraph.
 Use Case: Perfect for buttons or small elements aligned in a row.
 Use Case: Perfect for buttons or small elements aligned in a row.
1.3 display: inline-block
1.4 display: grid
Behaves like inline (sits in one line)

Allows setting width, height, and margin.
Turns a container into a grid layout.

Enables advanced control using rows and columns.
S H E R Y I A N S C O D I N G S C H O O L
 CSS Notes
2. Background Clip (background-clip)
3. Text Stroke
The background-clip property defines how far the background extends
within an element.
The -webkit-text-stroke property adds an outline around the text, giving it a
bold or outlined effect.
Values
Gradient Text Example
border-box → Covers border + padding + content.

padding-box → Inside padding only.

content-box → Inside content only.
 Result: Gradient-filled text using background-clip: text.
 Real-life Example: Stylish headings, logo effects, and hero
banners.
S H E R Y I A N S C O D I N G S C H O O L
 CSS Notes
Example:
Gradient + Stroke Combo
 Result: A red outline with transparent fill.
 Use Cases:
Bold hero headers

Neon or outlined typography

Stylish text with gradient fill
4. Removing Scrollbar (Webkit)
To hide the scrollbar while keeping scroll functionality:
S H E R Y I A N S C O D I N G S C H O O L
 CSS Notes
Alternative (Hide but Scroll)
 Works only on WebKit browsers (Chrome, Safari, Edge).
 Real-life Example: Clean UIs, sliders, and image galleries without
visible scrollbars.
display
background-clip
text-stroke
scrollbar
removal
Controls element
layout style
Defines how
background spreads
Adds text outline
Hides scrollbars for
clean look
Structure pages,
align content
Gradient text or
shapes
Bold titles, neon
effects
Sliders, modern
layouts
Concept Description Real-life use
Summary



Day - 18
Sheryians
Coding School
HTML Semantics and CSS Grid Notes
S H E R Y I A N S C O D I N G S C H O O L
 HTML Semantics and Their Role
HTML Semantics and CSS Grid Notes
Semantic HTML means using tags that describe their purpose clearly —
instead of just <div> or <span>.

 It helps browsers, developers, and search engines understand your content
better.
<header>, <main>, <article>, <footer>, etc.
What is Semantic HTML?
Why Semantic HTML Matters
Common Semantic Tags
Example Tag:
 Improves Accessibility — Screen readers can interpret page structure
easily.

 Better SEO — Search engines rank pages higher with meaningful
markup.

 Clean Code — Easier to read and maintain.

 Better Understanding — Developers can quickly identify each section’s
purpose.
Tag Description Example Use
<header> Top section of a page or
article
Logo, navigation
bar
S H E R Y I A N S C O D I N G S C H O O L
HTML Semantics and CSS Grid Notes
<nav>
<article>
<main>
<aside>
<aside>
<section>
<footer>
<figure>
Navigation section
Independent content
block
Main unique content of
page
Side information
Side information
Groups related topics
Bottom section
Media group (images,
charts)
Menus, sidebar
links
Blog posts, news
Blog content
Ads, related links
Ads, related links
Service sections
Copyright info
Image + caption
S H E R Y I A N S C O D I N G S C H O O L
HTML Semantics and CSS Grid Notes
<figcaption>
<time>
<address>
Caption for a figure
Represents date/time
Contact info
Describes image
Publish date
Email, location
Semantic HTML Example
 Real-life Use Case:
Used in blogs, news sites, or portfolios to create structure and improve SEO.
S H E R Y I A N S C O D I N G S C H O O L
HTML Semantics and CSS Grid Notes
Basic Grid Setup
2. CSS Grid and Its Properties
What is CSS Grid?
Common Grid Properties
CSS Grid is a 2D layout system that lets you create advanced page layouts
using rows and columns — great for designing entire web pages.
 Creates a 3-column, 2-row grid with 10px gap between boxes.
display: grid
grid-templatecolumns
Defines a grid
container
Sets number and width
of columns
display: grid;
repeat(3, 1fr)
Property Description Example
S H E R Y I A N S C O D I N G S C H O O L
HTML Semantics and CSS Grid Notes
grid-templaterows
align-content
gap
grid-auto-rows
justify-items
grid-auto-flow
justify-content
Sets row heights
Moves grid vertically
Adds spacing between
items
Default height for
implicit rows
Aligns content
horizontally
Controls placement flow
Moves entire grid
horizontally
100px 200px
space-between
gap: 20px
minmax(100px,
auto)
center
row, column
space-around
3. Grid Template Areas — Visual Layout Design
Example
S H E R Y I A N S C O D I N G S C H O O L
HTML Semantics and CSS Grid Notes
 Visually maps your webpage layout — just like a wireframe.
 Use Case: Ideal for full-page layouts like dashboards or portfolios.
S H E R Y I A N S C O D I N G S C H O O L
HTML Semantics and CSS Grid Notes
4. Other Useful Grid Properties
Property Description
place-items: center;
place-content: center;
minmax(200px, 1fr)
repeat(4, 1fr)
Shorthand for align-items
+ justify-items
Shorthand for align-content +
justify-content
Sets flexible column size
Repeats grid pattern easily
S H E R Y I A N S C O D I N G S C H O O L
HTML Semantics and CSS Grid Notes
 Summary
Semantic HTML
CSS Grid
Grid Areas
Combine Both
Adds meaning and
structure to content
2D layout system for
web design
Simplifies layout using
named regions
Semantic HTML + Grid
SEO & Accessibility
Webpage and
dashboard layouts
Clean, visual
arrangement
Professional,
responsive,
accessible web
designs
Concept Description Use Case



How to Create Responsive Websites Like a Pro
Prajapatiankur
Prajapatiankur

Follow
4 min read
·
Jun 3, 2025
110


13

1



In this post, let’s break down how to actually build fully responsive websites that don’t break the internet (or your codebase). No fluff, just the real dev wisdom.

Press enter or click to view image in full size

1. Start with Breakpoints in Mind
Before you even touch your CSS, take a step back and study your design across all screen sizes — mobile, tablet, desktop, and large desktops.

Use a smart layout with nested containers so that adapting to screen sizes is as simple as changing flex-direction or grid-template-columns.

50% of responsive design is just solid HTML structure.

Press enter or click to view image in full size

<!-- mobile first approach -->
<section class="some-section">
    <div class="top">
        <img
            src="hero.webp"
            alt="hero image"
        >
    </div>
    <div class="bottom">
        <div class="left">
            <p>some text</p>
        </div>
        <div class="right">
            <h1>some heading</h1>
            <p>paragraph</p>
        </div>
    </div>
</section>
2. Always Use Mobile-First CSS
Write your CSS for mobile first, then scale up using media queries.

It keeps the code clean and the UX solid for the majority of users who visit from phones.

/* Mobile styles */
.example {
    font-size: 1rem;
}

/* Tablet styles */
@media (min-width: 768px) {
    .example {
        font-size: 1.25rem;
    }
}

/* Desktop styles */
@media (min-width: 1024px) {
    .example {
        font-size: 1.5rem;
    }
}
3. Use Responsive CSS Units (`rem`, `em`)
Using px locks values to a fixed size, which breaks flexibility across devices and ignores user accessibility settings.

Instead, use rem, em, or % to make your design fluid, scalable, and responsive to browser settings like Zoom ( Ctrl + ) or custom font size.

html {
  font-size: clamp(0.875rem, 1vw + 0.5rem, 1.125rem);
}

h1 {
  font-size: 2rem; /* Scales based on the root size */
}
4. Flexbox & Grid
Flexbox and CSS Grid are your best friends for building responsive layouts.

Get Prajapatiankur’s stories in your inbox
Join Medium for free to get updates from this writer.

Enter your email
Subscribe

Remember me for faster sign in

You can create stacked layouts for mobile and horizontal ones for bigger screens — without adding a ton of media queries.

.responsive-section {
    display: flex;
    flex-direction: column;
}

@media (min-width: 768px) {
    .responsive-section {
        flex-direction: row;
    }
}
5. Use `clamp()` for Font Sizes
This ensures that text stays comfortably readable on smaller screens, grows proportionally on tablets and desktops, and avoids becoming overwhelmingly large on 4K or ultra-wide displays. It’s the perfect balance between accessibility and aesthetics, making sure your typography adapts naturally while still respecting boundaries.

html {
    font-size: clamp(0.875rem, 1vw + 0.5rem, 1.125rem);
}
6. Define CSS Variables (custom properties) for Reusability
This approach centralizes your design tokens, making it easy to update a value in one place and have that change reflected across your entire site.

It also pairs beautifully with media queries — you can redefine variables at different breakpoints for fully responsive design without rewriting the entire CSS block. Plus, when working in a team or maintaining a large project, variables instantly improve readability and reduce bugs caused by inconsistent values.

:root {
  --font-size-sm: 0.875rem;
  --font-size-md: 1rem;
  --border-radius-lg: 0.5rem;
}
7. Use Wrapper Sections for Centered Layouts
When designing for large screens, it’s important to prevent your content from stretching edge-to-edge, which can make it harder to read and visually unbalanced.

To fix this, wrap your section content inside a container div (commonly called a “wrapper”) and apply a max-width along with margin: auto. This centers the content and restricts its width, ensuring it stays clean, readable, and aligned — especially on desktop and ultra-wide monitors.

.wrapper {
  max-width: 1200px;
  margin: 0 auto;
}
Press enter or click to view image in full size

It’s a small trick that makes a huge difference in your overall UI polish.

8. Use Section Padding + Media Queries
Consistent vertical spacing makes layouts clean and breathable. Use padding-top and padding-bottom for each section, and adjust them with media queries. Define values as CSS variables for easy updates across breakpoints

Just make sure your media queries are spaced logically — intervals of 150px to 200px work well in most cases

@media (max-width: 800px) {
    section{
        --padding-top: 60px;
        --padding-bottom: 60px;
    }
}

@media (min-width: 800px) and (max-width: 1000px) {
    section{
        --padding-top: 100px;
        --padding-bottom: 100px;
    }
}

@media (min-width: 1000px) and (max-width: 1200px) {
    section{
        --padding-top: 150px;
        --padding-bottom: 100px;
    }
}

@media (min-width: 1200px){
    section{
        --padding-top: 200px;
        --padding-bottom: 150px;
    }
}
9. Don’t Be Scared of Media Queries
Media queries are essential for building truly responsive designs. While too many can clutter your code, avoiding them limits flexibility. The key is to strike a balance — use them where they add real value, organize them cleanly, and combine them with techniques like flex, grid, and clamp() to minimize overuse. When used wisely, media queries help your UI feel tailored across all devices without becoming a maintenance nightmare.

Final Thoughts
Start mobile-first. Use fluid units. Embrace CSS grid/flex. Structure your HTML with intention.



SCSS (sassy css)

SCSS is an advanced version of CSS that makes writing styles easier and
more powerful. It adds extra features like nesting, mixins, and imports,
which help you write cleaner and more organized code.

### 3. Nesting

In normal CSS, you often repeat selectors again and again:

But in SCSS, you can **nest** your CSS the same way your HTML is
structured: it makes your css more neat and readable


nav {
  background: black;

  ul {
    list-style: none;

    li {
      display: inline-block;

      a {
        color: white;
        text-decoration: none;
      }
    }
  }
}


------------------------------------------------------------------------

### 4. Partials & Import

When your project grows, you don't want all your code in **one big
file** it's confusing.

So SCSS allows you to **split your styles** into small files called
**partials**.

For example : partial files start with `_` (underscore)

    _header.scss
    _footer.scss
    _variables.scss
    style.scss

Then you combine them in your main file using:


@import "header";
@import "footer";


------------------------------------------------------------------------

### 5. Mixins

A **mixin** is like a "reusable piece of code."

If you find yourself writing the same CSS again and again for example,
Flexbox centering you can save it as a mixin.

Example:


@mixin flex-center {
  display: flex;
  justify-content: center;
  align-items: center;
}

.container {
  @include flex-center;
}


Now you can use `@include flex-center;` anywhere you need centering.

No need to retype those three lines again and again.

You can even make your mixins smarter by adding **arguments** (like
function parameters):


@mixin box($width, $color) {
  width: $width;
  background: $color;
}

.card {
  @include box(200px, #ff6347);
}

So now your `.card` will automatically get a width of 200px and a
background color of tomato all from one reusable mixin.

------------------------------------------------------------------------

### 6. Built-in Functions

SCSS has some **in-built color tools** that make design tweaks super
easy.

Examples:

lighten($color, 20%); // makes the color lighter
darken($color, 10%);  // makes the color darker
mix(#ff0000, #0000ff, 50%); // mixes two colors

You can use them like this:

button {
  background: lighten(#3498db, 10%);
}

