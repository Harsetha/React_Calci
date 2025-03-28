# Ex04 Simple Calculator - React Project
## Date:

## AIM
To  develop a Simple Calculator using React.js with clean and responsive design, ensuring a smooth user experience across different screen sizes.

## ALGORITHM
### STEP 1
Create a React App.

### STEP 2
Open a terminal and run:
  <ul><li>npx create-react-app simple-calculator</li>
  <li>cd simple-calculator</li>
  <li>npm start</li></ul>

### STEP 3
Inside the src/ folder, create a new file Calculator.js and define the basic structure.

### STEP 4
Plan the UI: Display screen, number buttons (0-9), operators (+, -, *, /), clear (C), and equal (=).

### STEP 5
Create a new file Calculator.css in src/ and add the styling.

### STEP 6
Open src/App.js and modify it.

### STEP 7
Start the development server.
  npm start

### STEP 8
Open http://localhost:3000/ in the browser.

### STEP 9
Test the calculator by entering numbers and operations.

### STEP 10
Fix styling issues and refine content placement.

### STEP 11
Deploy the website.

### STEP 12
Upload to GitHub Pages for free hosting.

## PROGRAM
```
app.js

import React, { useState } from "react";
import "./App.css";

const App = () => {
  const [input, setInput] = useState("");
  const [result, setResult] = useState("");

  const handleClick = (value) => {
    if (value === "=") {
      try {
        setResult((input)); // Use eval carefully
      } catch {
        setResult("Error");
      }
    } else if (value === "C") {
      setInput("");
      setResult("");
    } else {
      setInput(input + value);
    }
  };

  return (
    <div className="calculator">
      <div className="display">
        <div className="input">{input}</div>
        <div className="result">{result}</div>
      </div>
      <div className="buttons">
        {["C", "/", "*", "-", "7", "8", "9", "+", "4", "5", "6", "1", "2", "3", "0", ".", "="].map((btn) => (
          <button key={btn} onClick={() => handleClick(btn)}>
            {btn}
          </button>
        ))}
      </div>
       <footer className="footer">
        <p>HARSETHA J 212223220032</p>
      </footer>
    </div>
  );
};

export default App;
```
```
app.css
body {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  background-color: #4a5a7a;
  margin: 0;
  font-family: Arial, sans-serif;
}

.calculator {
  width: 300px;
  background: #2c3b4f;
  border-radius: 10px;
  padding: 20px;
  box-shadow: 0 4px 10px rgba(204, 4, 114, 0.2);
}

.display {
  background: #121a26;
  color: white;
  font-size: 1.5rem;
  padding: 10px;
  text-align: right;
  border-radius: 5px;
  margin-bottom: 10px;
}

.result {
  font-size: 1.2rem;
  color: #4af;
}

.buttons {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 10px;
}

button {
  background: #b5d0ea;
  color: #4af;
  border: none;
  padding: 15px;
  font-size: 1.2rem;
  cursor: pointer;
  border-radius: 5px;
}

button:hover {
  background: #f279de;
}

button:active {
  background: rgb(72, 146, 207);
  color: white;
}
```
```
index.js

import React from 'react';
import ReactDOM from 'react-dom/client';
import './index.css';
import App from './App';

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(
  <React.StrictMode>
    <App />
  </React.StrictMode>
);
```

## OUTPUT

![Screenshot (192)](https://github.com/user-attachments/assets/f62b9baf-c051-4d09-b548-e83888f2d8dd)

![Screenshot (193)](https://github.com/user-attachments/assets/9b59cdaf-cb57-4922-a892-e0b3111444b5)

## RESULT
The program for developing a simple calculator in React.js is executed successfully.
