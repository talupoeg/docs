# Interactivity with Javascript

Introduction to use javascript with web pages.

> Notes from the course

## Week I

The introduction to connecting Javascript with the web.

#### The DOM

DOM is the document object model - a mathematical tree like structure of all the elements on the page.

> Javascript and the DOM

Javascript is used to access the web page elements through DOM.

> How does it work?

- accessing the DOM is done through and API - application programming interface
- API is a layer, an interface to access javascript functions and language specifics

> The DOM objects/elements

- document - the root of the page
    - document.URI, document.baseURI, document.height, document.links, document.bgColor etc.
- element - a node in the tree
    - returned by a member of the API
- nodeList - an array (group) of elements
    - `document.getElementByTagName("p")` would return a set of nodes
- attribute
    - a node in the DOM, though rarely used that way. Another way to manipulate/change the document. (for <img> there's a `alt`, `src` etc.)

> Specific APIs

- document.getElementById(id)
- document.getElementsByClassName(class)
- element.innerHTML
- element.style
- element.setAttribute(attribute, value)
- element.removeAttribute(attribute)

#### Output

To print out to screen and make things happen.

> Interactivity

- html5 and css3 are not really interactive
- new elements and pseudo-classes can only go so far

> What can JS do?

- read and write HTML element
- react to events (mouse, keyboard etc)
- validate data
- detect visitor's browser info
- create cookies

> Javascript output

- javascript doesn't have a built-in print function
- data is displayed via
    - an alert box using `window.alert()`
    - a prompt using `window.prompt()`
    - HTML output using `document.write()`
    - HTML element using `innerHTML`
    - the browser console using `console.log()`

> alert()

Simple pop-up alert fn.

```js
alert('I approve this message!');
```

- pop-up window that displays information

> document.write() and ..writeln()

This is to replace a whole page content.

```js
document.write('This is the new information now')
```

- write "permanently" to the page and replace all previous content
- not good to use as it can be misused
- only for learning to write code

> innerHTML

For replacing content inside DOM elements (html elements).

```js
element.innerHTML = "Time to learn stuff";
```

```js
document.getElementsByTagName('p')[0].innerHTML = 'Hello world'
```

```js
document.getElementsById('myElement').innerHTML = 'This is the new content';
```

- can use innerHTML with combination to element you want to change

> Developer tools

Best way to test and experiment with code

#### Variables

Variables is for saving data.

> Storing data

- in js data is stored in variables
- to use a variable you have to declare it

```js
var name;
let name2;
const pi;
```

> Variable names

- consists of letters, digits, underscores and dollar sign
- can not start with a digit
- are case-sensitive
- should be mnemonic (meaningful)

> Variable assignments

- variables can be assigned a value with a `=` sign

```js
let plant = 'boletus mushroom';
...
plant = 'chanterelle mushroom'
```

> Using a variable

```js
let name = prompt('Favourite mushroom');
document.writeln(name);
```

#### Data types

In JS a variable can take on many different types. I.e. it's loosely typed language. Many other programming languages are strictly typed. That is variable types need to be declared with variable declaration.

```js
var peronsName = prompt('What is your name');
var fullDate = Date();
var path = window.location;
```

> Number

- numerical value
    - with or without decimals

```js
let width = window.innerWidth;
const pi = 3.14;
```

> String

- collection of characters
- string value is to be put in quotes `""`

```js
let location = window.location;
let myFamily = "Foxies";
```

> Boolean

Value is either `true` or `false`

```js
let status = false;
status = window.closed;
```

> Object

- more complex and structured value
- a node in the DOM is a type of object
- nodes are more than a single value, they have attributes.

```js
let topic = document.getElementById('topicId');
```

> Array

- collection of values
- array stores multiple values using a variable name and an index for each element in the array

```js
let links = document.getElementsByTagName('a');
let firstLink = links[0];
```

#### Operators and Expressions

Often times you write your code by typing statements.

> Statements

- Statements are code lines, in JS case lines ending with a semicolon
- statements also have `expressions`, which can be evaluated (väärtustatud, arvutatud) like `2%5` or `x == 12`
- expressions produce values, often times `boolean values`
- expressions produces values with the help of operatos

> Arithmetic operators

These expressions are evaluated to a numeric value

```
Operator    Example statement   Value stored in x
+           x = 2 + 5           7
-           x = 5 - 2           3
*           x = 2 * 5           10
/           x = 5 / 2           2.5
%           x = 5 % 2           1
++          x = 5               5
            x++                 6
--          x = 12              12
            x--                 11
+=          x = 2               5
            x += 5              7
```

> Boolean operators


Example x value is `12`
```
Operator    Example expression  Returns
==          x == 5              false
==          x == 12             true
!=          x != 5              true
==          x == "12"           true
===         x === "12"          false
!==         x !== 12            false    
```

> Logical Operatos

Assume `x = 12`

```
Name    Operator    Example expression      Returns
and     &&          (15 > x) && (x > 5)     true
or      ||          (15 > x) || (x > 5)     true
not     !           !(x == 12)              false
```
