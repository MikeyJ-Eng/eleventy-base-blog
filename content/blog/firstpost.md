---
title: This page highlights my TCG Bootcamp homework tasks
description: This is a post about my TCG Bootcamp experience
date: 2023-05-01
tags:
  - another tag
---
---------------------------------------------------------------
Task: We’ll make a program to calculate a tip
Create variables for the pre-tip total and the tip percentage
Calculate the new total
Output a sentence to the page (Console, Window, and Document): Your total bill, with tip, is £35.45

Additional:
Make a Procedural Function in Javascript.
BONUS POINTS:
Use toFixed() to round the output to 2 decimal places
Display the tip amount

<body>
    <h1>Calculate bill cost</h1>
    <button type="button" onclick="calculateTotalCost()">Calculate bill cost</button>
</body>

<script>
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
</script>
