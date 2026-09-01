# React.js

> **Purpose:** This section covers keeps the individual concepts short to revise them quickly.

## 1. Introduction To React.js

**Short Definition**

React is a JavaScript library for building fast, interactive and scalable user interfaces, especially Single Page Applications (SPAs).

**Example / Visual**

```text
React App
   ↓
Components
   ↓
Interactive UI
   ↓
No full-page reload
```

**Key Points**

- Created by **Jordan Walke** at **Facebook (Meta)**.
- First released in 2013.
- Maintained by Meta and the open-source community.
- UI is built using reusable components.

---

## 2. Single Page Application (SPA)

**Short Definition**

An SPA is a web application where the page does not fully reload when navigating or updating content.

**Example / Visual**

```text
Traditional:
Page → Reload → New Page

React SPA:
Page → Component changes → Same page
```

**Key Points**

- Provides smooth navigation.
- React updates required UI portions.
- Commonly used for dashboards and web applications.
- React is well suited for SPA development.

---

## 3. React Component

**Short Definition**

A component is a reusable, independent UI block in React.

**Example**

```jsx
function Button() {
  return <button>Click Me</button>;
}
```

**Key Points**

- Components are usually written as functions.
- Component names start with a capital letter.
- Components can be reused.
- Keep components small and focused.

---

## 4. React Project Structure with Vite

**Short Definition**

Vite provides a fast development setup for React projects.

**Example**

```bash
npm create vite
cd my-project
npm install
npm run dev
```

**Key Points**

- Select **React** as the framework.
- Select JavaScript, TypeScript or other available variants.
- Development server commonly runs at `localhost:5173`.
- Node.js is required.

---

## 5. `main.jsx` and `App.jsx`

**Short Definition**

`App.jsx` contains the main application component, while `main.jsx` mounts React into the HTML page.

**Example**

```jsx
const App = () => {
  return <h1>Hello from App</h1>;
};

export default App;
```

```jsx
import ReactDOM from "react-dom/client";
import App from "./App";

const root = ReactDOM.createRoot(document.getElementById("root"));

root.render(<App />);
```

**Key Points**

- `App.jsx` contains application UI.
- `main.jsx` is the React entry point.
- `createRoot()` connects React to the HTML element.
- `<App />` renders the App component.

---

## 6. React Project Cleanup

**Short Definition**

Project cleanup means removing unnecessary starter files and keeping only what the application needs.

**Example / Visual**

```text
src/
├── assets/
├── App.jsx
├── index.css
└── main.jsx
```

**Key Points**

- `assets` and `public` can be removed if unnecessary.
- `App.css` can be removed when not needed.
- `index.css` can contain global styles.
- `index.css` can be imported into `main.jsx`.

---

## 7. `rafce`

**Short Definition**

`rafce` is a VS Code React snippet used to quickly generate a functional component with export.

**Example**

```text
rafce → React Arrow Function Component
```

**Key Points**

- Saves typing.
- Commonly provided by React/ES7 snippets extensions.
- Useful while creating components.
- Component name should use PascalCase.

---

## 8. Real DOM

**Short Definition**

The Real DOM is the actual Document Object Model maintained by the browser.

**Example**

```javascript
document.getElementById("box").innerText = "Hello";
```

**Key Points**

- Directly represents the browser UI.
- JavaScript can manipulate it directly.
- Frequent updates can cause reflow/repaint.
- React abstracts most direct DOM manipulation.

---

## 9. Virtual DOM

**Short Definition**

The Virtual DOM is an in-memory representation of the UI that React uses to determine efficient DOM updates.

**Example / Visual**

```text
State / Props change
        ↓
New Virtual DOM
        ↓
Compare with old
        ↓
Update required DOM
```

**Key Points**

- Exists in memory.
- React compares previous and new UI representations.
- Only required changes are applied to the Real DOM.
- Helps make UI updates efficient.

---

## 10. Real DOM vs Virtual DOM

**Short Definition**

Real DOM directly represents browser elements, while React's Virtual DOM helps React determine efficient updates.

**Example**

```text
Real DOM       → Direct browser updates
Virtual DOM    → Compare → Minimal DOM updates
```

**Key Points**

- Real DOM is the actual browser DOM.
- Virtual DOM exists in memory.
- React uses reconciliation/diffing to determine changes.
- Virtual DOM is an implementation detail used to optimize updates.

