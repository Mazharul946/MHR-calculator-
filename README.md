# MHR-calculator-
Mhr calculator 
<!DOCTYPE html>
<html>
  <head>
    <title>MHR Calculator</title>
    <style>
      /* CSS for calculator layout */
      #calculator {
        width: 300px;
        margin: 0 auto;
        background-color: #0cbed8;
        border: 1px solid #ccc;
        border-radius: 5px;
        padding: 20px;
      }

      #calculator h2 {
        text-align: center;
        font-size: 24px;
        margin-bottom: 20px;
      }

      #calculator input[type="button"] {
        width: 64px;
        height: 64px;
        font-size: 24px;
        margin: 5px;
        border: 1px solid #ccc;
        background-color: #fff;
        border-radius: 5px;
        cursor: pointer;
      }

      #calculator input[type="text"] {
        width: 100%;
        height: 50px;
        font-size: 24px;
        text-align: right;
        margin-bottom: 10px;
        padding: 5px;
      }

      #calculator input[type="button"]:hover {
        background-color: #ddd;
      }

      #calculator .row {
        display: flex;
        justify-content: space-between;
      }
    </style>
  </head>
  <body>
    <div id="calculator">
      <h2>MHR Calculator</h2>
      <input type="text" id="result" readonly />
      <div class="row">
        <input type="button" value="1" onclick="insert('1')" />
        <input type="button" value="2" onclick="insert('2')" />
        <input type="button" value="3" onclick="insert('3')" />
        <input type="button" value="/" onclick="insert('/')" />
      </div>
      <div class="row">
        <input type="button" value="4" onclick="insert('4')" />
        <input type="button" value="5" onclick="insert('5')" />
        <input type="button" value="6" onclick="insert('6')" />
        <input type="button" value="*" onclick="insert('*')" />
      </div>
      <div class="row">
        <input type="button" value="7" onclick="insert('7')" />
        <input type="button" value="8" onclick="insert('8')" />
        <input type="button" value="9" onclick="insert('9')" />
        <input type="button" value="-" onclick="insert('-')" />
      </div>
      <div class="row">
        <input type="button" value="0" onclick="insert('0')" />
        <input type="button" value="." onclick="insert('.')" />
        <input type="button" value="C" onclick="clearResult()" />
        <input type="button" value="+" onclick="insert('+')" />
      </div>
      <div class="row">
        <input type="button" value="=" onclick="calculate()" />
      </div>
    </div>
    <script>
      // JavaScript for calculator functions
      function insert(num) {
        document.getElementById("result").value += num;
      }

      function clearResult() {
        document.getElementById("result").value = "";
      }

      function calculate() {
        var result = document.getElementById("result").value;
        var output = eval(result);
        document.getElementById("result").value = output;
      }
    </script>
 
