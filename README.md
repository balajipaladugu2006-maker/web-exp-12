## Exp 12 - Simple Single Page Application (SPA) using React
## NAME: Paladugu Venkata Balaji
## REG NO: 2305001024
## Aim
To develop a simple Single Page Application (SPA) using React JS with Home, About, and Contact pages and navigate between them using the useState hook.

## Objectives
1. To understand the concept of Single Page Applications.
2. To create reusable components in React.
3. To use the useState hook for managing state.
4. To implement navigation between different pages without reloading the browser.
5. To apply CSS styling to the React application.
# Program
## 1. App.jsx
~~~python
import { useState } from "react";
import "./App.css";

function Home() {
  return (
    <div>
      <h2>Home Page</h2>
      <p>Welcome to BALAJI's React SPA!</p>
    </div>
  );
}

function About() {
  return (
    <div>
      <h2>About Page</h2>
      <p>This is a simple Single Page Application.</p>
    </div>
  );
}

function Contact() {
  return (
    <div>
      <h2>Contact Page</h2>
      <p>Email: balaji@example.com</p>
    </div>
  );
}

function App() {
  const [page, setPage] = useState("home");

  return (
    <div className="app">
      <h1>Simple React SPA</h1>

      <nav>
        <button onClick={() => setPage("home")}>Home</button>
        <button onClick={() => setPage("about")}>About</button>
        <button onClick={() => setPage("contact")}>Contact</button>
      </nav>

      <hr />

      {page === "home" && <Home />}
      {page === "about" && <About />}
      {page === "contact" && <Contact />}
    </div>
  );
}

export default App;
~~~
## 2. App.css
~~~
.app {
  text-align: center;
  padding: 30px;
}

nav {
  margin: 20px;
}

button {
  margin: 5px;
  padding: 10px 20px;
  cursor: pointer;
  background-color: blue;
  color: white;
  border: none;
  border-radius: 5px;
}

button:hover {
  background-color: darkblue;
}
~~~ 
## 3. index.css
~~~
body {
  font-family: Arial, sans-serif;
  text-align: center;
  background-color: #f2f2f2;
}

h1 {
  color: darkblue;
}

h2 {
  color: darkgreen;
}
~~~
## 4. main.jsx
~~~python
import React from "react";
import ReactDOM from "react-dom/client";
import App from "./App.jsx";
import "./index.css";

ReactDOM.createRoot(document.getElementById("root")).render(
  <React.StrictMode>
    <App />
  </React.StrictMode>
);
~~~
## Output
<img width="1470" height="686" alt="image" src="https://github.com/user-attachments/assets/21196954-7f74-4356-8720-7dd6facf8afd" />
<img width="1001" height="462" alt="image" src="https://github.com/user-attachments/assets/5da8285e-145d-49e3-9fe3-06a906f6dc86" />
<img width="1442" height="713" alt="image" src="https://github.com/user-attachments/assets/136baad0-5f2f-4a6a-bf00-fc258c0c6fa0" />



## Result
Thus, a simple Single Page Application was successfully developed using React JS with Home, About, and Contact pages. Navigation between the pages was implemented using the useState hook without reloading the browser.
