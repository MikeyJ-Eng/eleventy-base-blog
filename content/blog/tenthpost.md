---
title: ToDo List
description: This is a post based on my TCG Bootcamp experience
date: 2023-05-10
tags:
  - Bootcamp Challenges
---

<head>
  <!-- Required meta tags -->
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">

  <title>Todo List!</title>

  <style>
    body {
  font-family: sans;
  line-height: 1.5;
}

/* Limit the maximum width regardless of window size */
.container {
  max-width: 60em;
  margin-left: auto;
  margin-right: auto;
}

/* The form */
#todo {
  border: solid thin darkgray;
  padding: 1.5em;
  border-radius: 0.25em;
}

/* The unordered list containing the todos */
#todo-pane {
  padding: 0;
}

/* The todos themselves */
#todo-pane li {
  display: flex;
  max-width: 20em;
  align-items: center;
  background-color: lightyellow;
  border: thin orange solid;
  border-radius: 0.25em;
  padding: 0.5em;
  margin: 1em 0;
}

/* A todo that was just created */
.just-created {
  box-shadow: 0 0 20px 1px orange;
}

/* The image of a flag within a todo */
#todo-pane li img {
  width: 1em;
  padding-right: 1rem;
}

/* The small text in the footer */
small {
  font-size: small;
  font-style: italic;
}
  </style>

</head>

<body>
  <div class="container">
    <h1>Todo</h1>
    <p>Fill out the form below to add a todo note. Click on the todo note to dispose of it.</p>
    <form id="todo">
      <label for="title">Title</label>
      <input type="text" name="title" id="title" required>
      <label for="priority">Priority</label>
      <select name="priority" id="priority">
        <option value="low">Low</option>
        <option value="medium" selected>Medium</option>
        <option value="high">High</option>
      </select>
      <button>Add</button>
    </form>

    <!-- This is an empty container for use by javascript. -->
    <ul id="todo-pane"></ul>

    <footer>
      <small>
        Flag images used with thanks from <a
          href="https://www.iconfinder.com/iconsets/prettyoffice8">https://www.iconfinder.com/iconsets/prettyoffice8</a>.
      </small>
    </footer>
  </div>

  <script>
    // Store the URL of an image for each priority level.
    const priorityImages = {
      low: 'https://cdn1.iconfinder.com/data/icons/prettyoffice8/256/Flag-green.png',
      medium: 'https://cdn1.iconfinder.com/data/icons/prettyoffice8/256/Flag-yellow.png',
      high: 'https://cdn1.iconfinder.com/data/icons/prettyoffice8/256/Flag-red.png',
    };

    // Get the form by ID from the forms collection.
    const form = document.forms.todo;
    // Get the todo pane (the 'ul' element) to insert todos into.
    const todoPane = document.getElementById('todo-pane');
    // Get the text input for the title. We'll read from this when creating the todo.
    const titleInput = form.elements.title;
    // Get the priority select element. We'll ready from this when creating the todo.
    const prioritySelect = form.elements.priority;
    // Get a *live* list of all elements with the 'todo' class.
    const allTodos = document.getElementsByClassName('todo');


    // Add a submit listener to the form that adds a todo and prevents default.
    form.addEventListener('submit', function (event) {

      // First remove the 'just-created' class from all existing todos. (Remember that
      // allTodos is a live collection that keeps itself automatically updated.)
      for (const todo of allTodos) {
        todo.classList.remove('just-created');
      }

      // Create the new todo using the values from the form elements.
      const newTodo = createTodo(titleInput.value, prioritySelect.value);

      // Add the new todo to the todo pane (ie add a new list item to the unordered
      // list).
      todoPane.appendChild(newTodo);

      // Clear the text input ready for the next one. We could also call reset() ontextInput
      // the form, and that would also affect the priority select.
      titleInput.value = '';

      // Don't actually submit the form to a server.
      event.preventDefault();
    });

    /**
     * Creates and returns a new todo element.  
     * @param {string} title - The title of the todo
     * @param {string} priority - The priority: 'high', 'medium', 'low'.
     * @return {HTMLElement} The new todo element with 'just-created' class.
     */
    function createTodo(title, priority) {
      // Create the text for the title.
      const textNode = document.createTextNode(title);
      // Create a div to contain the title text.
      const textDiv = document.createElement('div');
      // Add the title text to its div container.
      textDiv.appendChild(textNode);
      // Create the new list item for the new todo.
      const todo = document.createElement('li');
      // Create the new image for the todo flag.
      const image = document.createElement('img');
      // Set the src of the image to the appropriate flag.
      image.src = priorityImages[priority];

      // Add the image as the first child of the new todo.
      todo.appendChild(image);
      // Add the text div as the second child of the new todo.
      todo.appendChild(textDiv);

      // Add the standard 'todo' class and also a 'just-created' class that
      // will be removed later. Using multiple arguments won't work in IE.
      todo.classList.add('todo', 'just-created');

      // Add a click handler to the todo, so you can remove it by clicking.
      todo.addEventListener('click', function (event) {
        event.currentTarget.remove();
      })

      return todo;
    }
  </script>
</body>