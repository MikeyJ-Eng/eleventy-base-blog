---
title: TCG Bootcamp challenges
description: This is a post based on my TCG Bootcamp experience
date: 2023-05-01
tags:
  - Bootcamp Challenges
---
---------------------------------------------------------------
Task: We’ll make a program to calculate a tip
<br>Create variables for the pre-tip total and the tip percentage
<br>Calculate the new total
<br>Output a sentence to the page (Console, Window, and Document): <br>Your total bill, with tip, is £22.00.
<br><br>Additional:
<br>Make a Procedural Function in Javascript.
<br><br>BONUS POINTS:
<br>Use toFixed() to round the output to 2 decimal places
<br>Display the tip amount:
<br>Your total bill, with tip, is £22.00. The tip amount is £2.00.

<br><br>Code:
```diff-js
function calculateTotalCost() {
        // Calculate a tip

        // Get required values from user
        var mealCost = Number(prompt("Enter meal price:"));
        var tipPerc = Number(prompt("Enter the tip percentage:"));

        var tipTotal = Number(tipPerc / 100 * mealCost);
        var totalCost = mealCost + tipTotal;

        // Round the output to 2 decimal places
        totalCost = totalCost.toFixed(2);
        tipTotal = tipTotal.toFixed(2);

      // Output a sentence to the page (Console, Window, and Document)
        console.log("Your total bill, with tip, is £", totalCost, ".", "\n", "The tip amount is £", tipTotal);

        window.alert("Your total bill, with tip, is £" + totalCost + "." + "\n" + "The tip amount is £" + tipTotal);

        var billMsg = "Your total bill, with tip, is £" + totalCost + ". The tip amount is £" + tipTotal
        document.write(billMsg.replace("£ ","£"));
}
```

<body>
    <button type="button" onclick="calculateTotalCost()">Calculate bill cost</button>
</body>

<script>
function calculateTotalCost() {
        // Function to Calculate a tip

        // Get required values from user
        var mealCost = Number(prompt("Enter meal price:"));
        var tipPerc = Number(prompt("Enter the tip percentage:"));

        var tipTotal = Number(tipPerc / 100 * mealCost);
        var totalCost = mealCost + tipTotal;

        // Round the output to 2 decimal places
        totalCost = totalCost.toFixed(2);
        tipTotal = tipTotal.toFixed(2);

      // Output a sentence to the page (Console, Window, and Document)
        console.log("Your total bill, with tip, is £", totalCost, ".", "\n", "The tip amount is £", tipTotal);

        window.alert("Your total bill, with tip, is £" + totalCost + "." + "\n" + "The tip amount is £" + tipTotal);

        var billMsg = "Your total bill, with tip, is £" + totalCost + ". The tip amount is £" + tipTotal
        document.write(billMsg.replace("£ ","£"));
}
</script>
