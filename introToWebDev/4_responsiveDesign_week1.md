# Advanced Styling with Responsive Design
[![HTML and CSS study resource](https://learn.shayhowe.com/assets/images/book/book-sm.png "Learn to Code by Shay Howe")](https://learn.shayhowe.com/advanced-html-css/responsive-web-design/)

Designing for multiple devices and screen sizes is part of a Responsive Design.

## Week I

#### What is responsive Design?

- designing your site for multiple devices
- adapting to user needs and capabilities
    - nowadays people use phone screens to do a lot of things - videos, music, text, games etc.

> Concepts to consider

- media queries
- flexible grid-based layout for relative sizing
- flexible images

#### Testing existing sites

Not practically possible to test site on all available devices. 

> How to test you site

- online tools (i.e. ami.responsivedesign.is)
- web browser compability tools (mobile view, resizing)

#### Benefits of responsive design

R.D. means different things to many people.

> 'Responsive' options

- Responsive Web Design (RWD) - fluid measurements, flexible grids and varying css rules
- Adaptive Design (dynamic serving) - returns one of multiple versions of a page based on the type of device
- Separate Mobile Site (.m) - separate mobile site url

> RWD (Responsive Web Design)

- is it responsive? - if the server is sending back the same code regardless of the device, you are using RWD
- this can be detected automatically, by looking for `meta name="viewport"`

> AD (Adaptive Design)

- server returns different code (html and css) depending on the device requesting the page.

> Separate URL

- server return different code on different URL depending on the device
- for search engines you can relate (tell) the different URL-s with the same site info with a `<link>` tag and `rel="canonical` and `rel="alternate"` elements. This is for SEO (search engine optimization).

> Why RWD is simpler?

- easier to share data with a single URL
- easier for search engines to index a page
- fewer files = less maintenance
- less redirection = faster load time

#### Fluid measurements

To design responsiveness you need to use dynamic units of measurement.

> Fluid measurement

- content should fit the size constraints of the `viewport`
- vertical scrolling is about content, horizontal scrolling is bad design

> Absolute measurements

- px
    - one device pixel (devices differ)
- mm, cm, in
    - for printing out pages
- pt
    - one point is 1/72 of inch
- pc
    - one pica is 12 points (pt)

> Relative measurements

Relative measurement are for 

- relative measurements are `relative` to some other element value
- `%` - relative measurement of a parent element (nesting)
- `em` - font size of parent element (nesting)
- `rem` - font size of root element (in html page it's <html> element - no nesting)
- `vw`
    - viewport's width, 1 vw = 1/100th of the width of the viewport (once it was done with JS)
- `vh`
    - viewport's height, 1 vh = 1/100th of the height of the viewport
- `vh` and `vw` comes in handy to set headers and footer into position

Good article about mixing absolute and relative measurements for responsive design:
https://css-tricks.com/rems-ems/

What are the differences in px, em, rem:
https://www.futurehosting.com/blog/web-design-basics-rem-vs-em-vs-px-sizing-elements-in-css/





