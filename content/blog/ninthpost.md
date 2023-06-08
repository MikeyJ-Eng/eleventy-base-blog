---
title: Loops, Arrays and Objects - Averages
description: This is a post based on my TCG Bootcamp experience
date: 2023-05-09
tags:
  - Bootcamp Challenges
---

<body>
    <h3 Task 2: Work out the average of an array of values></h3>

    <br>We are going to be creating a function that is able to take all of the values of an array and return the average.
    <br>The function will be able to return the mode, median or mean of the numbers.
    <br>Create an array of random numbers.
    <br>Create a function which takes 2 arguments (the array and a type variable).
    <br>Create a switch statement which has the cases ‘mode’, ‘median’ and ‘mean’.
    <br>Return the required number based on the arguments passed.

</body>

<br>Code:

```diff-js
// Sorting - Mean=3, Median=2, Mode=5
const numArray = [1, 5, 1, 2, 5, 2, 5], type = "Mode";
console.log("The", type, "average is", calculateAverage(numArray, type));

function calculateAverage(numArray, type) {
    switch (type) {
        case "Mean":
            let meanValue = 0;
            for (i = 0; i < numArray.length; i++) {
                meanValue += numArray[i];
            }
            return meanValue / numArray.length;
            break;

        case "Median":
            // Check for an odd number of elements
            let middleNum = numArray.length / 2;
            if (middleNum != Math.round(numArray.length / 2)) {
                middleNum = Math.round(numArray.length / 2);
            }

            // Sort the array
            numArray.sort(function (a, b) {
                return a - b;
            })

            // Return the middle value
            return numArray[middleNum - 1];
            break;

        case "Mode":
            // Sort the array
            numArray.sort(function (a, b) {
                return a - b;
            })

            // Initialise start values
            let highNum = numArray[0], currNum = numArray[0], highVal = 1, currVal = 1;

            // Traverse the array of numbers from 2nd element
            for (i = 1; i < numArray.length; i++) {

                if (numArray[i] == currNum) {
                    // Same number read
                    currVal = currVal + 1;
                    if (currVal > highVal) {
                        highNum = currNum;
                        highVal = currVal;
                    }
                } else {
                    // New number read
                    currNum = numArray[i];
                    currVal = 1;
                }
            }

            // EOF processing
            if (currVal > highVal) {
                highNum = currNum;
            }

            return highNum;
            break;

        default:
            console.log("Invalid type (Mean, Mode, Median)");
            break;
    }
}

```
