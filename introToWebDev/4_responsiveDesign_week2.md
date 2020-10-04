# Advanced Styling with Responsive Design
[![HTML and CSS study resource](https://learn.shayhowe.com/assets/images/book/book-sm.png "Learn to Code by Shay Howe")](https://learn.shayhowe.com/advanced-html-css/responsive-web-design/)

Designing for multiple devices and screen sizes is part of a Responsive Design.

## Week II

#### Media queries

Media query allow the style to depend upon the media properties (i.e. viewport size - width)

> CSS2.1 used media types:

```css
<link rel="stylesheet" href="style.css" media="screen">
<link rel="stylesheet" href="print.css" media="print">
```

> CSS3 media properties

CSS3 increased the capabilities. Style can depend on many features.

- `width`, `height`, `orientation`, `resolution` etc.
- `boolean operators` can also be applied to increase power

> `Media query has two components`:

- a media type
    - screen, print, all, ...
- actual query of a media feature and `trigger`
    - width, height, orientation, resolution, ...

```css
@media screen and (max-device-width: 480px) and (resolution: 163dpi) {
    margin: 0 auto;
}
```

> How to implement media queries

- usage of `@import` rule
    - ```css 
        @import url('smallstyle.css') screen and (min-width: 600px)
        ```
- putting media query directly in the style sheet
    - ```css
        @media screen and (min-width: 500px) {
            font-size: 1.2em;
        }
        ```

- including query in the link
    - ```css
        <link rel="stylesheet" media="screen and (min-width: 400px) and (orientation: protrait)">
        ```

> Example

Putting media query in the css file:

```css
@media screen and (min-width: 500px) {
    p.desc {
        display: block;
        font-size: 150%;
    }
}

@media screen and (min-width: 900px) {
    p.desc {
        display: inline-block;
        width: 35%;
        font-size: 125%;
    }
}
```

#### Wireframes

Wireframes provide visual representation of your layouts.

- http://www.wireframeshowcase.com/ 

> Decide before code

- what content (including graphical) is needed to have on the page
- what is the best layout for this material

> Mobile view

- most important step in web design is `the design`

> Functionality

- the design should be about more than layout
- it is possible to test the interaction as well (navigation, form inputs etc.)

> Sketches vs Wireframes

- best to start with a sketch and then move on to wireframe

#### Breakpoints

Breakpoints are sizes that define a change in your site layout or content.

> What is a `trigger`

Breakpoints trigger a change for the site. Breakpoints should correspond to devices and/or content. Devices have different screen sizes so breakpoints can relate to those particular sizes.

> Mobile first

- the design starts for smaller screens first
- shouldnt see breakpoints for small screens. The default styling already cores that.
- should have min-width instead of max-width

#### Media Queries part II

There are three steps to do responsive design.

> STEP 1 Grab information

- the `meta viewport tag` tells mobile browsers viewport how to behave

```css
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

Setting the viewport:
https://www.w3schools.com/css/css_rwd_viewport.asp

Also possible to disallow zooming or set the maximum zoom level on devices:

```css
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0">
```

> STEP 2 fluid layout

- if using breakpoints some absolute measurements are not unusual
- percentages vs ems
    - ems are measurement of typography, 1em is width of one letter M in current typeface
- paddings and margins affected by width not height

> Step 3 Media queries

- fluid layout that is triggered by certain sizes
- design for small screens and work bigger