---

## 11. JSX

**Short Definition**

JSX is a JavaScript syntax extension that allows HTML-like markup inside JavaScript.

**Example**

```jsx
const element = <h1>Hello React</h1>;
```

**Key Points**

- JSX is not HTML.
- JSX is transformed into JavaScript.
- JavaScript expressions can be written using `{}`.
- JSX makes component UI easier to write.

---

## 12. JSX Component Naming

**Short Definition**

React component names must begin with a capital letter.

**Example**

```jsx
function Header() {
  return <h1>Header</h1>;
}
```

**Key Points**

- `Header` → React component.
- `header` → interpreted as an HTML/custom element name.
- Use PascalCase for components.
- Consistent naming improves readability.

---

## 13. React Fragments

**Short Definition**

A Fragment groups multiple JSX elements without adding an extra DOM element.

**Example**

```jsx
return (
  <>
    <h1>Hello</h1>
    <p>Welcome</p>
  </>
);
```

**Key Points**

- Uses `<>...</>`.
- Avoids unnecessary wrapper `<div>`.
- Keeps the DOM cleaner.
- Useful when a component needs to return multiple elements.

---

## 14. Styling in React

**Short Definition**

React supports different approaches for styling components.

**Example**

```text
React Styling
├── Inline Styles
├── CSS Stylesheets
├── CSS Modules
├── Utility CSS
└── CSS-in-JS
```

**Key Points**

- Inline styles are useful for small dynamic styles.
- CSS stylesheets work well for general styling.
- CSS Modules provide locally scoped classes.
- Utility-first CSS such as Tailwind is another approach.

---

## 15. CSS Modules

**Short Definition**

CSS Modules provide locally scoped CSS class names for a component.

**Example**

```text
Button.module.css
```

```css
.btn {
  padding: 10px;
}
```

```jsx
import styles from "./Button.module.css";

<button className={styles.btn}>Click</button>;
```

**Key Points**

- File convention: `Component.module.css`.
- Classes are scoped to the component.
- Reduces global CSS conflicts.
- Useful for component-based applications.

---

## 16. Reusable Components

**Short Definition**

A reusable component is created once and used multiple times with different data.

**Example**

```jsx
<Card title="HTML" />
<Card title="CSS" />
<Card title="React" />
```

**Key Points**

- Reduces duplicate code.
- Props make components reusable.
- Components should have a clear responsibility.
- Reusability is a major benefit of React.

---

## 17. Props

**Short Definition**

Props are data passed from a parent component to a child component.

**Example**

```jsx
<Card title="React" />
```

```jsx
function Card({ title }) {
  return <h2>{title}</h2>;
}
```

**Key Points**

- Props are read-only.
- Data normally flows parent → child.
- Props can contain strings, numbers, objects, arrays and functions.
- They make components reusable.

---

## 18. Passing Functions as Props

**Short Definition**

A parent can pass a function to a child so the child can trigger parent logic.

**Example**

```jsx
function App() {
  const handleClick = () => {
    console.log("Clicked");
  };

  return <Button onClick={handleClick} />;
}
```

**Key Points**

- Functions can be passed like normal props.
- Useful for child → parent communication.
- Child calls the received function.
- Supports React's one-way data flow.

---

## 19. Passing Styles as Props

**Short Definition**

A style object can be passed to a component as a normal prop.

**Example**

```jsx
const boxStyle = {
  width: "150px",
  backgroundColor: "orange",
};

<Box style={boxStyle} />;
```

**Key Points**

- Style objects use camelCase properties.
- `style` can be passed as a prop.
- Child applies it using `style={style}`.
- Useful for reusable styled components.

---

## 20. Partial Styles as Props

**Short Definition**

Individual style values can be passed as props and combined inside the child.

**Example**

```jsx
<Card bgColor="black" textColor="white" />
```

**Key Points**

- Child receives individual style values.
- Child can combine them with its own styles.
- Keeps reusable components flexible.
- Useful for configurable UI components.

---

## 21. Lists in React

**Short Definition**

Lists are commonly rendered using JavaScript's `map()` method.

**Example**

```jsx
items.map((item) => <Card key={item.id} title={item.name} />);
```

**Key Points**

