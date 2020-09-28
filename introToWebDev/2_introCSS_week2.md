# Introduction to CSS - WEEK 2

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

### Week II

HTML is to define and structure the document contents while CSS is for presentation - styling appearance of content.

#### Box Model

Box model is a general concept in CSS. The height and width of any element.

> Width and Height

- the default width of inline elements is the content
- elements that are not inline can take width and height properties

> Border

- any element can have border around it
- border properties specifies width, style and color
- border style must be specified

> Border style

- none, dotted, dashed, solid, double, groove, ridge, inset, outset, hidden

> Border color
- name, RGB, HEX, `transparent`

> Margin

- margin is space outside your border
- positive margin - element moves right/down
- negative margin - element moves left/upward

> Padding

- padding is additional space between the element and its border
- CSS does not support negative padding

Margin and padding wont take any color. These are always transparent space.

> What is the width and height of an element?

The width of an element is including the padding, margin and border width of the element also on both `two sides`.

```css
div {
    width: 100px;
    height: 50px;
    padding: 10px;
    margin: 5px;
    border: 1px solid black;
}
```

- width of the above div is `132px`
- height of the above div is `82px`

> Centering an element (not text)

- to horizontally center an element:
    - `margin: 0 auto;`
    - must `display: block;`
    - must `not float`
    - must `not have a fixed or absolute position`
    - must have a `width that is not auto`

> box-sizing

- `box-sizing` takes some of the "math" out
- options:
    - `content-box`: default additive
    - `border-box`: width takes content, padding and border into consideration (if you set element to `width: 200px` then the element is goint to be 200px minus padding and border)
    - it's not taking margin into account

###### Example

```css
.div1 {
    width: 300px;
    height: 100px;
    border: 1px solid blue;
    box-sizing: border-box;
}

.div2 {
    width: 300px;
    height: 100px;
    padding: 50px;
    border: 1px solid red;
    box-sizing: border-box;
}
```

The result will be 2 equivalent width boxes.

> Measurement

- absolute
    - set to a specific size
        - px, pt, mm, cm
- fluid
    - sets size relative to surrounding elements
        - %, vh, vw (viewport height and width)
        - em (for font)
            - 1 em is current size, .75 is 75% of the current size
        - rem (for font)
            - 1 rem is current size of root element

#### Styling links and lists

> Anchor Links

- links can take on all of the usual styles as well as `text-decoation`

```css
a {
    display: block;
    font-weight: bold;
    color: #343434;
    background-color: #676576;
    width: 200px;
    text-decoration: none;
    text-align: center;
    padding: 4px;
}
```

Above code looks like a button, but it's actually a link. For semantic purposes it's better to use a `<button></button>` instead.

> States

- some links are blue, purple etc.
    - `a:link` - a normal, unvisited link
    - `a:visited` - has been visited
    - `a:hover` - hover state (on touch screen not working)
    - `a:focus` - focus state with tabbing/clicking
    - `a:active` - while clicked, activated

> Precedence of state elements

- `a:hover` must come after `a:link` and `a:visited`
- `a:active` must come after `a:hover`

So the correct order should be:

```css
 /* unvisited link */
a:link {
  color: green;
}

/* visited link */
a:visited {
  color: green;
}

/* mouse over link */
a:hover {
  color: red;
}

/* selected link */
a:active {
  color: yellow;
}
```

> list-style-type

Style an unordered list with alpha-numeric and uppercase letters:

```css
ul {
    list-style-type: upper-alpha;
}
```

> list-style-image

Possible to replace the standard list style graphics with custom image. If `square` is not found then use custom image:

```css
ul {
    list-style-image: square url('icon.gif')
}
```

#### Advanced selectors

Simple selectors are h1, p, a, section etc. These are called `type` selectors. There are more ways to style specific elements or parts of elements.

> CSS selectors

Some selectors follow the DOM (DOM brakes up your page in a tree like structure)

`Descendant selectors`

```css
nav a {
    color: red;
}
```

- Can style all the anchor links inside a `nav` tag even when a tags are inside another tag.
- Intermediate tags between parent and child are allowed (nav -> p -> span -> a)

