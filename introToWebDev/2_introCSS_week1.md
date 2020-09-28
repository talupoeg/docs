# Introduction to CSS

[![HTML and CSS study resource](https://learn.shayhowe.com/assets/images/book/book-sm.png "Learn to Code by Shay Howe")](https://learn.shayhowe.com/html-css/)

This online book on the picture is a side resource and has more detailed descriptions and methods to learn html and css.

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

> Color conventions

- color names (blue, red, yello etc.) but should be avoided (browser differences)
- Hexadecimal is common convention
    - #0000FF, #FF0000, #FFFF00 (3 or 6 digits) - blue, red, yellow
- RGB
    - (0,0,1), (1,0,0), (1,1,0) - blue red, yellow
- RGBA
    - (0,0,1,.5) - 4th place is for alphatransparency

Different monitors show colors differently

> Accessibility

Appropriate use of color is critical to web accessibility. Many people are visually impaired or color blind than are legally blind.

> What is color contrast?

- You intuitively know when something has poor contrast
- there are tools that quantify the contrast between text and background
    - wave.webaim.org
    - webaim.org/resources/contrastchecker

> Review

- use web safe colors and use an accepted convention
- test your site using a contrast checker

#### Styling your text

> Options

- many ways to style your text:
    - font (family, style, variant, size)
    - color and background
    - alignment
    - line-height

> font-family

- font families are stues of text
- examples
    - helvetica, courier, comic sans ms

```css
body {
    font-family: Arial;
}

h1 {
    font-family: Courier, Impact, Arial
}
```

> font-family considerations

- some fonts are not as user-friendly, use sans-serif when possible

> Custom fonts

- to expand beyond "web-safe" fonts use @font-face

```css
@font-face {
    font-family: mySpecialFont;
    src: url('specialFont.ttf')
}

h1 {
    font-family: mySpecialFont;
}
```

> font-style

- normal
- italic
- oblique

> font-variant

- normal
- small-caps
- etc.

> font-size

- xx-small, x-small, small, smaller, medium, larger, x-large, xx-large, larger ..
- pixel sizes
- pt (point size)
- percentage (flexibility on different screen sizes)

> color and background-color

- color attribute is the color of the foreground (text)
- the background-color is the color of the background

> text-align

- left
- right
- center
- justify (spread out to use as much space as possible)

> line-height

- it doesn't affect font
- adjusts the space between the lines of text

```css
h1 {
    line-height: 50%;
}

h2 {
    line-height: 150%
}
```

#### Display and Visiblity part 1

> Display is Key to Layout

- every element is a box
- display affects the layout of neighboring elements on page

> Common display values

```css
p {
    display: inline;
}

h6 {
    display: block;
}

h6 {
    display: inline-block;
}

h6 {
    display: none;
}
```

- inline
    - sits next to other elements
    - takes up "just enough" width and height
- block
    - forces line break
    - default is taking up all horizontal width and "just enough" height
    - rules can ser height and width
- inline-block
    - best of both (inline and block)
    - same as inline so elements can be `next to each other` plus you can set `height` and `width`
- none
    - removed from page

> Complementary properties of 'display'

- float
    - reposition elements tho the right of left
    - elements are aware of one another and will not overlap
    - values: `left`, `right`
- clear
    - used to keep floating elements away
    - values: left, right, both
        - left - nothing is floating to set element's left side
        - both - nothing is floating to either side of the set element

```css
    p {
        height: 300px;
        width: 500px;
        float: left;
    }
    
    h4 {
        clear: both;
    }
```

#### Display and Visiblity part 2

Sometimes elements get hidden behind other elements or screen borders. It's possible to change the access to those elements.

> Element overflow

Four values of the `overflow`:

- visible
    - can cause text to show up "on top" of other elements
- hidden
    - hides anything that goes beyond bounding box
    - this may cause problems since if the user increases font size they may not be able to see contens
- scroll
    - gives horizontal and vertical scrollbars
- auto
    - adds scrollbars as needed

##### Other display values
New display properties are available to most recent browsers.

- Table
- Grid
- Flexbox

> `display: table`

```css

span .table {
    display: table;
}

span .el {
    display: table-cell;
}

```

> `visibility: hidden`

- specifies whether or not element is visible
- element isn't removed from html like with `display: none`

> Review

- `display` attribute is just one tool for positioning elements on the page
- early design will make coding easier
- utilize tools to see different options (inspect element in browser)


































