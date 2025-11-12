# Ex04 Simple Calculator - React Project
## NAME : NAVEEN KUMAR T
## REG NO : 212223220067
## Date: 12:11:2025

## AIM:
To  develop a Simple Calculator using React.js with clean and responsive design, ensuring a smooth user experience across different screen sizes.

## ALGORITHM:
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

## PROGRAM :
Calculator.js
```
import React, { useState } from "react";
import "./Calculator.css";

const Calculator = () => {
  const [input, setInput] = useState("");

  const handleClick = (value) => setInput(input + value);
  const handleClear = () => setInput("");
  const handleEqual = () => {
    try {
      setInput(eval(input).toString());
    } catch {
      setInput("Error");
    }
  };

  return (
    <div className="calculator">
      <input type="text" value={input} readOnly className="display" />
      <div className="buttons">
        <button onClick={handleClear}>C</button>
        {[7, 8, 9, "/", 4, 5, 6, "*", 1, 2, 3, "-", 0, ".", "+", "="].map(
          (val, i) =>
            val === "=" ? (
              <button key={i} onClick={handleEqual}>
                {val}
              </button>
            ) : (
              <button key={i} onClick={() => handleClick(val)}>
                {val}
              </button>
            )
        )}
      </div>
    </div>
  );
};

export default Calculator;
```

App.jsx
```
import React from "react";
import Calculator from "./Calculator";
import "./App.css"

function App() {
  return (
    <div>
      <h1 style={{ textAlign: "center" }}>Simple Calculator</h1>
            <h1 style={{ textAlign: "center" }}>done by - Naveen Kumar T</h1>

      <Calculator />
    </div>
  );
}

export default App
```

Calculator.css
```
.calculator {
  width: 250px;
  margin: 100px auto;
  padding: 15px;
  background: #ffffff3b;
  border-radius: 10px;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
}

.display {
  width: 100%;
  height: 40px;
  margin-bottom: 10px;
  text-align: right;
  font-size: 1.2em;
  padding-right: 10px;
}

.buttons {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 10px;
}

button {
  height: 50px;
  font-size: 1.1em;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  background: #a3a132;
}

button:hover {
  background: #790a0a;
}
```

Calculator.jsx
```
import React, { useState } from "react";
import "./Calculator.css";

const Calculator = () => {
  const [input, setInput] = useState("");

  const handleClick = (value) => setInput(input + value);
  const handleClear = () => setInput("");
  const handleEqual = () => {
    try {
      setInput(eval(input).toString());
    } catch {
      setInput("Error");
    }
  };

  return (
    <div className="calculator">
      <input type="text" value={input} readOnly className="display" />
      <div className="buttons">
        <button onClick={handleClear}>C</button>
        {[7, 8, 9, "/", 4, 5, 6, "*", 1, 2, 3, "-", 0, ".", "+", "="].map(
          (val, i) =>
            val === "=" ? (
              <button key={i} onClick={handleEqual}>
                {val}
              </button>
            ) : (
              <button key={i} onClick={() => handleClick(val)}>
                {val}
              </button>
            )
        )}
      </div>
    </div>
  );
};

export default Calculator;
```
Calculator.css
```
.calculator {
  width: 250px;
  margin: 100px auto;
  padding: 15px;
  background: #f4f4f4;
  border-radius: 10px;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
}

.display {
  width: 100%;
  height: 40px;
  margin-bottom: 10px;
  text-align: right;
  font-size: 1.2em;
  padding-right: 10px;
}

.buttons {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 10px;
}

button {
  height: 50px;
  font-size: 1.1em;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  background: #dcdcdc;
}

button:hover {
  background: #bbb;
}
```

## OUTPUT:
<img width="1920" height="1080" alt="Screenshot (103)" src="https://github.com/user-attachments/assets/ef4b0ad6-5461-4933-a081-834ca6afea76" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/80543b57-d6a8-4be1-bc71-03ba9d59f02f" />

## RESULT
The program for developing a simple calculator in React.js is executed successfully.
