---
title: TCG Bootcamp Form-processing challenge
description: This is a post based on my TCG Bootcamp experience
date: 2023-05-02
tags:
  - Bootcamp Challenges
---
Create a new HTML form on the new page on your static site:
<br>First name.
<br>Surname.
<br>Email.
<br>Message.
<br>Checkbox for terms and conditions.
<br>Embed the form in your site, and style the form using bootstrap.
<br>Test the form on the site.
<br>Test the data was submitted.

<br>Code:
```diff-js
<body>
    <h1>Form Processing</h1>
    // method="GET" used to show parameters
    <form action=Imaginary_Page.js method="GET">

        <div class="form-group">
            <label for="firstName">First name:</label>
            <input type="text" id="firstName" name="firstName" class="form-control" required placeholder="Sherlock">
        </div><br>

        <div class="form-group">
            <label for="surname">Surname:</label>
            <input type="text" id="surname" name="surname" class="form-control" required placeholder="Holmes">
        </div><br>

        <div class="form-group">
            <label for="email">Email:</label>
            <input type="email" id="email" name="email" class="form-control" required>
        </div><br>

        <div class="form-group">
            <label for="password">Password(8-16 chars):</label>
            <input type="password" id="password" name="password" class="form-control" minlength="8" maxlength="16"
                required>
        </div><br>

        <div class="form-group">
            <label for="message">Message:</label>
            <input type="text" id="message" name="message" class="form-control">
        </div><br>

        <div class="form-group">
            <label for="tnc">Agree to terms and conditions:</label>
            <input type="checkbox" id="tnc" name="tnc">
        </div><br>

        <div class="form-group">
            <button class="btn btn-default" type="reset">Reset</button>
        </div>

        <div class="form-group">
            <button class="btn btn-default" type="submit">Submit</button>
        </div>

    </form>
</body>
```


<body>
    <h1>Form Processing</h1>
    // method="GET" used to show parameters
    <form action=Imaginary_Page.js method="GET">

        <div class="form-group">
            <label for="firstName">First name:</label>
            <input type="text" id="firstName" name="firstName" class="form-control" required placeholder="Sherlock">
        </div><br>

        <div class="form-group">
            <label for="surname">Surname:</label>
            <input type="text" id="surname" name="surname" class="form-control" required placeholder="Holmes">
        </div><br>

        <div class="form-group">
            <label for="email">Email:</label>
            <input type="email" id="email" name="email" class="form-control" required>
        </div><br>

        <div class="form-group">
            <label for="password">Password(8-16 chars):</label>
            <input type="password" id="password" name="password" class="form-control" minlength="8" maxlength="16"
                required>
        </div><br>

        <div class="form-group">
            <label for="message">Message:</label>
            <input type="text" id="message" name="message" class="form-control">
        </div><br>

        <div class="form-group">
            <label for="tnc">Agree to terms and conditions:</label>
            <input type="checkbox" id="tnc" name="tnc">
        </div><br>

        <div class="form-group">
            <button class="btn btn-default" type="reset">Reset</button>
        </div>

        <div class="form-group">
            <button class="btn btn-default" type="submit">Submit</button>
        </div>

    </form>
</body>