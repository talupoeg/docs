# Introduction to CSS - WEEK 3

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

### Week III

HTML is to define and structure the document contents while CSS is for presentation - styling appearance of content.

#### Pseudo classes and Elements

These elements and classes are not in DOM tree but still dependant on it.

`Pseudo-Classes`

https://learn.shayhowe.com/advanced-html-css/complex-selectors/#pseudo-classes

- Elements that are dynamically populated or dependant on tree structure
- e.g. a:hover

> Types of Pseudo classes

- link
    - :link, :visited
- user action
    - :hover, :active, :focus
- forms (interfaces)
    - :enabled, :checked, :disabled
- structural/positional
    - :first-child, :last-child, :nth-child(), :only-child
    - :first-of-type, :last-of-type, :only-of-type

`Pseudo elements`

https://learn.shayhowe.com/advanced-html-css/complex-selectors/#pseudo-elements

> Types of Pseudo Elements

- textual
    - :first-letter, :first-line
- positional/generated
    - :before, :after
- fragments
    - ::selection

#### Transitions

Changing element from one state to another or even animating any propertie of an element.

- When elements transition from one state to another, you can alter their appearance
- if hovering over the link change the color, size etc.

> Transition properties

- transition-propperty
    - what needs to be changed? (size, color, position etc.)
- transition-duration
    - how long should each transition last
- transition-timing
    - should it be a smooth transition (linear) or different
- transition delay
    - how long should the wait be before the transition begins

> Setting up

1. `Define your element`
2. `Choose the elements for transition`
3. `Define the new values`
    - must combine this step with a pseudo-class

`1. step`
```css
div {
    color: #000;
    background: #234224;
    line-height: 200px;
    text-align: center;
    width: 250px;
    height: 200px;
    border-radius: 6px;
}
```

`2. step`

```css
div {
    transition-property: color, width, background, border-radius;
    transition-duration: .5s;
    transition-timing-function: linear;
    transition-delay: .5s;
}
```

`3. step`

```css
div:hover {
    color: #fff;
    width: 350px;
    background: #2D31B3;
    border-radius: 50%;
}
```

> Transition shorthands

- if multiple properties transition, it's possible to use a shorthand

```css
div {
    transition: background .2s linear, border-radius 1s ease-in 1s;
}
```

#### Transforms

Transforms are similar to transitions. Possible to change in 2D and also in 3D. Transforms will give the result of moved or transformed element however it's still possible to combine it with transitions to animate element properties.

https://learn.shayhowe.com/advanced-html-css/css-transforms/

> 2D Transform Options

- translate
- rotate
- scale
- skew
- matrix

`Translate`

Way to move element around on it's X and Y coordinate. transform: translate(`x, y`)

```css
.box-1 {
    transform: translate(100, 75);
}
```

`Rotate`

Rotate or spin the element a certain number of degrees. 
transform:rotate(`deg`)

```css
.box-1 {
    transform:rotate(30deg);
}
```

`Scale`

Scaling the element - changing the size.
transform:scale(`width: height`)

```css
.box-1{
    transform:scale(2, 3);   
}
```

`Skew`

Rotate the element a certain number of degrees along the x and y axis. transform: skew(`x-angle, y-angle`), transform: skewX(X-angle) etc. It's to distort elements on the horizontal, vertical or on both axis.

```css
.box-1 {
    transform: skew(5deg, -20deg);
}
```

`Matrix`

Combining all of the 2D transform methods into one

> 3D Transform options

Possible to rotate along the x, y and z dimension along a given degree.

https://learn.shayhowe.com/advanced-html-css/css-transforms/#three-dimensional-transforms

transform: rotateY(`deg`)
transform: rotateX(`deg`)
transform: rotateZ(`deg`)
transform: rotate3D(`x, y, z`)


#### Positioning

Probably the most time consuming task on a page is to position elements correctly.

> Position properties

- static
- relative
- absolute
- fixed

`Static`

- Default position value for elements
- browser will put the element in the next available position
    - if span it will put next to other span element, if block then to next available free row
- not affected by the `top`, `bottom`, `left` and `right` properties

`Relative`

- positioned 'relative to itself'
- similar to static however it adds offsets
- it still gets put to next available free space but it's possible to set a new position relative to it's original position with offsets:
    - `top`, `bottom`, `left`, `right`
- so the NEW POSITION does NOT affect any other element and it leaves a hole to it's original position
- relative positioned elements are often used as container blocks for other elements

`Absolute`

- element is removed from the document flow and positioned relative to it's `nearest ancestor` (or the root document, not the browser window) 
- other elements behave as if absolutely positioned element does not exist
- can end up on top of another element

`Fixed`

- relative to the browser window
- fixed position can follow scrolled window
- IE7 and IE8 support the fixed value only if a !DOCTYPE is specified
- popup boxes which wont go away
- navi bar that is always visible while scrolling





























