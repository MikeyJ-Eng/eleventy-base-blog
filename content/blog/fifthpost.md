---
title: This is my fifth post
date: 2023-05-05

---
This is an "Intro to JS functions" task assigned by TCG:

Task 4
a) Make a variable called "temperature". Write some code that tells you to put on a coat if it is below 50 degrees<br>
b) Extend the Program to show the following:
If it's less than 50 degrees, wear a coat.
If it's less than 30 degrees, wear a coat and a hat.
If it's less than 0 degrees, stay inside.
Otherwise, just pants and vest is fine.<br>
c) Add a logical operator to your ‘Shall I wear a coat?’ program

<script>
function testMyJS(temperature_arg) {
    if (temperature_arg < 0) {
        document.write("Stay inside");
    }
    else if (temperature_arg < 30) {
        document.write("Wear a coat and a hat");
    }
    else if (temperature_arg < 50) {
        document.write("Wear a coat");
    }
    else {
        document.write("Just pants and vest is fine");
    }

    if (temperature_arg > 20 && temperature_arg < 35) {
        document.write("<br>Time to sunbathe!");
    }
}

const temperature = 25;
testMyJS(temperature);
</script>