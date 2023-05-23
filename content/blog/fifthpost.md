---
title: TCG Bootcamp challenges
description: This is a post based on my TCG Bootcamp experience
date: 2023-05-05
tags:
  - Bootcamp Challenges
---
---------------------------------------------------------------
<h2 Fix Start challenge></h2>
<br><h2 id="fixStart">Task: Fixstart</h2>
<br>Create a function called fixStart. It should take a single argument, a string, and return a version where all occurrences of its first character have been replaced except for the first character itself.
<br>You can assume that the string is at least one character long. <br>For example:
<br>fixStart('babble'): 'ba**le'
<br>fixStart('turtle'): 'tur*le'
<br>fixStart('and'): 'and'

<br>Start by writing the pseudocode.
<br>Pseudocode for function:
<br>STORE the first character of the passed string
<br>SPLIT the string to an array
<br>LOOP FOR each character from the 2nd character
<br>-  IF the character == the stored character
<br>--      UPDATE the character to "*"
<br>JOIN the array back to a string
<br>RETURN the string

<br>Code:

```diff-js
var oldString = prompt("Enter a word to play Fix Start");
document.write(`Changed ${oldString} to ${fixStart(oldString)}`);

function fixStart(oldString) {
    // Store the first character of the passed string
    let firstChar = oldString[0];
    // Split the string to an array
    let newString = oldString.split('');
    let len = oldString.length;

    // Loop for each character from the 2nd character
    for (i = 1; i < len; i++) {
        if (oldString[i] === firstChar) {
            newString[i] = "*";
        }
    }

    // Join the array back to a string
    newString = newString.join("");
    return (newString);
}
```

<script>
    var oldString = prompt("Enter a word to play Fix Start");
    document.write(`Changed ${oldString} to ${fixStart(oldString)}`);

    function fixStart(oldString) {
        // Store the first character of the passed string
        let firstChar = oldString[0];
        // Split the string to an array
        let newString = oldString.split('');
        let len = oldString.length;

        // Loop for each character from the 2nd character
        for (i = 1; i < len; i++) {
            if (oldString[i] === firstChar) {
                newString[i] = "*";
            }
        }

        // Join the array back to a string
        newString = newString.join("");
        return (newString);
    }
</script>
