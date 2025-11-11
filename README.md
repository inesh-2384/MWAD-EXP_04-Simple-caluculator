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
import React, { useState } from "react";

export default function App() {
  const [input, setInput] = useState("");

  const handleClick = (value) => {
    setInput((prev) => prev + value);
  };

  const handleClear = () => {
    setInput("");
  };

  const handleEvaluate = () => {
    try {
      const result = eval(input);
      setInput(String(result));
    } catch {
      setInput("Error");
    }
  };

  const buttons = [
    ["7", "8", "9", "/"],
    ["4", "5", "6", "x"],
    ["1", "2", "3", "-"],
    ["0", ".", "=", "+"]
  ];

  return (
    <div style={{
      display: 'flex',
      justifyContent: 'center',
      alignItems: 'center',
      minHeight: '100vh',
      background: 'linear-gradient(135deg, #a1c4fd, #c2e9fb)',
    }}>
      <h1 style={{
        position: 'absolute',
        top: '20px',
        left: '20px',
        fontSize: '24px',
        color: '#1e3a8a',
        fontFamily: 'monospace'
      }}>
        Simple Calculator
      </h1>
      <div style={{
        backdropFilter: 'blur(12px)',
        backgroundColor: 'rgba(255, 255, 255, 0.35)',
        borderRadius: '20px',
        padding: '24px',
        width: '320px',
        boxShadow: '0 8px 32px rgba(0, 0, 0, 0.25)'
      }}>
        <div style={{
          backgroundColor: 'rgba(255, 255, 255, 0.4)',
          textAlign: 'right',
          fontSize: '26px',
          padding: '16px',
          borderRadius: '12px',
          fontFamily: 'monospace',
          marginBottom: '24px',
          color: '#0f172a'
        }}>
          {input || "0"}
        </div>
        <div style={{
          display: 'grid',
          gridTemplateColumns: 'repeat(4, 1fr)',
          gap: '12px'
        }}>
          {buttons.flat().map((btn, idx) => (
            <button
              key={idx}
              onClick={() => btn === "=" ? handleEvaluate() : handleClick(btn)}
              style={{
                padding: '18px',
                fontSize: '18px',
                borderRadius: '10px',
                backgroundColor: 'rgba(173, 216, 230, 0.7)',
                border: 'none',
                boxShadow: '2px 2px 6px rgba(0,0,0,0.1)',
                cursor: 'pointer',
                transition: '0.2s ease',
                color: '#1e3a8a'
              }}
            >
              {btn}
            </button>
          ))}
          <button
            onClick={handleClear}
            style={{
              gridColumn: 'span 4',
              marginTop: '12px',
              padding: '16px',
              fontSize: '18px',
              borderRadius: '10px',
              backgroundColor: '#3b82f6',
              color: 'white',
              border: 'none',
              cursor: 'pointer',
              boxShadow: '2px 2px 8px rgba(0,0,0,0.15)'
            }}
          >
            Clear
          </button>
        </div>
      </div>
    </div>
  );
}

```

## OUTPUT
![image](https://github.com/user-attachments/assets/e12d7483-5cb1-4b54-8f78-5a1bfd64a4f4)


## RESULT
The program for developing a simple calculator in React.js is executed successfully.
