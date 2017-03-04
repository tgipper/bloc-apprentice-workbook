# Module 1 Review Questions and Exercises

## Instructions

1. Click "edit" at the top of the page.
2. Fill in your answers below each question.
3. Save your changes and send a link to your mentor!

## HTML

### Questions

1. What is HTML and what is it used for? It is a text language used for creating web pages.
2. What is the difference between an ID and a class? An ID is used for a unique tag that appears once on a page, a class can be used in different tags throughout a page.
3. What does it mean to write "semantic" HTML? Writing semantic HTML means to use tags that are more clear about their purpose. An example would be to use a header tag instead of a div tag.

### Exercises

1. Write a paragraph tag with a class of "highlight" and content "Watch out!".
```html
<p class="highlight">Watch out!</p>
```
2. Write an HTML image tag to show an image called `profile-picture.jpg`.
```html
<img src="profile-picture.jpg" alt="profile-picture">
```
3. Write a link tag that links to http://google.com.
```html
<a href="http://www.google.com">
```
5. Write an complete standard HTML document outline (including a DOCTYPE, and `<html>`, `<head>`, and `<body>` tags).
```html
<!DOCTYPE html>
<head>
<script src="main.js">
<link type="text/css" rel="stylesheet" src="main.css">
<title></title>
</head>
<body>
  <ol>
    <li>A Bag of Bones</li>
    <li>Musicophelia</li>
    <li>So You Want to be a Wizard</li>
  </ol>
</body>
</html>
```
6. Inside of the code for the previous exercise, write the appropriate tag to link to a script file called `main.js`.
7. Inside of the code for the previous exercise, write the appropriate tag to link to a stylesheet file called `main.css`.
8. Write a numbered list in HTML and list three of your favorite books.
9. Fix the indentation of the following HTML sample:

  ```html
  <div>
    <ul>
      <li>Item 1</li>
      <li>Item 2</li>
      <li>Item 3</li>
    </ul>
  </div>
  ```

## CSS

### Questions

1. What is CSS and what is it used for? It is a stylesheet, used to change the appearance of an HTML document.
2. What is the CSS box model? Different sections of CSS are visually displayed as boxes. The boxes are then stacked on top of each other going down the web page, but CSS is able to change the way the boxes are arranged so that they can be different heights, widths, or side by side.
3. What's the difference between margin and padding? Padding puts space between the content of a box and the border of the box, whereas margin changes the space between the border and the edge of other document elements.

### Exercises

1. Write a CSS rule to make the text of all `h1` tags red.
```CSS
h1 {
color: red;
}
```
2. Write a CSS rule to make the background color of the link with `class="btn"` blue:
```CSS
.class {
color: blue;
}
```
  ```html
  <a href="#" class="btn">Learn more</a>
  ```

3. Write a CSS rule to give the first paragraph in the following HTML a font size of `20px`, but not the second paragraph.
```CSS
header p {
font-size: 20px;
}
```
  ```html
  <header class="jumbotron">
    <p>Hello, World!</p>
  </header>

  <p>Welcome to this awesome website!</p>
  ```

## JavaScript

### Questions

1. What is a function? What are they used for? A function is a piece of code designed to perform a specific task.
2. What is the difference between `==` and `===`? '==' compares two values even if they aren't the same type; whereas "===" requires the values to be of the same type if they will be equal to each other.
3. What is the difference between global and local scope variables? Global scope variables can be used throughout the program and can be accessed from anywhere in the program. Local scope variables are only accessible within their own sphere, so local variables can not be references by parts of the program outside of the local variable's scope.
4. What is a boolean value? A boolean value is either true or false.
5. What is an array? An array is a variable that can hold more than one value at a time.

### Exercises