- `map()` converts data into JSX.
- Each rendered item needs a `key`.
- Lists are useful for users, products, posts, etc.
- Data is usually stored in arrays.

---

## 22. Keys

**Short Definition**

A key uniquely identifies an item in a React list.

**Example**

```jsx
items.map((item) => <Card key={item.id} />);
```

**Key Points**

- Keys should be unique among siblings.
- Prefer stable IDs.
- Helps React track list changes.
- Avoid array indexes when list items can be reordered or removed.

---

## 23. Conditional Rendering

**Short Definition**

Conditional rendering means displaying different UI based on a condition.

**Example**

```jsx
{
  isLoggedIn ? <Dashboard /> : <Login />;
}
```

**Key Points**

- Uses normal JavaScript conditions.
- Can depend on state, props or API data.
- Ternary operators are useful for two alternatives.
- `&&` is useful for conditionally showing one element.

---

## 24. React Event Handling

**Short Definition**

React events allow components to respond to user interactions.

**Example**

```jsx
<button onClick={handleClick}>Click</button>
```

**Key Points**

- Event names use camelCase.
- Pass a function, not the function result.
- Events can update state.
- Event handlers receive event information when needed.

---

## 25. Common React Events

**Short Definition**

React provides event handlers for mouse, keyboard, form and focus interactions.

**Example**

```jsx
<input onChange={handleChange} />
<form onSubmit={handleSubmit}>
```

**Key Points**

- `onClick` → click.
- `onChange` / `onInput` → input changes.
- `onMouseEnter` / `onMouseLeave` → mouse movement.
- `onFocus`, `onBlur`, `onKeyDown`, `onDoubleClick`, `onScroll` handle other interactions.

---

## 26. `preventDefault()`

**Short Definition**

`event.preventDefault()` prevents the browser's default action.

**Example**

```jsx
function handleSubmit(e) {
  e.preventDefault();
  console.log("submitted");
}
```

**Key Points**

- Commonly used with forms.
- Prevents the normal page reload during form submission.
- Allows React to handle the action.
- The event object is received as a parameter.

---

## 27. Arrow Function in Events

**Short Definition**

An arrow function can be used when an event needs to execute inline logic.

**Example**

```jsx
<button onClick={() => console.log("clicked")}>Click</button>
```

**Key Points**

- Useful for short event handlers.
- Can pass arguments easily.
- Function executes when the event occurs.
- Do not write `onClick={handleClick()}` unless you intentionally want immediate execution.

---

## 28. State

**Short Definition**

State is data stored by a component that can change over time and cause the UI to update.

**Example**

```jsx
const [count, setCount] = useState(0);
```

**Key Points**

- State stores changing values.
- Examples: counters, forms, toggles and API data.
- Updating state causes a re-render.
- Data that never changes does not need state.

---

## 29. `useState()`

**Short Definition**

`useState` is a React Hook used to create and update state in functional components.

**Example**

```jsx
const [count, setCount] = useState(0);
```

**Key Points**

- `count` → current state.
- `setCount` → state updater.
- `0` → initial value.
- State updates cause the component to re-render.

---

## 30. State Update and Re-render

**Short Definition**

When state changes through its setter, React renders the component again with the new state.

**Example / Visual**

```text
setCount(...)
     ↓
State changes
     ↓
Component re-renders
     ↓
Updated UI
```

**Key Points**

- Do not directly modify state.
- Use the setter function.
- React updates the UI automatically.
- State is preserved between renders.

---

## 31. State Immutability

**Short Definition**

React state should be updated by creating a new value rather than directly mutating the existing value.

**Example**

```jsx
setUsers([...users, newUser]);
```

**Key Points**

- Use spread syntax for arrays/objects.
- Do not directly mutate state.
- New state references help React detect updates.
- This is especially important for arrays and objects.

---

## 32. Controlled Component

**Short Definition**

A controlled component is a form element whose value is controlled by React state.

**Example**

```jsx
const [email, setEmail] = useState("");

<input value={email} onChange={(e) => setEmail(e.target.value)} />;
```

**Key Points**

- State controls the input value.
- `onChange` updates the state.
- React becomes the source of truth.
- Common in React forms.

---

## 33. Two-Way Binding

**Short Definition**

Two-way binding means the UI updates state and state updates the UI.

**Example / Visual**

