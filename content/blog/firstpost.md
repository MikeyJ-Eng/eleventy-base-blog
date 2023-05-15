---
title: TCG Bootcamp challenges
description: This is a post based on my TCG Bootcamp experience
date: 2023-05-01
tags:
  - Bootcamp Challenges
---
{% image "./firstpostbanner.jpg", "A teamwork diagram" %}
---------------------------------------------------------------
Task: Make a program to calculate a tip
<br>Create variables for the pre-tip total and the tip percentage
<br>Calculate the new total
<br>Output a sentence to the page (Console, Window, and Document): <br>Your total bill, with tip, is £22.00.
<br><br>Additional:
<br>Make a Procedural Function in Javascript.
<br><br>BONUS POINTS:
<br>Use toFixed() to round the output to 2 decimal places
<br>Display the tip amount:
<br>Your total bill, with tip, is £22.00. The tip amount is £2.00.
<br>Code:
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

<br><br>---------------------------------------------------------------
<br>Task: Intro to JS functions
<br>a) Create a variable called "temperature" to hold °C values.
<br>Write code that informs the user:
<br>-  If it's less than 10 degrees, "Wear a coat."
<br>-  If it's less than 5 degrees, "Wear a coat and a hat."
<br>-  If it's less than 0 degrees, "Stay inside."
<br>-  Otherwise, "Just pants and vest is fine.".
<br>b) Add a logical operator.
<br>Code:
```diff-js
<body>
    <button type="button" onclick="WhatShallIWear()">What shall I wear?</button>
</body>

<script>
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

// const temperature = 25;
// testMyJS(temperature);
</script>
```

<body>
    <button type="button" onclick="WhatShallIWear()">What shall I wear?</button>
</body>

<script>
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

<br>------------------------------------------------------------
Task: Fixstart 
<br>Create a function called fixStart. It should take a single argument, a string, and return a version where all occurrences of its first character have been replaced with except for the first character itself. You can assume that the string is at least one character long. <br>For example:
<br>fixStart('babble'): 'ba**le'
<br>fixStart('turtle'): 'tur*le'
<br>fixStart('and'): 'and'
<br>Start by writing the pseudocode

<br>Pseudocode for function:
<br>STORE the first character of the passed string
<br>SPLIT the string to an array
<br>LOOP FOR each character from the 2nd character
<br>  IF the character == the stored character
<br>      UPDATE the character to "*"
<br>JOIN the array back to a string
<br>RETURN the string

<br>Code:
```diff-js
// fixStart game
oldString = "babble";  // Expected answer: 'ba**le'
document.write(`Changed ${oldString} to ${fixStart(oldString)}`);

function fixStart(oldString) {
  // Store the first character of the passed string
  let firstChar = oldString[0];
  // Split the string to an array
  let newString = oldString.split('');
  let len = oldString.length;

  // Loop for each character from the 2nd character
  for (i=1; i < len; i++) {
    if (oldString[i] === firstChar) {
        newString[i] = "*";
    } 
  }

  // Join the array back to a string
  newString = newString.join("");
  return (newString);
}
```

// fixStart game
oldString = "babble";  // Expected answer: 'ba**le'
document.write(`Changed ${oldString} to ${fixStart(oldString)}`);

function fixStart(oldString) {
  // Store the first character of the passed string
  let firstChar = oldString[0];
  // Split the string to an array
  let newString = oldString.split('');
  let len = oldString.length;

  // Loop for each character from the 2nd character
  for (i=1; i < len; i++) {
    if (oldString[i] === firstChar) {
        newString[i] = "*";
    } 
  }

  // Join the array back to a string
  newString = newString.join("");
  return (newString);
}
