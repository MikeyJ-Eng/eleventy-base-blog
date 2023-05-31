---
title: Loops, Arrays and Objects - Practical
description: This is a post based on my TCG Bootcamp experience
date: 2023-05-08
tags:
  - Bootcamp Challenges
---

<body>
    <h3 Task: We are going to be using an array of objects provided as a simple shopping cart example></h3>
    <br>Task - Get the cart total


<br><br>Part 1 - Get the cart total
<br>We need to work out the total cost of the items in the shopping cart:
<br> - Create a function that takes 1 argument (the array)
<br> - Create a variable inside the function called “totalPrice”
<br> - Loop through each item in the array and add the value of the item to the total price, remember to account for the quantity.
<br> - Return the totalPrice Variable
<br> - Console.log the returned value
<br>This task introduced students to looping within functions.

<br><br>Part 2
<br>If the item has a type of “food” the total price is 20% less
<br>This task re-introduced students to flow control.

<br><br>Part 3
<br>Add 2 extra arguments to the function for “discountAmount” and “type”
<br> - Replace the logic that takes off 20% for object.type == “food” for object.type == type and allow the 20% to be the {discountAmount}%
<br> - Create logic so that if type == “any” all products have a discount applied
<br>This task re-introduced students to flow control.

</body>

<br>Code:

```diff-js
// Part 1: Get the cart total
let shoppingCart = [
    { name: "loaf of bread", type: "food", quantity: 1, price: 0.85 },
    { name: "multipack beans", type: "food", quantity: 1, price: 1 },
    { name: "mushrooms", type: "food", quantity: 10, price: 0.1 },
    { name: "can of beer", type: "alcohol", quantity: 4, price: 1.1 },
    { name: "prosecco", type: "alcohol", quantity: 1, price: 8.99 },
    { name: "steak", type: "food", quantity: 2, price: 3.99 },
    { name: "blue cheese", type: "food", quantity: 1, price: 2.99 },
    { name: "candles", type: "home", quantity: 3, price: 1.99 },
    { name: "cheesecake", type: "food", quantity: 1, price: 4.99 },
    { name: "onions", type: "food", quantity: 3, price: 0.4 },
];

console.log(shopper(shoppingCart).toFixed(2));

function shopper(cart) {
    let totalPrice = 0;
    for (let item of cart) {
        totalPrice += item.quantity * item.price
    }
    return totalPrice;
}


// Part 2: If the item has a type of “food” the total price is 20% less
let shoppingCart = [
    { name: "loaf of bread", type: "food", quantity: 1, price: 0.85 },
    { name: "multipack beans", type: "food", quantity: 1, price: 1 },
    { name: "mushrooms", type: "food", quantity: 10, price: 0.1 },
    { name: "can of beer", type: "alcohol", quantity: 4, price: 1.1 },
    { name: "prosecco", type: "alcohol", quantity: 1, price: 8.99 },
    { name: "steak", type: "food", quantity: 2, price: 3.99 },
    { name: "blue cheese", type: "food", quantity: 1, price: 2.99 },
    { name: "candles", type: "home", quantity: 3, price: 1.99 },
    { name: "cheesecake", type: "food", quantity: 1, price: 4.99 },
    { name: "onions", type: "food", quantity: 3, price: 0.4 },
];

console.log(shopper(shoppingCart).toFixed(2));

function shopper(cart) {
    let totalPrice = 0;
    for (let item of cart) {
        if (item.type == "food") {
            totalPrice += item.quantity * item.price * 0.8;
        } else {
            totalPrice += item.quantity * item.price;
        }
    }
    return totalPrice;
}


// Part 3: Add 2 arguments to the function for “discountAmount” and “type”
// Replace the logic that takes off 20% for object.type == “food” for object.type == type and allow the 20% to be the {discountAmount}%
// Create logic so that if type == “any” all products have a discount applied
let shoppingCart = [
    { name: "loaf of bread", type: "food", quantity: 1, price: 0.85 },
    { name: "multipack beans", type: "food", quantity: 1, price: 1 },
    { name: "mushrooms", type: "food", quantity: 10, price: 0.1 },
    { name: "can of beer", type: "alcohol", quantity: 4, price: 1.1 },
    { name: "prosecco", type: "alcohol", quantity: 1, price: 8.99 },
    { name: "steak", type: "food", quantity: 2, price: 3.99 },
    { name: "blue cheese", type: "food", quantity: 1, price: 2.99 },
    { name: "candles", type: "home", quantity: 3, price: 1.99 },
    { name: "cheesecake", type: "food", quantity: 1, price: 4.99 },
    { name: "onions", type: "food", quantity: 3, price: 0.4 },
];

const type = "all";
const discountPercent = 80; 

console.log(shopper(shoppingCart, type, discountPercent).toFixed(2));

function shopper(cart, type, discountPercent) {
    let totalPrice = 0;
    for (let item of cart) {
        if (type == "all" || type == item.type) {
            totalPrice += item.quantity * item.price * discountPercent / 100;
        } else {
            totalPrice += item.quantity * item.price;
        }
    }
    return totalPrice;
}
```
