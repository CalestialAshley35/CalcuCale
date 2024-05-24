### CalcuCale

CalcuCale is a simple, web-based calculator application built with HTML, CSS, and JavaScript. This project provides a straightforward and interactive interface for basic arithmetic calculations.

#### Features

- **Responsive Design**: The calculator is styled to be user-friendly and works seamlessly across various device sizes.
- **Basic Arithmetic Operations**: Supports addition, subtraction, multiplication, and division.
- **Error Handling**: Displays an error message for invalid inputs or calculations.

#### Project Structure

- **HTML**: Defines the structure of the calculator, including the display and buttons for digits and operations.
- **CSS**: Provides styling for the calculator, including layout, button styles, and hover effects.
- **JavaScript**: Implements the functionality of the calculator, handling input, operations, and error handling.

#### Usage

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/CalcuCale.git
   ```
2. Navigate to the project directory:
   ```bash
   cd CalcuCale
   ```
3. Open the `index.html` file in your web browser to use the calculator.

#### Code Breakdown

- **HTML**: Defines the calculator layout and includes links to the CSS and JavaScript files.
- **CSS**:
  - `.calculator`: Styles the main container of the calculator.
  - `#display`: Styles the input display.
  - `.buttons button`: Styles the calculator buttons and includes hover effects.
- **JavaScript**:
  - `clearDisplay()`: Clears the display.
  - `appendValue(value)`: Appends a value to the display.
  - `calculate()`: Evaluates the expression in the display and shows the result.

Feel free to fork the repository and contribute to enhancing the CalcuCale project!

#### Example Code

**HTML:**
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CalcuCale</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="calculator">
        <input type="text" id="display" disabled>
        <div class="buttons">
            <button onclick="clearDisplay()">C</button>
            <button onclick="appendValue('7')">7</button>
            <button onclick="appendValue('8')">8</button>
            <button onclick="appendValue('9')">9</button>
            <button onclick="appendValue('+')">+</button>
            <button onclick="appendValue('4')">4</button>
            <button onclick="appendValue('5')">5</button>
            <button onclick="appendValue('6')">6</button>
            <button onclick="appendValue('-')">-</button>
            <button onclick="appendValue('1')">1</button>
            <button onclick="appendValue('2')">2</button>
            <button onclick="appendValue('3')">3</button>
            <button onclick="appendValue('*')">*</button>
            <button onclick="appendValue('0')">0</button>
            <button onclick="appendValue('.')">.</button>
            <button onclick="calculate()">=</button>
            <button onclick="appendValue('/')">/</button>
        </div>
    </div>
    <script src="script.js"></script>
</body>
</html>
```

**CSS:**
```css
.calculator {
    width: 200px;
    margin: 100px auto;
    padding: 20px;
    border: 2px solid #ccc;
    border-radius: 10px;
    text-align: center;
}

#display {
    width: 100%;
    margin-bottom: 10px;
    padding: 10px;
    font-size: 18px;
}

.buttons button {
    width: 40px;
    height: 40px;
    margin: 5px;
    font-size: 18px;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    background-color: #f0f0f0;
}

.buttons button:hover {
    background-color: #ccc;
}
```

**JavaScript:**
```javascript
function clearDisplay() {
    document.getElementById('display').value = '';
}

function appendValue(value) {
    document.getElementById('display').value += value;
}

function calculate() {
    try {
        var result = eval(document.getElementById('display').value);
        document.getElementById('display').value = result;
    } catch (error) {
        document.getElementById('display').value = 'Error';
    }
}
```

Enjoy using CalcuCale for your basic calculation needs!
