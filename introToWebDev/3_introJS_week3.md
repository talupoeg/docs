# Interactivity with Javascript

Introduction to use javascript with web pages.

[![Eloquent Javascript](https://eloquentjavascript.net/img/cover.jpg "Eloquent Javascript")](https://eloquentjavascript.net/)

> This online book on the picture is a side resource and has more detailed descriptions and methods to learn JS.

## Week III

Javascript arrays

#### Arrays

Arrays are collections of data. Data can be either number, string, object, boolean etc.

> Declaring an array

There are many ways to declare an array.

```js
var grades = [7, 3, 6, 9];
var foodz = ['apple', 'pineapple', 'watermelon'];
let images = document.getElementsByClassName('imgs');
var listItems = document.getElementsByTagName('li')
```

Elements are referenced by `index`.

```js
grades[0] // first element
grades[3] // 4th element
```

> Javascript Arrays are Objects

- that is arrays have attributes and methods

```js
grades.length
grades.sort()
grades.push(new_grade)
```

#### Javascript iteration (looping)

Retrieveing data from array is fast. Arrays can store a lot of data. We need some sort of mechanism to retrieve a lot of data fast and simple way.

> Iteration / looping

- to access all data in an array it's needed to loop over everything

`for loop`

```js
// 1 initial variable and value
// 2 boolean condition check whether to go to next cycle
// 3 initial value modification for the next loop
for (init = 0; init < 5; init ++) {
    // lets loop
}
```

#### Flow of Control

There are also decision points to control the `flow of execution`.

> Dynamic execution

- there are ways to put decision points into code
    - react to good/bad user input
    - way for a interactive program

> Flow of control

- break a program into blocks
- efficient algorithms execute only the blocks needed
- execution of these decision blocks is `flow of control`

`if statement`

- evaluates a `boolean expression` before performing an action (running a code block)
- if expression is true, execute code
- if expression is false, skip the execution

```js
if (n % 1 === 0) {
    // whole number - integer
}
```

> Blocks

- in javascript, statement enclosed in curly brackets `{}` are considered a single statement
- indentation is not required but important for readability

```js
// helper fn
// returns true if type is float
// 7.5 returns true
// 8737 returns false
// 
const isFloat = (n) => {
    return Number(n) === n && n % 1 !== 0;
}
```

#### Nested conditionals

Sometimes there are more conditionals needed.

`Nested if statements`

```js
if (boolean condition) {
    // another inner condition
    if (boolean condition) {
        // this code runs when both conditions are true
    }
}
```

`Nested if else statements`

- an else statement always matches the most recent open if statement
- indentation is of no importance over logic

```js
if (boolean condition) {
    // run if first condition
} else if (boolean condition) {
    // run if second condition succeeds
} else {
    // run if all else falsifies
}
```


 
