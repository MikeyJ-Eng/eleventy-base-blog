---
title: This is my sixth post
description: This is a post on My Blog for the TCG SSG task.
date: 2023-04-06
tags:
  - another tag
---
Today, I completed the task for my TCG "Intro to JavaScript" lesson, as follows:

1 We’ll make a program to calculate a tip

Create variables for the pre-tip total and the tip percentage
Calculate the new total
Output a sentence to the page - something like:
Your total bill, with tip, is £35.45

BONUS POINTS:

Use toFixed() to round the output to 2 decimal places
Display the tip amount in the output as well
2 Extend the Tip program

Create variables for the pre-tip total and the tip percentage
Calculate the new total
Output a sentence to the page - something like:
“Your total bill, with tip, is £35.45”

Extension: round the figure to 2 DP and display the tip amount.

Additional
Make a Procedural Function in Javascript.

Please provide a link below to your Codepen with the tasks on. Also please add a blog about these tasks to your Blogs.


## Section Header

<a href="/blog/fifthpost/">Fifth post</a>

HTML:
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Javascript</title>

</head>

<body>
    <h1>Calculate bill cost</h1>
    <button type="button" onclick="calculateTotalCost()">Calculate bill cost</button>

    <!--Name your external files-->
    <script src="Calculate a tip.js"></script>
</body>

</html>


JAVASCRIPT:
function calculateTotalCost() {
        // Calculate a tip

        /* Get required values from user */
        var mealCost = Number(prompt("Enter meal price:"));

        var tipPerc = Number(prompt("Enter the tip percentage:"));

        var tipTotal = Number(tipPerc / 100 * mealCost);
        var totalCost = mealCost + tipTotal;

        totalCost = totalCost.toFixed(2);
        tipTotal = tipTotal.toFixed(2);

        console.log("Your total bill, with tip, is £", totalCost, ".", "\n", "The tip amount is £", tipTotal);

        window.alert("Your total bill, with tip, is £" + totalCost + "." + "\n" + "The tip amount is £" + tipTotal);

        var billMsg = "Your total bill, with tip, is £" + totalCost + ". The tip amount is £" + tipTotal
        document.write(billMsg.replace("£ ","£"));
}

```