```text
User types
    ↓
onChange
    ↓
setState
    ↓
State changes
    ↓
UI updates
```

**Key Points**

- React fundamentally follows one-way data flow.
- Controlled inputs can create this two-way interaction.
- Uses `useState`, `value` and `onChange`.
- Useful for forms.

---

## 34. Form Submission in React

**Short Definition**

React handles form submission using the form's `onSubmit` event.

**Example**

```jsx
<form onSubmit={submitHandler}>
  <button type="submit">Submit</button>
</form>
```

**Key Points**

- Use `e.preventDefault()` when preventing page reload.
- Form can submit through the button or Enter key.
- State can store submitted data.
- Controlled inputs can be reset after submission.

---

## 35. Local Storage

**Short Definition**

Local Storage is browser storage that stores key-value data persistently.

**Example**

```javascript
localStorage.setItem("theme", "dark");

localStorage.getItem("theme");
```

**Key Points**

- Data survives refresh and browser restart.
- Data is stored as strings.
- It belongs to the Web Storage API.
- Useful for preferences and cached client-side data.

---

## 36. Local Storage vs Session Storage vs Cookies

**Short Definition**

All three store browser-related data but differ in lifetime, capacity and server behavior.

**Example / Visual**

```text
Local Storage   → Long-term browser data
Session Storage → Current tab/session
Cookies         → Data that can be sent to server
```

**Key Points**

- Local Storage remains until cleared.
- Session Storage generally lasts for the browser tab/session.
- Cookies can have expiration rules.
- Cookies are automatically sent with applicable HTTP requests.

---

## 37. Client-Side Rendering (CSR)

**Short Definition**

CSR is a rendering approach where the browser executes JavaScript and builds the UI on the client.

**Example / Visual**

```text
Server
  ↓
HTML + JS
  ↓
Browser executes React
  ↓
UI rendered
```

**Key Points**

- Browser performs much of the UI rendering.
- Common for interactive SPAs.
- Smooth client-side interactions.
- SEO and initial loading need additional consideration.

---

## 38. Server-Side Rendering (SSR)

**Short Definition**

SSR generates the initial HTML on the server before sending it to the browser.

**Example / Visual**

```text
Browser request
      ↓
Server renders HTML
      ↓
Browser displays HTML
      ↓
JavaScript adds interactivity
```

**Key Points**

- Server generates initial HTML.
- Useful for content-heavy applications.
- Can improve initial content visibility and SEO.
- Requires more server-side rendering infrastructure.

---

## 39. CSR vs SSR

**Short Definition**

CSR renders primarily in the browser, while SSR renders the initial page on the server.

**Example**

| CSR                     | SSR                            |
| ----------------------- | ------------------------------ |
| Browser rendering       | Server rendering               |
| Common for web apps     | Common for content-heavy sites |
| Client downloads JS     | Server sends rendered HTML     |
| SEO needs consideration | Strong initial SEO potential   |

**Key Points**

- CSR is highly interactive.
- SSR can provide faster initial content.
- Both can be combined in modern React frameworks.
- Choice depends on application requirements.

---

## 40. Axios

**Short Definition**

Axios is a promise-based HTTP client used to make API requests from browsers and Node.js.

**Example**

```javascript
axios.get("/api/users");
```

**Key Points**

- Simplifies HTTP requests.
- Automatically parses JSON responses.
- Supports interceptors.
- Supports cancellation and timeouts.

---

## 41. Axios vs Fetch

**Short Definition**

Both Axios and Fetch can communicate with APIs, but they provide different APIs and default behaviors.

**Example**

```text
Fetch:
fetch() → response.json()

Axios:
axios.get() → response.data
```

**Key Points**

- Fetch requires explicit JSON conversion.
- Axios provides parsed response data.
- Axios rejects promises for HTTP error status codes by default.
- Axios provides additional request/response features.

---

## 42. Axios with `useEffect`

**Short Definition**

Axios can be used inside `useEffect` to fetch data when a component loads or when dependencies change.

**Example**

```jsx
useEffect(() => {
  axios
    .get("/api/users")
    .then((response) => setUsers(response.data))
    .catch((error) => console.error(error));
}, []);
```

**Key Points**

- `axios.get()` sends the request.
- `response.data` contains server data.
- `useEffect` controls when the request runs.
- `useState` stores the response data.

