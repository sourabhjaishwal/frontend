# What is react and why devs use it for making up a project or product

# Why react replaces html css js or is react just a bundler?

# Steps to Create a Vite Project

## 1. Install Node.js

Install Node.js (LTS) on your system from the official Node.js website.  
(Windows / macOS – same process)

## 2. Run the Command (Create Vite Project)

```bash
npm create vite
```

## 3. Project Name

Project name: › my-project

Creates a folder with this name.

## 4. Select Framework

Options:

- Vanilla
- React
- Vue
- Svelte
- Solid
- Preact

Example:

Select a framework: › React

## 5. Select Variant (Language)

Options:

- JavaScript
- TypeScript
- JavaScript + SWC
- TypeScript + SWC

Recommended:

JavaScript + SWC

## 6. Move Into Project Folder

```bash
cd my-project
```

## 7. Install Dependencies

```bash
npm install
```

## 8. Start Development Server

```bash
npm run dev
```

## 9. Local Development URL

http://localhost:5173/

click on index.html

- there is an id "root" - it is parent element

come to main and app - empty everything
app.jsx parent element is - main.jsx
main.jsx parent element is - index.html

come to main.js - add these code

- import ReactDOM from 'react-dom/client';
- const root = ReactDOM.createRoot(document.getElementById('root))
- root.render()

come to app.js - add these

- const app = () => { return 'Hello from APP'}
- export default App

next come to main.js - update

- import ReactDOM from 'react-dom/client';
- import app from './App' -- Here we are importing the app.jsx
- const root = ReactDOM.createRoot(document.getElementById('root))
- root.render(<App/>) -- self closing tag -- Here we are calling the app.jsx (whatever is written in app.jsx it will load into root element of index.html)

(Here we are using jsx inside of js) - both js + html can be written in a single jsx file (combination) - directly we are writing html in a js file

- a function will return only one thing

trick: rafce - shortcut/snippet to create a boilerplate code inside app.jsx

Now go to index.html

- before root id - add few html tags (h1, h2, hr) - just for experimenting
- also you change the name of root to anything, but make sure for production apps keep as root only

## cleanup the project for ease of use

folder strcuture

- assets folder- improtant files (optional for now) you can remove
- public folder- static files (optional for now) you can remove
- remove app.css (not required as of now)
- remove or keep empty or add your your css - index.css
- you can import index.css to main.jsx instead of linking to index.html
- download extensions in vscode (react snippets and es7 react)
