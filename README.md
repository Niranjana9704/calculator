<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=, initial-scale=1.0">
    <title>CALCULATOR</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f0f0f0;
        }
        .calculator {
            width: 350px;
            margin: 50px auto;
            background-color: #fff;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        input[type="button"] {
            width: 70px;
            height: 50px;
            margin: 5px;
            font-size: 20px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        input[type="text"] {
            width: 100%;
            height: 50px;
            margin-bottom: 10px;
            font-size: 24px;
            text-align: right;
            padding: 0 10px;
            border: 1px solid #ccc;
            border-radius: 5px;
            box-sizing: border-box;
        }
    </style>

</head>
    <body>
        <div class="calculator">
            <input type="text" id="display" readonly>
            <input type="button" value="1" onclick="appendToDisplay('1')">
            <input type="button" value="2" onclick="appendToDisplay('2')">
            <input type="button" value="3" onclick="appendToDisplay('3')">
            <input type="button" value="+" onclick="appendToDisplay('+')">
            <br>
            <input type="button" value="4" onclick="appendToDisplay('4')">
            <input type="button" value="5" onclick="appendToDisplay('5')">
            <input type="button" value="6" onclick="appendToDisplay('6')">
            <input type="button" value="-" onclick="appendToDisplay('-')">
            <br>
            <input type="button" value="7" onclick="appendToDisplay('7')">
            <input type="button" value="8" onclick="appendToDisplay('8')">
            <input type="button" value="9" onclick="appendToDisplay('9')">
            <input type="button" value="*" onclick="appendToDisplay('*')">
            <br>
            <input type="button" value="C" onclick="clearDisplay()">
            <input type="button" value="0" onclick="appendToDisplay('0')">
            <input type="button" value="=" onclick="calculate()">
            <input type="button" value="/" onclick="appendToDisplay('/')">
        </div>
        <script>
            function appendToDisplay(value) {
                document.getElementById('display').value += value;
            }
    
            function clearDisplay() {
                document.getElementById('display').value = '';
            }
    
            function calculate() {
                try {
                    document.getElementById('display').value = eval(document.getElementById('display').value);
                } catch (error) {
                    document.getElementById('display').value = 'Error';
                }
            }
        </script>
    </body>
</html>