---

## 43. Axios Error Handling

**Short Definition**

Axios errors can be handled using `.catch()`.

**Example**

```jsx
axios
  .get("/api/data")
  .then((res) => console.log(res.data))
  .catch((err) => {
    console.log(err);
  });
```

**Key Points**

- Network errors can occur.
- Servers can return 4xx/5xx errors.
- Requests can time out.
- `err.response` can provide server response information.

---

## 44. `useEffect`

**Short Definition**

`useEffect` is a React Hook used to perform side effects such as API calls, timers, DOM updates and event listeners.

**Example**

```jsx
useEffect(() => {
  console.log("Effect");
}, []);
```

**Key Points**

- Runs after rendering.
- Dependency array controls when it runs.
- Useful for external systems and side effects.
- Can return a cleanup function.

---

## 45. `useEffect` Dependency Array

**Short Definition**

The dependency array determines when an effect should run again.

**Example**

```jsx
useEffect(() => {
  console.log("Runs when count changes");
}, [count]);
```

**Key Points**

- No dependency array → runs after every render.
- `[]` → runs after the initial render in the usual client-side case.
- `[count]` → runs when `count` changes.
- Dependencies should reflect values used by the effect.

---

## 46. Cleanup Function

**Short Definition**

A cleanup function removes subscriptions, timers or event listeners created by an effect.

**Example**

```jsx
useEffect(() => {
  const id = setInterval(() => {
    console.log("Running");
  }, 1000);

  return () => clearInterval(id);
}, []);
```

**Key Points**

- Cleanup runs before an effect re-runs when dependencies change.
- Cleanup runs when the component unmounts.
- Prevents unwanted timers/listeners.
- Helps avoid resource leaks.

---

## 47. React Router DOM

**Short Definition**

React Router DOM is a library for client-side routing in React applications.

**Example**

```bash
npm install react-router-dom
```

```text
/          → Home
/about     → About
/contact   → Contact
```

**Key Points**

- Supports multiple routes in an SPA.
- Navigation can happen without a full page reload.
- Routes render different components.
- Common components include `BrowserRouter`, `Routes`, `Route`, `Link` and `Outlet`.

---

## 48. `BrowserRouter`

**Short Definition**

`BrowserRouter` provides routing context using the browser's history API.

**Example**

```jsx
<BrowserRouter>
  <App />
</BrowserRouter>
```

**Key Points**

- Usually wraps the application.
- Enables client-side routing.
- Works with `Routes` and `Route`.
- Keeps navigation inside the SPA.

---

## 49. `Routes` and `Route`

**Short Definition**

`Routes` contains route definitions, while `Route` connects a URL path to a component.

**Example**

```jsx
<Routes>
  <Route path="/" element={<Home />} />
  <Route path="/about" element={<About />} />
</Routes>
```

**Key Points**

- `path` defines the URL.
- `element` defines what should render.
- `Routes` groups route definitions.
- Only the matching route is rendered.

---

## 50. `Link`

**Short Definition**

`Link` provides client-side navigation without a traditional page reload.

**Example**

```jsx
<Link to="/about">About</Link>
```

**Key Points**

- Used instead of `<a>` for internal React routes.
- Prevents a full page reload.
- Updates the current route.
- Useful for navigation menus.

---

## 51. Dynamic Routing

**Short Definition**

Dynamic routing allows part of a URL to change based on data.

**Example**

```jsx
<Route path="/user/:id" element={<User />} />
```

```text
/user/101
/user/202
/user/303
```

**Key Points**

- `:id` is a dynamic parameter.
- Useful for users, products and posts.
- Different values can use the same component.
- Parameters are read using `useParams()`.

---

## 52. `useParams()`

**Short Definition**

`useParams()` reads dynamic parameters from the current URL.

**Example**

```jsx
const { id } = useParams();

return <h2>User ID: {id}</h2>;
```

**Key Points**

- Returns an object containing route parameters.
- `/user/101` gives `{ id: "101" }`.
- Parameters are strings.
- Multiple parameters can be destructured.

---

## 53. Multiple Route Parameters

**Short Definition**

A route can contain more than one dynamic parameter.

**Example**

```jsx
<Route path="/product/:category/:id" element={<Product />} />
```

```jsx
const { category, id } = useParams();
```

