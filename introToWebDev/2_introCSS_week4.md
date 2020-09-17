# Introduction to CSS - WEEK 4

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

### Week IV

Week 4 consists of more code than theory.

#### Accessible navigation

Designing navigation bar for screen readers.

> Navigation

- critical aspect of accessibility
- blind and low-vision users rely on proper coding of page orientation

> For blind users

- Title of page lets you know what page you're on when page loads
- proper heading placement and hierarchy conveys organization of page and allows disabled users to skip navigation
- link descriptions convey content of page and organization of site

> Proper heading hierarchy

- Headings need to be properly nested to convey organization of the page
- <h2> tags follow the <h1> tag, the <h3> tags follow the <h2> etc.
 
> Off-page headings

- useful when you want to give SR (disabled) users a navigational aid without cluttering presentation
- use CSS to position headings off-page
- dont use display:none or visibility:hidden because for screen readers its not good

```css
.offPage {
    position: absolute;
    left: -1000px;
}
```

> Meaningful link text

- screen readers can find and list links
- description for the links must be meaningful out of context, via tabbing or presented in a list




