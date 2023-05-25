---
title: Calculator task
description: This is a post based on my TCG Bootcamp experience
date: 2023-05-06
tags:
  - Bootcamp Challenges
---

<body>
    <h3 Task: Calculator></h3>
    We need to create a function capable of using the addition, subtraction, multiply, divider or modulus operator on 2 numbers provided.
    <br>1. Create a function named calculator
    <br>2. Add 3 arguments for “number1”, “number2” and “operator”
    <br>3. Use a switch statement to determine which operator to use
    <br>4. Add the math code for each operator in the case statement to return the value
    <br>5. Console.log a message “{number1} {operator} {number2} = {value}”
</body>

<br>Code:

```diff-js
// Calculator

// Get required values from user
const number1 = Number(prompt("Enter the first operand:"));
const number2 = Number(prompt("Enter the second operand:"));
const operator = prompt("Enter the mathematical operator (+, -, *, /, or %):");
            
console.log(number1 + operator + number2 +  "=" + calculator(number1, number2, operator));
document.write(number1 + operator + number2 +  "=" + calculator(number1, number2, operator));

function calculator(number1, number2, operator) {
    switch (operator) {
        case "+":
            return (number1 + number2);
        case "-":
            return (number1 - number2);
        case "*":
            return (number1 * number2);
        case "%":
            return (number1 % number2);
        case "/":
            if (number2 == 0) {
                console.log("Error: Division by zero");
                return (0);
            }
            else {
                return (number1 / number2);
            }

        default:
            console.log("Invalid operation");
            return (0);
    }

} 
```

<script>
// Calculator

// Get required values from user
const number1 = Number(prompt("Enter the first operand:"));
const number2 = Number(prompt("Enter the second operand:"));
const operator = prompt("Enter the mathematical operator (+, -, *, /, or %):");
            
console.log(number1 + operator + number2 +  "=" + calculator(number1, number2, operator));
document.write(number1 + operator + number2 +  "=" + calculator(number1, number2, operator));

function calculator(number1, number2, operator) {
    switch (operator) {
        case "+":
            return (number1 + number2);
        case "-":
            return (number1 - number2);
        case "*":
            return (number1 * number2);
        case "%":
            return (number1 % number2);
        case "/":
            if (number2 == 0) {
                console.log("Error: Division by zero");
                return (0);
            }
            else {
                return (number1 / number2);
            }

        default:
            console.log("Invalid operation");
            return (0);
    }

} 
</script>