**Key Points**

- Multiple dynamic values can exist.
- Each parameter begins with `:`.
- `useParams()` returns all matched parameters.
- Useful for structured URLs.

---

## 54. Nested Routing

**Short Definition**

Nested routing means defining child routes inside a parent route.

**Example / Visual**

```text
/dashboard
    ├── profile
    └── settings
```

**Key Points**

- Useful for dashboards and layouts.
- Child routes belong to a parent route.
- Parent component usually contains `<Outlet />`.
- Keeps related routes organized.

---

## 55. `Outlet`

**Short Definition**

`Outlet` is the placeholder where a matched child route renders.

**Example**

```jsx
function Dashboard() {
  return (
    <>
      <h2>Dashboard</h2>
      <Outlet />
    </>
  );
}
```

**Key Points**

- Required in the parent component for child content to appear there.
- Child routes render inside `<Outlet />`.
- Useful for shared layouts.
- Common with nested routing.

---

## 56. `useNavigate()`

**Short Definition**

`useNavigate()` allows programmatic navigation from JavaScript.

**Example**

```jsx
const navigate = useNavigate();

navigate("/dashboard");
```

**Key Points**

- Useful after login, logout or form submission.
- Navigation happens programmatically.
- `navigate(-1)` can go back.
- Used inside React components.

---

## 57. Universal / 404 Route

**Short Definition**

A universal route handles URLs that do not match any defined route.

**Example**

```jsx
<Route path="*" element={<NotFound />} />
```

**Key Points**

- `*` catches unmatched routes.
- Used for 404 pages.
- Provides better user experience.
- Can provide a link back to Home.

---

## 58. `createBrowserRouter`

**Short Definition**

`createBrowserRouter` is an object-based routing approach available in modern React Router.

**Example**

```jsx
const router = createBrowserRouter([
  {
    path: "/",
    element: <Layout />,
    children: [
      { path: "home", element: <Home /> },
      { path: "about", element: <About /> },
    ],
  },
]);
```

**Key Points**

- Uses route objects.
- Supports nested routes naturally.
- Used with `RouterProvider`.
- Provides an alternative to `<BrowserRouter>` + `<Routes>`.

---

## 59. `NavLink`

**Short Definition**

`NavLink` is a special version of `Link` that provides active-route information.

**Example**

```jsx
<NavLink to="/home" className={({ isActive }) => (isActive ? "active" : "")}>
  Home
</NavLink>
```

**Key Points**

- Provides `isActive`.
- Useful for navigation bars.
- Makes active-link styling easier.
- Use when navigation needs active-state styling.

---

## 60. Context API

**Short Definition**

Context API allows data to be shared across components without manually passing props through every level.

**Example / Visual**

```text
Prop Drilling:

App
 ↓
Component A
 ↓
Component B
 ↓
Component C

Context:

Provider
   ↓
Consumer
```

**Key Points**

- Helps solve prop drilling.
- Useful for global/shared data.
- Common examples: authentication, theme and language.
- Avoid using it for every piece of application state.

---

## 61. Prop Drilling

**Short Definition**

Prop drilling is passing data through intermediate components that do not actually need the data.

**Example**

```text
App
 ↓ props
A
 ↓ props
B
 ↓ props
C
```

**Key Points**

- Makes deeply nested data flow harder to manage.
- Context can avoid unnecessary intermediate props.
- Props are still preferable for simple parent-child relationships.
- Context is useful when many components need the same data.

---

## 62. `createContext()`

**Short Definition**

`createContext()` creates a Context object used to share data.

**Example**

```jsx
const UserContext = createContext();
```

**Key Points**

- Creates the context.
- Context can hold shared values.
- Usually exported for use by providers and consumers.
- It is one of the core parts of Context API.

---

## 63. Context Provider

**Short Definition**

A Context Provider makes a value available to its descendant components.

**Example**

```jsx
<UserContext.Provider value="Anubhav">
  <Dashboard />
</UserContext.Provider>
```

**Key Points**

- `value` contains shared data.
- Child components can access the value.
- Provider defines the scope of the shared data.
- Multiple providers can be nested.

---

## 64. `useContext()`

**Short Definition**

`useContext()` reads the value from the nearest matching Context Provider.

**Example**

