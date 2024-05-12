# Ex.08 Design of a Standard Calculator
## Date:

## AIM:
To design a web application for a standard calculator with minimum five operations.

## DESIGN STEPS:

### Step 1:
Clone the github repository and create Django admin interface.

### Step 2:
Change settings.py file to allow request from all hosts.

### Step 3:
Use CSS for creating attractive colors.

### Step 4:
Write JavaScript program for implementing five different operations.

### Step 5:
Validate the HTML and CSS code.

### Step 6:
Publish the website in the given URL.

## PROGRAM :
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Simple Calculator</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            background-color: #f52f39;
            font-family: Arial, sans-serif;
        }

        .calculator {
            width: 300px;
            padding: 20px;
            background-color: #a8c541;
            box-shadow: 0 5px 10px rgba(0, 0, 0, 0.1);
            border-radius: 8px;
        }

        #display {
            width: 100%;
            height: 50px;
            border: 2px solid #169ace;
            margin-bottom: 10px;
            font-size: 24px;
            padding: 10px;
            box-sizing: border-box;
            text-align: right;
            border-radius: 5px;
        }

        .buttons {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 10px;
        }

        button {
            background-color: #e641b4;
            border: none;
            padding: 15px;
            border-radius: 10px;
            font-size: 18px;
            cursor: pointer;
            transition: background-color 0.1s;
        }

        button:hover {
            background-color: #b0aaeb;
        }

        button:active {
           
            background-color: #24e063;
      
        }

        .equals {
            grid-column: span 4;
        }
    </style>
</head>
<body>
   
    <div class="calculator">
        <h1>DILIP SANJAY M(212223240032)</h1>
        <input type="text" style="background-color: #e8ece9;"  id="display" >
        <div class="buttons">
            <button onclick="clearDisplay()" style="background-color: rgb(232, 144, 12);">C</button>
            <button onclick="inputValue('/')">/</button>
            <button onclick="inputValue('*')">*</button>
            <button onclick="inputValue('.')">.</button>
            <button onclick="inputValue()">(</button>
            <button onclick="inputValue()">)</button>
            <button onclick="inputValue('%')">%</button>
            <button onclick="inputValue('^')">^</button>
            <button onclick="inputValue('7')">7</button>
            <button onclick="inputValue('8')">8</button>
            <button onclick="inputValue('9')">9</button>
            <button onclick="inputValue('-')">-</button>
            <button onclick="inputValue('4')">4</button>
            <button onclick="inputValue('5')">5</button>
            <button onclick="inputValue('6')">6</button>
            <button onclick="inputValue('+')">+</button>
            <button onclick="inputValue('1')">1</button>
            <button onclick="inputValue('2')">2</button>
            <button onclick="inputValue('3')">3</button>
            <button onclick="inputValue('0')">0</button>
            <button onclick="calculateResult()" class="equals" style="background-color: burlywood;">=</button>
            
            
        </div>
    </div>
    <script>
        const display = document.getElementById('display');

        function inputValue(value) {
            display.value += value;
        }

        function clearDisplay() {
            display.value = '';
        }

        function calculateResult() {
            try {
                // eval can be dangerous if you are working with user input on sensitive data/systems.
                display.value = eval(display.value).toString();
            } catch (error) {
                display.value = 'Error';
                setTimeout(clearDisplay, 20000); // Clear after 2 seconds
            }
        }
    </script>
</body>
</html>
```
## OUTPUT:
![image](https://github.com/dilipsanjay/Calc/assets/155506948/80ce53eb-48d0-4160-996d-1e3739c454b3)
![image](https://github.com/dilipsanjay/Calc/assets/155506948/7e86565e-740d-4fa7-ad16-f397fbccbad0)


## RESULT:
The program for designing a standard calculator using HTML and CSS is executed successfully.
