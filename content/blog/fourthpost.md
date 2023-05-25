---
title: Drinks Machine
description: This is a post based on my TCG Bootcamp experience
date: 2023-05-04
tags:
  - Bootcamp Challenges
---

<body>
    <h3 Task: Switch statement></h3>
    Customers can order 3 types of drink (Cola, Lemonade and Orangeade) in 3 sizes (Small, Medium and Large)
    <br>The buttons they press have the values “cola”, ”lemon”, ”orange”
    <br>Create a function that will return the message “You have ordered a {size} of {softDrinkLabel}”
    <br>1. Create a function named drinkOrder
    <br>2. Add 2 arguments for “size” and “buttonName”
    <br>3. Use a switch statement to determine where the functional code needs to be written
    <br>4. Create a message in each case statement to be returned.
    <br>5. Console.log the returned message
</body>

<br>Code:

```diff-js
// Drinks machine
var size = "s", buttonName = "orange";

msg = drinkOrder(size, buttonName);
console.log(msg);

function drinkOrder(size, buttonName) {
    switch (size) {
        case "s":
            size = " small";
            break;
        case "m":
            size = " medium";
            break;
        case "l":
            size = " large";
            break;
        default:
            size = "n undetermined-sized";
    }

    switch (buttonName) {
        case "cola":
            buttonName = "Cola";
            break;
        case "lemon":
            buttonName = "Lemonade";
            break;
        case "orange":
            buttonName = "Orangeade";
            break;
        default:
            buttonName = "water";
    }
  
    msg = "You have ordered a" + size + " " + buttonName;
  return (msg);
}
```

<script>
// Drinks machine
var size = "s", buttonName = "orange";

msg = drinkOrder(size, buttonName);
console.log(msg);

function drinkOrder(size, buttonName) {
    switch (size) {
        case "s":
            size = " small";
            break;
        case "m":
            size = " medium";
            break;
        case "l":
            size = " large";
            break;
        default:
            size = "n undetermined-sized";
    }

    switch (buttonName) {
        case "cola":
            buttonName = "Cola";
            break;
        case "lemon":
            buttonName = "Lemonade";
            break;
        case "orange":
            buttonName = "Orangeade";
            break;
        default:
            buttonName = "water";
    }
  
    msg = "You have ordered a" + size + " " + buttonName;
  return (msg);
}
</script>