1. Write a line that declares a variable called `myName` and set its value to your name.
```javascript
var myName = "Trevor";
```
2. Write a loop that logs the numbers 1 through 10 to the console.
```javascript
for (var i = 1; i <= 10; i++){
  console.log(i);
}
```
3. Translate the following pseudocode into JavaScript: if `score` is greater than `3` and `lives` is greater than `0`, alert "You win!".
```javascript
  if ( score > 3 && lives > 0){
    alert("You win!");
  }
```
4. Write a function `sayHello` that takes one argument, a name, and logs "Hello, <name>!" to the console. Then, call the function below the function definition and pass in your name as the argument.
```javascript
function sayHello (name){
  console.log("Hello, " + name + "!");
};
sayHello ("Trevor");
```
5. What would the following script log to the console?

  ```javascript
  var currentSong = "Call Me Maybe";

  function setSong(song) {
    currentSong = song;
  }

  setSong("Friday, Friday");

  console.log(currentSong);
  ```
"Friday, Friday"

6. What would the following script log to the console?

  ```javascript
  var add = function(a, b) {
    return a + b;
  }

  var result = add(3, 7);

  console.log(result);
  ```
10

7. What would the following script log to the console?

  ```javascript
  var helloGoodbye = function(name) {
    return sayHello(name) + " " + sayGoodbye(name);
  }

  var sayHello = function(name) {
    return "Hello " + name " !";
  }

  var sayGoodbye = function(name) {
    return "Goodbye " + name " !";
  }

  console.log(helloGoodbye("Sarah"));
  ```
  Technically, it'll be an error because there should be a + between the name and the " !" string in both sayHello and sayGoodbye. If it's fixed, it wil log:
  
  "Hello Sarah ! Goodbye Sarah !"

8. Write a function `findLongestWord()` that takes an array of words and returns the length of the longest one.
```javascript
function findLongestWord(array){
  var longestWord = 0;
  for(var i = 0; i < array.length; i++){
    if (array[i].length > longestWord){
      longestWord = array[i].length;
    };
  };
  console.log(longestWord);
};
```

9. Define a function `sum()` that sums all the numbers in an array of numbers. For example, `sum([1,2,3,4])` should return 10.
```javascript
function sum(nums){
  var total = 0;
  for(var i = 0; i < nums.length; i++){
    total += nums[i];
  };
  console.log(total)
};
```

10. Write a function that takes a character (i.e. a string of length 1) and returns true if it is a vowel, false otherwise.
```javascript
function vow (letter){
  newLetter = letter.toUpperCase();
  if (newLetter == "A" || newLetter == "E" || newLetter == "I" || newLetter == "O" || newLetter == "U"){
    console.log(true);
  } else {
    console.log(false);
  };
};
```

11. Write the correct line to make `"Woof!"` show up in the console based on this script:

  ```javascript
  var pet = {
    name: "Charles",
    goodDog: true,
    speak: function() {
      console.log("Woof!");
    }
  };
  console.log(pet.speak());
  ```

12. Using the same script as above, write the correct line to log the dogs name to the console.
console.log(pet.name);

## Command Line

### Questions

1. What is the command line and what is it used for? The command line is a way of interfacing with a computer via text input.
2. What does the command `ls` do? It prints all of the files and folders within the current folder.
3. What does the command `pwd` do? It prints the name of the current directory.
4. What does the following command do: `cd my-cool-project` Moves to the directory "my-cool-project"

### Exercises

1. Write the command to make a new directory called "my-cool-project". mkdir "my-cool-project"
2. Write the command to create a file called "index.html". touch index.html
3. Write the command to delete a file called "main.css". rm main.css

## Git

### Questions

1. What is Git and what is it used for? Git is a version control system used to track changes in files.
2. Whats the difference between a local repository and a remote repository? A local repository is saved on a local computer, a remote repository is stored on a network.

### Exercises

1. Write the command that you would use to create a new local Git repository. git init
2. Write the command to stage a file called `index.html` to be committed. git add index.html
3. Write the command to view the current status of the git repository. git status
