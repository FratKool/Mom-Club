
<!DOCTYPE html>
<html>
<head>
  <title>Math Multiplication Example</title>
  <style>
    body {
      font-family: sans-serif;
    }
    #container {
      width: 500px;
      margin: 20px auto;
      padding: 20px;
      border: 1px solid #ccc;
      border-radius: 5px;
    }
    label {
      display: block;
      margin-bottom: 5px;
    }
    input[type="number"] {
      width: 100%;
      padding: 8px;
      margin-bottom: 10px;
      border: 1px solid #ddd;
      border-radius: 4px;
      box-sizing: border-box; /* Important for padding to be included in width */
    }
    button {
      background-color: #4CAF50;
      color: white;
      padding: 10px 15px;
      border: none;
      border-radius: 4px;
      cursor: pointer;
    }
    #result {
      margin-top: 15px;
      font-weight: bold;
    }
  </style>
</head>
<body>

  <div id="container">
    <h1>Multiplication Calculator</h1>

    <label for="num1">Enter the first number:</label>
    <input type="number" id="num1" name="num1">

    <label for="num2">Enter the second number:</label>
    <input type="number" id="num2" name="num2">

    <button onclick="multiply()">Calculate</button>

    <div id="result"></div>
  </div>

  <script>
    function multiply() {
      var number1 = document.getElementById("num1").value;
      var number2 = document.getElementById("num2").value;

      // Check if the inputs are valid numbers
      if (isNaN(number1) || isNaN(number2)) {
        document.getElementById("result").innerHTML = "Please enter valid numbers.";
        return; // Exit the function
      }

      // Convert the input strings to numbers (important!)
      number1 = parseFloat(number1);
      number2 = parseFloat(number2);

      var product = number1 * number2;

      document.getElementById("result").innerHTML = "The product is: " + product;
    }
  </script>

</body>
</html>
