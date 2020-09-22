# Interactivity with Javascript

Introduction to use javascript with web pages.

[![Eloquent Javascript](https://eloquentjavascript.net/img/cover.jpg "Eloquent Javascript")](https://eloquentjavascript.net/)

> Notes from the course

## Week II

The functions and events

#### Functions

Functions are bits of codes that you can reuse. Whenever possible reuse built in functions.

Functions have a special syntax.

```js
function fnName(parameter1, parameter2, parameterN) {
    //code block to run
}
```

> Function call

- declaring a function is the initialization phase
- to start a function it needs to be `called`
- calling a function changes a `program flow`

> Parameters

- extra information to run a function
- function can take as many parameters as needed

> Return values

- sometimes it's important for a function to return a value
- it's possible to assign a function to a variable when it returns a value

#### Code placement

It's better to separate code from content.

> Places to put your code

- head section
- <script> tag in the head section or in the end of body
- external file (without a <script> tag)

> Debugging code

- browser's developer console is a good tool
- codepen and similar online tools

#### Folder structure

Important to organize files however it's different organizational ways are conventions not rules.

> Different files to put into separate folders

- HTML
- CSS
- images
- JavaScript

> Linking from an HTML file

```html
<link rel="stylesheet" href="css/style.css">
<script src="js/junctions.js"></script>
<img src="images/sunset.jpg"/>
```

> Linking from a CSS file

```css
background: url("../images/sunset.jpg")
```

#### Events

Events are used to make things happen.

> Adding interactivity

- functions and dynamic behaviour can be called after special events
- these events are inside Javascript API

> Specific events

- onclick
    - user clicks on an HTML element
- onmouseover
    - user moves the mouse over an HTML element
- onresize
    - browser windows is resized
- onload
    - browser finishes loading the page

> How it works

- any element can react to an event
- need to add the event to the tag and include a function to be called

```html
<div onclick="msg()">You have a new message</div>
```

> Using quotes

- possible to use single or double quotes
- better to make a convention and use double quotes inside html and single quotes in scripts
- also it's not possible to mix different quotes without using escaping characters

```html
<div onclick = "message('Hello world')">New message</div>
```

> The program flow

- events change the program flow
- events cause the program to `run continuously` since the DOM is always listening for events

> More events

- mouse events
    - onclick, onmouseleave ..
- keyboard events
    - onkeydown, onkeypress ..
- frame events
    - onload, onresize, onscroll, onerror..
- `developer.mozilla.org`

#### THIS keyword

`this` referrs to self object, function etc.

> Referring to elements

- a key to smart programming is using functions
- a common roadblock is figuring out how to set up functions for reuse

> "this"

- `this` is a keyword that allows an element to reference itself
    - every object in DOM has an automatically geneated `this`
- allows you to access an element's info
- `this` is also used outside of functions

```html
<div onclick="getElement(this)" id="firstDiv"></div>
```

```js
const getElement = (el) => {
    console.log(el.id)
}
```













