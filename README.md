# Calculator
This code is used to create a simple calculator that using HTML combine with CSS and JavaScript.
<!DOCTYPE html>
<html lang="en">
<head>
    <h1>Here is a sample <strong>Calculator</strong>.</h1>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculator</title>
    <style>
        /* Add CSS styles for the calculator here */
        body {
            font-family: Arial, sans-serif;
            background-color: #faa5a5;
            text-align: center;
        }
        .calculator {
            width: 300px;
            margin: 0 auto;
            background-color: #dba3a3;
            border-radius: 5px;
            box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.2);
            padding: 20px;
        }
        input[type="text"] {
            width: 100%;
            font-size: 24px;
            padding: 10px;
            margin-bottom: 10px;
        }
        .button {
            width: 50px;
            height: 50px;
            font-size: 18px;
            margin: 5px;
            cursor: pointer;
            border: 1px solid #ccc;
            background-color: #eee;
            border-radius: 5px;
        }
        .button:hover {
            background-color: #ddd;
        }
    </style>
</head>
<body>
    <div class="calculator">
        <input type="text" id="display" readonly>
       
        <div>
            <div style="text-align: left;">
                <button class="button" onclick="clearDisplay()">C</button>
            </div>
        </div>
        
        <div>
            <button class="button" onclick="appendToDisplay('7')">7</button>
            <button class="button" onclick="appendToDisplay('8')">8</button>
            <button class="button" onclick="appendToDisplay('9')">9</button>
            <button class="button" onclick="appendToDisplay('+')">+</button>
        </div>
        <div>
            <button class="button" onclick="appendToDisplay('4')">4</button>
            <button class="button" onclick="appendToDisplay('5')">5</button>
            <button class="button" onclick="appendToDisplay('6')">6</button>
            <button class="button" onclick="appendToDisplay('-')">-</button>
        </div>
        <div>
            <button class="button" onclick="appendToDisplay('1')">1</button>
            <button class="button" onclick="appendToDisplay('2')">2</button>
            <button class="button" onclick="appendToDisplay('3')">3</button>
            <button class="button" onclick="appendToDisplay('*')">*</button>
        </div>
        <div>
            <button class="button" onclick="appendToDisplay('0')">0</button>
            <button class="button" onclick="appendToDisplay('.')">.</button>
            <button class="button" onclick="calculateResult()">=</button>
            <button class="button" onclick="appendToDisplay('/')">/</button>
        </div>
    </div>

    <script>
        // JavaScript functions for the calculator
        function appendToDisplay(value) {
            document.getElementById("display").value += value;
        }

        function clearDisplay() {
            document.getElementById("display").value = "";
        }

        function calculateResult() {
            try {
                const expression = document.getElementById("display").value;
                const result = eval(expression);
                document.getElementById("display").value = result;
            } catch (error) {
                document.getElementById("display").value = "Error";
            }
        }
    </script>
</body>
</html>