`Child selectors`

```css
nav > a {
    color: blue;
}
```

- More constraining than descendant selector.
- The anchor elements must be a child of the nav and no intermediate tags in between.
- Intermediate tags between parent and child are not allowed (nav -> a) while (nav -> p -> a) is not styled with this selector.

`Adjacent siblings selector`

```css
h2 + ol {
    margin-left: 10px;
}
```

- Elements must be at the same level and follow each other

`id selectors`

```css
#bottom_form {
    border: 1px solid gray;
}
```

- used to identify single element in the DOM
- there's a small movement to move the 'id' out of css

`class selector`

```css
.thumb {
    width: 15%;
}
```

- used to identify an element in the DOM that is part of special class of items
- like thumbnail images, all of the links that are in the navigation etc.

> classes vs. id's

- syntax is `.` vs. `#`
- classes can be used multiple times
- id should be unique

`Narrowing the scope selector`

When pages grow more complex you'd want to narrow the scope of the action.

```css
p.main {
    font-style: normal;
}
```

- here only the paragraphs which use the class "main" will be styled
- there can be other elements with class "main" but if these elements are not paragraphs then those are left alone

```css
header img.special {
    display: block;
}
```

- here only the images which use a class "special" and also are inside <header> tag as descendants are styled. NB! <img> tags can also be inside another element but those elements need still be inside <header>.

`Expanding the scope selectors`

```css
p, h1, #main, .special {
    font-weight: 900;
}
```

- rules apply to all the elements
- when there are multiple rules for the same selector then `most recent will be used` unless a rule has `!important` defined

`Universal selectors`

```css
* {
    color: black;
}
```

- will style all the elements on the page

`Attribute selectors`

```css
a[href="temp.html"] {
background-color: red;
}
```

- will style an element with defined attribute
- more useful with js coding
- could select all the images that use 'gif' files or links which go to gov sites etc.

> Using Operatos in attribute tags

Operators can be used to find attribute values you are looking for.

- `^` - match the beginning exactly
    - `a[href^='http://gov']`
- `$` - match the end exactly
    - `img[src$='.png']`
- `*` - wildcard, match all in any part
    - `a[href*='government']`


`Pseudo-Classes`

https://learn.shayhowe.com/advanced-html-css/complex-selectors/#pseudo-classes

`Pseudo-Elements`

https://learn.shayhowe.com/advanced-html-css/complex-selectors/#pseudo-elements

#### Browser Capabilities

Even modern browsers display content differently.

> Browser differences

- easiest to deal with differences in various browsers is to use a default style sheet (css reset)

> Handling unsupported porperties

- not all browsers support HTML5 tags
- not all browsers support CSS3 properties
- browser prefixes (vendor prefixes) provide a quick fix for handling unsupported CSS3 options

> Browser prefixes

- `-webkit-`: Android, Chrome, iOS, Safari
- `-moz-`: Firefox
- `-ms-`: Internet explorer
- `-o-`: Opera

> Often unsupported properties (2015)

- column-count
- border-radius
- gradient
- site 'caniuse.com' will tell you when you need to use prefixes

> Automate prefixes

- editor plugins
- external programs/scripts etc.

#### Designing for Accessibility

Using the P.O.U.R. principle.

> Perceivable

- provide text alternatives for images
- provide captions and transcripts for video and audio
- use correct semantic markup so content can be presented different ways
- make it easier for users to see content by using good color contrast

> Operable

- all the information should be available from keyboard
- users should have control over timing and limits
- dont use flashing content on pages
- provide ways to navigate, find content and where they are on the page

> Understandable

- economical and plain use of language
- text supplemented with illustrations, videos and other formats
- navigation, information structure are discernable(eristatav) and consistent
- make pages operate in predictable ways

> Robust

- site needs to be functional across various technologies (smart phones, screen readers, laptop, pensticks etc.)
- syntax errors that dont affect visual presentation may hamper assistive technology and tools
- adhering to W3C standards ensures future compatibility
- validate code in vavlidator.w3c.org and wave.webaim.org
