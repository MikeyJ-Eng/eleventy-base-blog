---
title: Loops, Arrays and Objects
description: This is a post based on my TCG Bootcamp experience
date: 2023-05-07
tags:
  - Bootcamp Challenges
---

<body>
    <h3 Tasks:></h3>
    <br>Task 1: Write a loop that outputs the 7 times table, from 1 x 7 = 7 to 12 x 7 = 84
<br>This task introduced students to loops.

<br><br>Task 2: Create an array of your favourite foods, and print some of them to the screen
<br>This task introduced students to array processing.

<br><br>Task 3: Use a for loop to print a list of all your favourite foods
<br>This task introduced students to traversing an array.

<br><br>Task 4: Create an object to hold information on your favourite recipe. Then, display the properties on screen.
Bonus Points: Create a loop to list all the ingredients and directions.
<br>This task introduced students to lists within objects.

<br><br>Task 5: Add a function called letsCook. Have it say: "I'm hungry! Let's cook..." with the name of your recipe title.
Call your new method.
<br>This task introduced students to passing objects to functions.
</body>

<br>Code:

```diff-js
// -------------------------------------------------------------------------------------------------------------
// Task 1: Write a loop that outputs the 7 times table, from 1 x 7 = 7 to 12 x 7 = 84
for (let i = 1; i < 13; i++) {          // For loop
    document.write("<br>" + i + " * 7 = " + 7 * i);
}

// -------------------------------------------------------------------------------------------------------------
// Task 2: Create an array of your favourite foods, and print some of them to the screen
const faves = ["curry", "pizza", "stir fry", "hotpot"];   // Create food array
document.write(faves[0] + "<br>" + faves[2]);  // Print selected elements

// -------------------------------------------------------------------------------------------------------------
// Task 3: Use a for loop to print a list of all your favourite foods
const faves = ["curry", "pizza", "stir fry", "hotpot"];   // Create food array
for (const i of faves) {       // Loop format for traversing lists
  document.write("<br>" + i);  // Print elements
}

// -------------------------------------------------------------------------------------------------------------
// Task 4: Create an object to hold information on your favourite recipe. Then, display the properties on screen.
Bonus Points: Create a loop to list all the ingredients and directions.
// Create object containing recipe
const recipe = {
    title: "Hotpot",
    servings: 2,
    ingredients: ['soup', 'sausages', 'salt', 'pepper'],
    directions: ['Blend', 'Slice', 'Shake', 'Dice']
}

document.write("Servings: " + recipe.servings);
document.write("<br>Ingredients: ", recipe.ingredients);
document.write("<br><br>Method:");
for (i = 0; i < 4; i++) {
    document.write("<br>" + recipe.directions[i] + " " + recipe.ingredients[i]);
}

// -------------------------------------------------------------------------------------------------------------
// Task 5: Add a function called letsCook. Have it say: "I'm hungry! Let's cook..." with the name of your recipe title.
Call your new method.
Answer:
const recipe = {  // Define recipe object
    title: "Hotpot",
    servings: 2,
    ingredients: ['soup', 'sausages', 'salt', 'pepper'],
    directions: ['stir', 'scoop', 'shake', 'blend']
}

// Print recipe
document.write("Servings: " + recipe.servings);
document.write("<br><br>Ingredients:");
for (const i of recipe.ingredients) {       // New style for loop
  document.write("<br>" + i);  // Print elements
}

document.write("<br><br>Method:");
for (i = 0; i < 4; i++) {     // Original style for loop
    document.write("<br>" + recipe.directions[i] + " " + recipe.ingredients[i]);
}

letsCook(recipe);

function letsCook(recipe) {
    document.write(`<br><br>I'm hungry! Let's cook ${recipe.title}.`);
}
```
