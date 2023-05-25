---
title: Percentage Calculator
description: This is a post based on my TCG Bootcamp experience
date: 2023-05-03
tags:
  - Bootcamp Challenges
---

<body>
    <h3 Task: Percentage Calculator></h3>
    Create a function that is able to return a percentage of a number. For example you want to know what 30% of 135 is.
    <br>1. Create a function named percentageCalculator
    <br>2. Add 2 arguments for “number” and “percentage”
    <br>3. Do the maths required to work out a percentage with the arguments
    <br>4. Return the result of the maths
    <br>5. Console.log the returned value
</body>

<br>Code:

```diff-js
// Percentage calculator
const number = 60, percentage = 5;
console.log(percentageCalculator(number, percentage));

function percentageCalculator (number, percentage)
{
    return (number*percentage/100);
}
```

<script>

// Get required values from user
var number = Number(prompt("Enter the number:"));
var percentage = Number(prompt("Enter the percentage:"));

console.log(percentage + "% of" + number + "=" + percentageCalculator(number, percentage));
document.write(percentage + "% of" + number + "=" + percentageCalculator(number, percentage));

function percentageCalculator (number, percentage)
// Percentage calculator
{
    return (number*percentage/100);
}
</script>
