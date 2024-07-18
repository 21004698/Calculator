# Calculator
Aim:Design a Webpage using JavaScript eith a minimum of five mathematical operations.
program :
```
<!DOCTYPE html>
<html lang="en">
  <head>
    
    <title>Calculator</title>
    <style>
        * {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: "Poppins", sans-serif;
}
body {
  
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  background: whitesmoke;
}

.container {
  position: relative;
  max-width: 500px;
  width: 100%;
  border-radius: 12px;
  padding: 10px 20px 20px;
  background: #fff;
  box-shadow: 0 5px 10px yellowgreen;
}
.display {
  height: 60px;
  width: 100%;
  outline: none;
  border: none;
  text-align: right;
  margin-bottom: 10px;
  font-size: 25px;
  color: #000e1a;
  pointer-events: none;
}
.buttons {
  display: grid;
  grid-gap: 15px;
  grid-template-columns: repeat(4, 1fr);
}
.buttons button {
  padding: 10px;
  border-radius: 6px;
  border: none;
  font-size: 20px;
  cursor: pointer;
  background-color: rgb(0, 242, 255);
}
.buttons button:active {
  transform: scale(0.99);
}
.operator {
  color:red;
}
    </style>

  </head>
  <body>
    <div>
        <div>        <h2 align="center">Challa Maheswar (212221040031)</h2>
        </div>
        <div class="container" style="background-color: #000e1a;">
      
      
      <input type="text" class="display" />

      <div class="buttons">
        <button class="operator" data-value="AC">AC</button>
        <button class="operator" data-value="DEL" id="back"><i class="bi bi-backspace-fill"></i></button>
        <button class="operator" data-value="%">%</button>
        <button class="operator" data-value="/">/</button>

        <button data-value="7">7</button>
        <button data-value="8">8</button>
        <button data-value="9">9</button>
        <button class="operator" data-value="*">*</button>

        <button data-value="4">4</button>
        <button data-value="5">5</button>
        <button data-value="6">6</button>
        <button class="operator" data-value="-">-</button>

        <button data-value="1">1</button>
        <button data-value="2">2</button>
        <button data-value="3">3</button>
        <button class="operator" data-value="+">+</button>

        <button data-value="00">00</button>
        <button data-value="0">0</button>
        <button data-value=".">.</button>
        <button class="operator" data-value="=">=</button>
      </div>
    </div>
    </div>

    <script>
        const display = document.querySelector(".display");
const buttons = document.querySelectorAll("button");
const specialChars = ["%", "*", "/", "-", "+", "="];
let output = "";

const calculate = (btnValue) => {
  display.focus();
  if (btnValue === "=" && output !== "") {
    output = eval(output.replace("%", "/100"));
  } else if (btnValue === "AC") {
    output = "";
  } else if (btnValue === "DEL") {
    output = output.toString().slice(0, -1);
  } else {
    if (output === "" && specialChars.includes(btnValue)) return;
    output += btnValue;
  }
  display.value = output;
};

buttons.forEach((button) => {
  button.addEventListener("click", (e) => calculate(e.target.dataset.value));
});
    </script>
  </body>
</html>
``` 
Out put:
![Assignment -5 output](https://github.com/user-attachments/assets/14c2f2a6-c7f0-43eb-8585-78e69ac0ae6c)



Result:
Design a Webpage using JavaScript eith a minimum of five mathematical operationswas executed successfully.