```jsx
const user = useContext(UserContext);

return <h1>Welcome, {user}</h1>;
```

**Key Points**

- No manual prop passing is required.
- Reads the nearest Provider's value.
- Makes shared data easier to access.
- Commonly used with custom providers.

---

## 65. Context with Object Data

**Short Definition**

Context can provide an object containing multiple related values.

**Example**

```jsx
<UserContext.Provider
  value={{
    name: "Anubhav",
    role: "Admin",
  }}
>
  <Dashboard />
</UserContext.Provider>
```

```jsx
const { name, role } = useContext(UserContext);
```

**Key Points**

- Context values can be objects.
- Destructuring makes access convenient.
- Functions, arrays and state can also be shared.
- Group related values when appropriate.

---

## 66. Context with State

**Short Definition**

Context can share both state and its updater function with descendant components.

**Example**

```jsx
const [user, setUser] = useState("Guest");

<UserContext.Provider value={{ user, setUser }}>
  <Profile />
</UserContext.Provider>;
```

**Key Points**

- Child can read the state.
- Child can call the updater.
- Useful for authentication-style data.
- Shared state can update all consuming components.

---

## 67. Custom Context Provider

**Short Definition**

A custom Provider component keeps Context logic separate and reusable.

**Example**

```jsx
export function UserProvider({ children }) {
  const [user, setUser] = useState("Guest");

  return (
    <UserContext.Provider value={{ user, setUser }}>
      {children}
    </UserContext.Provider>
  );
}
```

**Key Points**

- Keeps context logic organized.
- Uses `children` to render nested content.
- Can be reused across the application.
- Useful as an application grows.

---

## 68. Multiple Contexts

**Short Definition**

React allows multiple Context Providers to manage different types of shared data.

**Example**

```jsx
<ThemeContext.Provider value="dark">
  <UserContext.Provider value="Anubhav">
    <Dashboard />
  </UserContext.Provider>
</ThemeContext.Provider>
```

**Key Points**

- Each context can manage a separate concern.
- Theme and user data can have different contexts.
- Providers can be nested.
- Avoid creating unnecessary contexts.

---

## 69. Context API vs Props

**Short Definition**

Props are ideal for direct component communication, while Context is useful for shared data across many levels.

**Example**

| Props                            | Context                 |
| -------------------------------- | ----------------------- |
| Parent → Child                   | Provider → Descendants  |
| Explicit                         | Shared                  |
| Simple                           | Useful for global data  |
| Good for component-specific data | Good for app-level data |

**Key Points**

- Prefer props for simple relationships.
- Use Context when prop drilling becomes a problem.
- Context can cause consuming components to re-render when its value changes.
- Do not use Context simply because it is available.

---

# React Quick Revision Flow

```text
React
 │
 ├── Components
 │     └── Reusable UI
 │
 ├── JSX
 │     └── UI inside JavaScript
 │
 ├── Props
 │     └── Parent → Child
 │
 ├── State
 │     └── Dynamic data
 │
 ├── Events
 │     └── User interaction
 │
 ├── Hooks
 │     ├── useState
 │     ├── useEffect
 │     └── useContext
 │
 ├── Forms
 │     └── Controlled Components
 │
 ├── API
 │     └── Fetch / Axios
 │
 ├── Routing
 │     ├── Routes
 │     ├── Link
 │     ├── useParams
 │     ├── useNavigate
 │     └── Outlet
 │
 └── Context
       └── Shared application data
```

# One-Line Revision

| Concept              | Remember                         |
| -------------------- | -------------------------------- |
| React                | UI library                       |
| Component            | Reusable UI                      |
| JSX                  | JavaScript + HTML-like syntax    |
| Props                | Parent → Child data              |
| State                | Component's changing data        |
| Event                | User interaction                 |
| `useState`           | Manage state                     |
| `useEffect`          | Side effects                     |
| Controlled Component | State-controlled input           |
| Local Storage        | Persistent browser data          |
| Axios                | HTTP client                      |
| CSR                  | Browser renders UI               |
| SSR                  | Server renders initial HTML      |
| Router               | Client-side navigation           |
| `useParams`          | Read URL parameters              |
| `useNavigate`        | Programmatic navigation          |
| `Outlet`             | Render nested route              |
| Context              | Share data without prop drilling |
| `useContext`         | Read context value               |
