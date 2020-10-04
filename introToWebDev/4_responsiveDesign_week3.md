# Advanced Styling with Responsive Design
[![HTML and CSS study resource](https://learn.shayhowe.com/assets/images/book/book-sm.png "Learn to Code by Shay Howe")](https://learn.shayhowe.com/advanced-html-css/responsive-web-design/)

Designing for multiple devices and screen sizes is part of a Responsive Design.

## Week III

#### Frameworks

Frameworks in font-end provide simpler CSS, JS tools to use.

> Popular front-end frameworks

- Bootstrap
- Foundation by Zerb
- Semantic UI
- Pure by Yahoo .. etc

> Ways to build your site

- use templates either written by you or others
- use frameworks where lots of functionality has been written for you
- write your own code and experiment fully

#### Twitter Bootstrap 

It's a framework to create websites. Focuses on responsive mobile first design. It consists of CSS and HTML templates. Plus some JS extensions. It uses interfaces and layouts as its tooling set.

> Bootstrap 3..

- uses 12-column grid system
- helps with spacing issues and has responsive design
- it has common jQuery functionalities:
    - accordion, drop-down, carousel
- familiar look and feel (forms look standardised etc.)

Some `PROS`:

It's helpful to use a Bootstrap framework becuase it speeds up development. It is platform independant, responsive by default and also customizable.

Some `CONS` are that it might not follow best practises in coding standards. Content and layout are intertwined. It also acan be resource heavy and looks are generic.

> Two ways to use bootstrap

- a supplement to your style
- a theme that you can expand upon

#### Bootstrap breakpoints

Bootstrap has hardcoded breakpoints for different viewports. It's intention is to use the mobile-first paradigm. It plans for the smallest screen size first and after then when screen gets bigger it makes changes to layout.

> Extra small devices in Bootstrap fw

- xs-
- any device that has a minimum width of 480px

> Small devies

- sm-
- minimum width of 768px

> Medium devies

- md-
- minimum width of 992px

> Large devies

- lg-
- minimum width of 1200px

> Check newer Bootstrap version documentation for extra values

> Custom breakpoints

- it's possible to change default values
- either write your own media queries or customize .css files

#### Bootstrap Grid system

The Bootstrap layout is based on a 12 column grid. 

> Grid classes

- every grid consists of
    - a container
    - a row
        - one or more column classes
        - col-xx-yy (xx - `vieport size`, yy - `# of columns`)

```html
<div class="container">
    <div class="row">
        <div class="col-md-6">
```

> Positioning classes

- on viewport md and up, there is and option for push and pull class
- `-col-xx-push-yy` - move yy columns to the right
- `-col-xx-pull-yy` - move yy columns to the left

> Responsive utility classes

- `hidden-xx` - content will only be hidden on the xx screen size
- `visible-xx` - content will only be visible on the xx screen size
- `sr-only` - content is hidden on all devices except screen readers










