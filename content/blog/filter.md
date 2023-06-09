---
title: Filter
description: This is a post based on my TCG Bootcamp experience
date: 2023-06-09
tags:
  - Bootcamp Challenges
---

<head>
  <!-- Required meta tags -->
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">

  <title>Filter!</title>

  <style>
 h1{
  text-align: center;
}

.form-preamble {
  text-align: center;
}

form {
  width: 55em;
  margin: 1em auto;
}

fieldset {
  margin-bottom: 1em;
}

.hidden {
  display: none;
}

button {
  margin-left: 1em;
}

/* Populating the summary shouldn't affect the images */
#summary {
  min-height: 2em;
}

small {
  margin-top: 1em;
  display: block;
  font-size: medium;
}
  </style>

</head>

<body>
 <!--
  Four animals:
  - pandas
  - tigers
  - lions
  - giraffes
-->
<h1>Animal Filters</h1>
<p class="form-preamble">
  You can filter the images by selecting a type. You can also enter keywords into the search box.
</p>
<form id="filters">
  <fieldset>
    <legend>Type</legend>
      <input type="radio" name="animalType" id="panda" value="panda">
      <label for="panda">Panda</label>
      <input type="radio" name="animalType" id="tiger" value="tiger">
      <label for="tiger">Tiger</label>
      <input type="radio" name="animalType" id="lion" value="lion">
      <label for="lion">Lion</label>
      <input type="radio" name="animalType" id="giraffe" value="giraffe">
      <label for="giraffe">Giraffe</label>
      <input type="radio" name="animalType" id="all" value="all" checked>
      <label for="all">Show All</label>
  </fieldset>
  <label for="search">Search</label>
  <input type="search" name="search" id="search">
</form>

<div id="summary"></div>
<div id="results">
<img animal="panda" class="imageFilter" src="https://images.pexels.com/photos/4444036/pexels-photo-4444036.jpeg?auto=compress&cs=tinysrgb&w=300">
<img animal="panda" class="imageFilter" src="https://images.pexels.com/photos/4741847/pexels-photo-4741847.jpeg?auto=compress&cs=tinysrgb&w=300">
<img animal="lion" class="imageFilter" alt="yawning" src="https://images.pexels.com/photos/2265248/pexels-photo-2265248.jpeg?auto=compress&cs=tinysrgb&w=300">
<img animal="giraffe" class="imageFilter" src="https://images.pexels.com/photos/5745126/pexels-photo-5745126.jpeg?auto=compress&cs=tinysrgb&w=300">
<img animal="giraffe" class="imageFilter" src="https://images.pexels.com/photos/1054699/pexels-photo-1054699.jpeg?auto=compress&cs=tinysrgb&w=300">
<img animal="lion" class="imageFilter" alt="yawning" src="https://images.pexels.com/photos/3498323/pexels-photo-3498323.jpeg?auto=compress&cs=tinysrgb&w=300">
<img animal="panda" class="imageFilter" src="https://images.pexels.com/photos/6939449/pexels-photo-6939449.jpeg?auto=compress&cs=tinysrgb&w=300">
<img animal="tiger" class="imageFilter" alt="yawning" src="https://images.pexels.com/photos/40553/tiger-yawning-snow-adult-40553.jpeg?auto=compress&cs=tinysrgb&w=300">
<img animal="giraffe" class="imageFilter" src="https://images.pexels.com/photos/4577496/pexels-photo-4577496.jpeg?auto=compress&cs=tinysrgb&w=300">
<img animal="tiger" class="imageFilter" src="https://images.pexels.com/photos/2668607/pexels-photo-2668607.jpeg?auto=compress&cs=tinysrgb&w=300">
<img animal="tiger" class="imageFilter" src="https://images.pexels.com/photos/1926335/pexels-photo-1926335.jpeg?auto=compress&cs=tinysrgb&w=300">
<img animal="lion" class="imageFilter" src="https://images.pexels.com/photos/46795/lion-big-cat-predator-safari-46795.jpeg?auto=compress&cs=tinysrgb&w=300">
<img animal="tiger" class="imageFilter" src="https://images.pexels.com/photos/831275/pexels-photo-831275.jpeg?auto=compress&cs=tinysrgb&w=300">
<img animal="lion" class="imageFilter" src="https://images.pexels.com/photos/1320412/pexels-photo-1320412.jpeg?auto=compress&cs=tinysrgb&w=300">
<img animal="giraffe" class="imageFilter" src="https://images.pexels.com/photos/4577498/pexels-photo-4577498.jpeg?auto=compress&cs=tinysrgb&w=300">
<img animal="panda" class="imageFilter" src="https://images.pexels.com/photos/4741848/pexels-photo-4741848.jpeg?auto=compress&cs=tinysrgb&w=300">
</div>

<small>Photos provided by <a href="https://www.pexels.com">Pexels</a>.</small>

  <script>
 const images = document.getElementsByClassName('imageFilter');
// Get the form by ID from the live collection 'document.forms'.
const form = document.forms.filters;
// Get the radio elements by name from the live collection 'form.elements'.
const animalRadios = form.elements.animalType;
// Get the search text field by name from the live collection 'form.elements'.
const search = form.elements.search;
// Get the summary element (for "showing animals that match...").
const summary = document.getElementById('summary');

function shouldShowImage(image) {
  // Get the currently selected animal from the animal type radios collection.
  const selectedAnimal = animalRadios.value;
  // If 'Show All' isn't selected, and the currently selected animal doesn't
  // match the current image's 'animal' attribute, then it shouldn't be visible.
  if (selectedAnimal !== 'all' && selectedAnimal !== image.getAttribute('animal')) {
    return false;
  }
  // At this point we know the animal isn't filtered out by the radio buttons.
  // So if there's nothing in the search text field, it should be visible.
  if (!search.value) {
    return true;
  }
  // At this point we know there's something in the search text field. If the
  // image's alt attribute includes the search value, then the image should be
  // visible; otherwise it shouldn't.
  // For a case insensitive match, convert both the alt text and the search query
  // to lower case.
  return image.alt.toLowerCase().includes(search.value.toLowerCase());
}

function update() {
  filterAnimals();
  updateSummary();
}

// Now update the summary on page load for the default selection.
updateSummary();

function filterAnimals() {
  for (const image of images) {
    if (shouldShowImage(image)) {
      image.classList.remove('hidden');
    }
    else {
      image.classList.add('hidden');
    }
  }  
}

function updateSummary() {
  // Steve used Node.textContent here, which we haven't learnt.
  // We could use Element.innerHTML instead.
  // It's generally safer to use Node.textContent to set dynamic text content:
  // with innerHTML you always have to ensure you're dealing with trusted input.
  // See https://developer.mozilla.org/en-US/docs/Web/API/Node/textContent
  const filterLabel = form.querySelector(`label[for=${animalRadios.value}]`).textContent;
  // If the search value exists... (colon means "doesn't exist"
  summary.textContent = search.value ?
    `Showing animals that match the filter "${filterLabel}" and the search "${search.value}".` :
    `Showing animals that match the filter "${filterLabel}".`;
}

// Prevent submission of the form. Even though there's no submit button, there are
// other ways to trigger a submission, eg. pressing ENTER on a text field.
form.addEventListener('submit', function (event) {
  event.preventDefault();
});

// Whenever an animal type is selected via the radio buttons, run filterAnimals.
for (const animalRadio of animalRadios) {
  animalRadio.addEventListener('change', update);
}

// Whenever the search query in the search text field is changed, run filterAnimals.
search.addEventListener('keyup', update);
  </script>
</body>