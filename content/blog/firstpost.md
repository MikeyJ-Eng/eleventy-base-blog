---
title: TCG Bootcamp challenges
description: This is a post based on my TCG Bootcamp experience
date: 2023-05-01
tags:
  - Bootcamp Challenges
---
{% image "./firstpostbanner.jpg", "A teamwork diagram" %}
---------------------------------------------------------------
<h2 id="toc">Table Of Contents</h2>
<a href="#calculateTip">1. Calculate a tip challenge</a>
<br><a href="#whatShallIWear">2. What shall I wear? challenge</a>
<br>
---------------------------------------------------------------

<body>
    <br><button type="button" onclick="calculateTotalCost()">Calculate a tip</button>
    <br><button type="button" onclick="WhatShallIWear()">What shall I wear?</button>
    <br><br><br>
    <h3 id="calculateTip">Task: Make a program to calculate a tip</h3>
    Create variables for the pre-tip total and the tip percentage
    <br>Calculate the new total
    <br>Output a sentence to the page (Console, Window, and Document): <br>Your total bill, with tip, is £22.00.
    <br><br>Additional:
    <br>Make a Procedural Function in Javascript.
    <br><br>BONUS POINTS:
    <br>Use toFixed() to round the output to 2 decimal places
    <br>Display the tip amount:
    <br>Your total bill, with tip, is £22.00. The tip amount is £2.00.
</body>

<br>Code:
```diff-js
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
```

<br><a href="#toc">Return to top</a>

<br><br>---------------------------------------------------------------
<br><h3 id="whatShallIWear">Task: Checking the temperature</h3>
<br>a) Create a variable called "temperature" to hold °C values.
<br>Write code that informs the user:
<br>-  If it's less than 10 degrees, "Wear a coat."
<br>-  If it's less than 5 degrees, "Wear a coat and a hat."
<br>-  If it's less than 0 degrees, "Stay inside."
<br>-  Otherwise, "Just pants and vest is fine.".
<br>b) Add a logical operator.
<br>Code:

```diff-js
function WhatShallIWear() {
var temperature = Number(prompt("Enter temperature:"));
    if (temperature < 0) {
        document.write("Stay inside");
    }
    else if (temperature < 5) {
        document.write("Wear a coat and a hat");
    }
    else if (temperature < 10) {
        document.write("Wear a coat");
    }
    else {
        document.write("Just pants and vest is fine");
    }

    if (temperature > 20 && temperature < 50) {
        document.write("<br>Time to sunbathe!");
    }
}
```

<br><a href="#toc">Return to top</a>

<script>
// Functions here:
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

function WhatShallIWear() {
var temperature = Number(prompt("Enter temperature:"));
    if (temperature < 0) {
        document.write("Stay inside");
    }
    else if (temperature < 5) {
        document.write("Wear a coat and a hat");
    }
    else if (temperature < 10) {
        document.write("Wear a coat");
    }
    else {
        document.write("Just pants and vest is fine");
    }

    if (temperature > 20 && temperature < 50) {
        document.write("<br>Time to sunbathe!");
    }
}
</script>
