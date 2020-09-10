# Introduction to CSS

> Notes from the course

[![HTML and CSS study resource](https://learn.shayhowe.com/assets/images/book/book-sm.png "Learn to Code by Shay Howe")](https://learn.shayhowe.com/html-css/)

This course has 4 weeks of study material.

- Week one
	- Syntax and how to use
	- Simple positioning
- Week Two
	- The Box model
	- Styling links and lists
	- Advanced selectors
	- Browser capabilities
- Week Three
	- Pseudo classes and Elements
	- Transitions
	- Transforms
	- Positioning
- Week Four
	- Samples styling a table
	- samples of styling a nav menu

### Week I

HTML is to define and structure the document contents while CSS is for presentation - styling appearance of content.

#### Cascading Style Sheets

CSS - defined generic rules that can apply to multiple elements.

> Syntax

.

```sh
selector {
    property: value;
}
```

For setting heading.

```sh
h1 {
    color: red;
}
```

> Browser Styling

- same html may look different on other browsers
- browsers have default styles

 > Rule syntax
 
 - brackets and semicolons are important
 - good editor can help you with syntax

> Adding style

One way is to add it into HTML element but it's not recommended anymore.
```sh
<h1 style="color: red">
    Styled Heading
</h1>
```

> Internal Style Sheet

- styling defined within `<head>`
- rules are defined within `<style>`
- styles are applies to all elements in that file

```sh
<head>
    <meta charset="UTF-8">
    <title>Site with CSS</title>
    <style>
        h1 {
            color> red;
        }
    </style>
</head>
```

> External Style Sheet

- rules in an external file
- a link to the style sheet is put in the head section

```sh
<link rel="stylesheet" href="style.css">
```

> Cascading part of CSS (order of applying)

In here the nr 1 is the most important for browser.

- 4 `browser default`
- 3 `external` style sheet
- 2 `internal` style
- 1 `inline` style

> Rule precedence

If one selector is defined in 2 different files then the rules from the most recent file have precedence.

If one selector has more than one rule in the same file then the last rule defined or most recent rule has precedence.

Its possible to `override` the rules precedence. It's done with the `!important` value.

```sh
h1 {
    font-family: Arial !important;
}

h1 {
    font-family: Times;
}
```

#### Colors

asda




















