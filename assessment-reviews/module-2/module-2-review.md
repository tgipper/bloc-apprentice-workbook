# Module 2 Review Questions and Exercises

## Instructions

1. Click "edit" at the top of the page.
2. Fill in your answers below each question.
3. Save your changes and send a link to your mentor!

*Note: any topics from the first assessment should be reviewed in addition to the questions below!*

## CSS

### Questions

1. What is the box model? The box model refers to how CSS handles HTML elements. Each element is treated as a box that, by default, fills the width of the screen. Different elements are then stacked on top of each other.
2. What is the difference between block and inline elements? Block elements do not tolerate being side-by-side with other elements, whereas inline elements natural sit next to other inline elements.
3. What is responsive design? Responsive design is the ability for an application to change it's layout or functionality based on the type of device using the application.
4. Which selector is more specific, a tag selector or class selector? A class selector.
5. What does `box-sizing` do? It defines how a box is measured. By default, boxes are measured by it's content and padding, border, and margin are all added to the measurements of the content. THe box-sizing can also be set to border-box, which includes the content, padding, and border in it's calculation of box size.
6. What's the difference between `relative` and `absolute` positioning? `Relative` positioning maintains the normal flow of the document and adjusts the element's position based on where the element would normally be positioned. `Absolute` positioning takes the element out of the normal flow of the document and positions the element relative to it's parent container.

### Exercises

1. Write a CSS rule to turn the background color of the link with the `.btn` class blue on hover:

  ```html
  <a href="#" class="btn">Learn more</a>
  ```
  
  ```css
  .btn:hover {
    background-color: blue;
  }
  ```

2. Write a CSS rule to give the `.container` a maximum width of `980px` when the browser window is wider than `1200px`:

  ```html
  <div class="container">
    <h1>I'm a heading!</h1>
  </div>
  ```
  ```css
  @media (min-width: 1201px) {
    .container {
      max-width: 980px;
    }
  }
  ```

3. Which text would be red in the following example?

  ```html
  <style>
    section p:last-child {
      color: red;
    }
  </style>

  <section>
    <p>First paragraph</p>
    <p>Second paragraph</p>
    <p>Third paragraph</p>      This paragraph
  </section>
  <section>
    <p>First paragraph</p>
    <p>Second paragraph</p>
    <p>Third paragraph</p>      This paragraph
  </section>
  ```

4. Open this [JSBin](http://jsbin.com/qigiwuhepe/1/edit?html,css,output). Write a CSS rule using floats to make the HTML sample into a four column layout. Paste your udpated link below.

http://jsbin.com/halufequce/edit?html,css,output

## JavaScript

### Questions

1. What is a callback? It is a function passed in to another function.

### Exercises

1. Write a function `filterLongWords()` that takes an array of words and an integer `num` and returns the array of words that are longer than `num`.

```
var filterLongWords = function (array, num) {
  var longWords = [];
  for ( i = 0; i < array.length; i++ ) {
    if (array[i].length > num) {
      longWords.push(array[i]);
    }
  }
  return longWords;
}
```

2. Write a function `charFreq()` that takes a string and builds a frequency listing of the characters contained in it. Represent the frequency listing as a Javascript object. Try it with something like `charFreq("abbabcbdbabdbdbabababcbcbab")`.

```
function charFreq(string) {
  var charList = {};
  for ( i = 0; i < string.length; i++ ) {
    if (charList.hasOwnProperty(string[i])) {
      charList[string[i]]++;
    }
    if (charList.hasOwnProperty(string[i]) === false) {
      charList[string[i]] = 1;
    }
  }
  return charList;
};
```

## DOM Scripting

### Questions

1. What does DOM stand for and what is it? Document Object Model, and it is the way that a document is layed out. Each document is made up of objects that are all connected together as described in the Document Object Model.

### Exercises

1. Write a JavaScript statement that finds the element with the ID, `next`, and saves it to a variable called `nextButton`:

  ```html
  <a href="#" id="next" class="btn">Next</a>
  ```
  
  ```
  var nextButton = document.getElementById('next');
  ```

2. Write another line that updates the text of `nextButton` to `"Next image"`.
```
nextButton.innerHTML = "Next image";
```
3. Write another line that adds a click event listener to `nextButton` so that when it's clicked the browser alerts `"Next image coming up."`.
```
nextButton.addEventListener('click', function(){alert("Next image coming up.")});
```

## jQuery

### Questions

1. What is a JavaScript library and why do we use them? It is a set of prewritten JavaScript, used to make programming easier and faster.
2. What is jQuery for? jQuery is a JavaScript library that simplifies DOM manipulation.

### Exercises

1. Write a statement to select all elements with the `.btn` class using a jQuery selector and save them to a variable called `buttons`:

  ```html
  <a href="#" id="next" class="btn">Next</a>
  <a href="#" id="beginning" class="btn">Beginning</a>
  <a href="#" id="previous" class="btn">Previous</a>
```

```
var buttons = $('.btn');
```

2. Write another line that adds a click event to the buttons that logs `'click'` to the console when the button is clicked. Use the jQuery syntax.

```
$buttons.click(function() {
  console.log('click')
});
```

## Angular

### Questions

1. How is a framework different than a library? A framework provides structure for a piece of software and provides a repeatable solution to a common software problem. A library also is used to provide solutions, but it is broken up into little pieces that can be used within a framework.
2. What is a controller? A controller holds the business-logic for a prtion of an Angular page, and is used to add behavior to a page.
3. What is a view? A view is what is displayed to the user.
4. What is a single page application? A single page application
5. What is a directive in Angular?

## Git

### Exercises

1. Write a command to create a new branch called `bug-fix`.
2. If you're on the `master` branch, write a command to merge a branch called `bug-fix` into the `master` branch.
