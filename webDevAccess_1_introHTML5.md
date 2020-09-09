# Web developer beginner course

[![HTML&CSS](https://learn.shayhowe.com/assets/images/book/book-sm.png)](https://learn.shayhowe.com/html-css/)

> Notes from the course

This course program has 5 courses worth of study material
  - course 1 - intro to HMTL5
  - course 2 - intro to CSS3
  - course 3 - interactivity with javascript
  - course 4 - advanced styling with responsive design
  - course 5 - web design capstone

## Course 1 - Introduction to HTML 5
### Week I
---
#### 1. HTML 

HTML was invented in 1990 to connect hyperlinks with documents.

Groups that "run" the Internet or the Web:
- Internet Engineering Task Force (IETF)
- World Wide Web Consortium (W3C)
- The Web Accessibility Initiative (WAI)

2005 - 2008 was the era where HTML files were accompanied with CSS files as a new standard.


| Year | Tech |
| --- | --- |
| 1993 | HTML1.0 |
| 1995 | HTML2.0 |
| 1996 | CSS1 |
| 1997 | HTML3.2 |
| 1998 | HTML 4.0 |
| 1998 | CSS2 |
| 1999 | HTML 4.01 |
| 2012 | HTML5 |

HTML5 is a cooperation between W3C and WHATWG (Web Hypertext Application Technology Working Group).

They established guidelines:
 - new features should be based on HTML, CSS, the DOM and Javascript
 - reduce the need for external plugins (e.g. flash)
 - more markup to replace scripting
 - HTML5 should be device independent
 
To Review:

- Browsers translate HTML documents into viewable webpages
- HTML was intended to facilitate content types (pictures, links, lists etc.)
- new standards are written to handle new requirements and browsers adopt the new standards

#### 2. How it Works
.
> Request-response cycle

- servers
- clients

Clients are requesting resources from servers through web browsers URL field. It has the protocol part, domain (server) and document which is optional to define.

> Different protocols

HTTP, HTTPS, FTP

> Domain names

Different domain names (school.edu, wikipedia.com) are mapped to an ip address.

> Document

Optionally it's possible to access a resource through a document. Normally there's a default document to return through url address.

> The Request

Once IP address is determined the browser creates an HTTP request. In this request there are lots of hidden request data like header, cookies, form data etc.

> The Response

The server returns files, not "web pages". It is up to browser to decide what to do with those files (css, js, xml etc.)

If the server can't fulfill the request it will send back files with server response error codes: 404, 500 etc.

### Week II
---
#### 1. Document Object Model (DOM)

The DOM is a tree like structure.

![DOM](https://www.w3schools.com/js/pic_htmltree.gif)

> DOM and HTML5

The DOM provides common tree-like structure that all pages should follow.
The basis of HTML5 is "New features should be based on HTML, CSS, the DOM and JavaScript...".
Computer scientists love trees (mathematical kind) because you can test them.

> Three parts of a well-formed document

1. Doctype
  1.1. version of HTML that you will be using
2. Head
  2.1 Metadata
3. Body
  3.1 Displayable content

> Doctype

- HTML5
    - `<!DOCTYPE html>`
- Previous versions dictated backwards compatibility

> Head

- Additional information used by the browser
    - Meta data - language, title
    - Supporting files - javascript, styling, add-ons
- other than title, meda-data is not displayed

> Body

- Bulk of your page
- Important to write well-formatted (tree-like) code
- Most of the content is displayed by the browser but there may be some meta-data too

###### To conclude

- Well-formed pages use the DOM structure
    - use beginning and end tags
    - close inner tags before outer ones
    - use valid attributes
- browsers will fix bad code, but not always well. Use validator to check your code

#### 2. HTML elements

Tags have a beginning and an end. Some tags have self closing tags like <img /> and also attributes like src, alt etc.

##### HTML5 tags and syntax
###### .

> Display

One of the most important attributes of an element is its display. Two most common are:

- block
    - block can take width and height
    - newline character is inserted before and after, e.g. it "Takes up" whole width
- inline
    - can no take width and height
    - only uses as much space as needed to contain the element

> Common Tags

- Headings (block)
    - h1, h2, h3, h4, h5, h6
    - these tags have syntax and semantics
    - semantics means h1 has greater importance over h2 etc.
- Paragraphs (block)
    - p
    - should only contain inline elements
- Divs (block)
    - div
    - generic section that is larger than a paragraph

> More Tags

- ordered list
    <ol>
    <li></li>
    </ol>
- unordered list
    <ul>
    <li></li>
    </ul>

- line break
    <br />
    - line breaks in source are ignore by browser unless there's a <br> tag

> Images

- Images (inline)
    <img src="picturefile.jpg" alt="aPic">
    <img> tag is taking attributes like src, alt, title, class, id etc.

> More attributes

- class
    applies sepecial properties to groups of elements
- id
    specifies a unique id to one element on the page
- style
    specifies a certain visual style (to be avoided)
- accesskey
    a shortcut key to activate an element
- tabindex
    the order elements will come into focus using the tab key
    - high tab index is a small number. So tabindex="1" is the highest priority

> special Entities

- < : &lt;
- \> : &gt;
- & : &amp;

##### Semantic tags
###### .
> How to design

- the most important in design is to think about the page design/layout before you start to code.
- once there was just a div to group things together and make a page layout
    - <div class="header"> ...
    - <div class="section"> ...
    - <div class="footer"> ...

In HTML5 there are more semantic tags to make up a layout of page content.

- <header></header>
    this is good for many types and sizes of screen readers where semantic tags have a special meaning
- <nav></nav>
    - links of your site for navigating the page
    - often found in the <header> tag
    - there's a debate whether the <ul> should be in the <nav> tag however links should be definitely inside <nav> tag
    <nav>
    <ul>
    <li><a href="">Home</a></li>
    <li><a href="">About</a></li>
    </ul>
    </nav>

- <figure>
    - more semantics than <img> tag has
    - can include caption and many multimedia resources
    <figure>
    <img src="" alt="" />
    <figcaption> A sunset over lake Pukaki</figcaption>
    </figure>

- there are way more HTML5 tags which have many kinds of attributes
    - structural elements
    article, aside, main, menuitem, summary, section
    - form elements
    datalist, keygen, output
    - input types
    color, date, email, list
    - graphics elements
    canvas, svg

#### 3. Images

There are many kinds of file types supported like JPEG, GIF, PNG. SVG and BMP are additional options.

##### HTML5 images
###### .

- every image must be downloaded so size can be a factor
- image files need to have a file extension (.jpg, .png etc.)
- every image requires an http request

> Image sizes

- when linking to an image the browser displays the image as big or small as the file (in bytes)
- quick solutions are to change file, use width/height attributes

> Using editor

- editors change images permanently
- only works on local files


> Using attributes

- <img> tag can include size and widht attribute
- normally its not a good idea to use style attributes however in img it's forgivable at times

> Favicons

- can put image/logo/icon next to the title of your page (in the tab) 
- must go in <head> section
    - <link rel="icon" type="image/png" href="img/logo.png" />

> Alternative text attributes

- provides contextual alternative to non-text content
- read by screen readers
- displayed in place of images if image unavailable
- provides semantic meaning to search engines

> Good alt text

- be accurate
- be succint (mõttetihe)
- not to be redundant (liialdatud)
- specific and distinct

> Font-awesome

- good to use however also important to put "aria-label='label name'" attribute inside <a> tag to reference an otherwise empty link, because <i> tag which the Fontawesome uses is not a proper text 

#### 4. Hyperlinks

##### Anchor links
###### .

<a href="asdad">A great link</a>

- tha <a> tag stands for anchor
- needs a hyper-reference (href)
    - href: reference to location of new content
- needs content:
    - content: the clickable part (text or image)

> Types of links

- Absolute links
    - full url with http://
- Relative links
    - file name or relative path or with hashtag to link to a local page location
- Internal links
    - local page links connected by id tag and hashtag
- Graphical links
    - can put <img> tag inside anchor tag

> Targets

- Anchors can take target attribute
    - _self - default action
    - _blank - open in new tab
    - _top and _parent

#### 5. Multimedia

##### Video and audio on webpage
###### .

> Video element <video>

- video tag uses src attr or embedded <source>
- common attributes:
    - height, width
    - autoplay
    - loop
    - controls
- text inside <video>..</video> is displayed if browser can not support the tag

> Audio element <audio>

- Audio tag uses a src attribute to link to audio file, typically .mp3 or .wav
- common attributes:
    - autoplay, controls, loop
    - buffered
    - muted
    - volume

> Setting clips

You can set both the video and audio elements to play clips by adding to the src attribute

- .ogg#t=5, 25
- .mp3#t=, 39
- .mov#t=, 1:38:45
- .mp4#t=15

> Plugins

- before HTML5 there was no standard for video display, plugins were required

> Accessibility issues

- make sure to provide links to plugins
- include text descriptions and closed captions
- multimedia should enhance not distract

#### 6. Tables

##### Using tables in HTML5
###### .

Tables should only be used for tabular data.

> Design

- sketch your layout before you code
- decide on the number of rows and columns
- decide if any rows/columns will span multiple cells

> The tags

- <table> - the container
- <tr> - the rows
- <th> - table heading
- <td> - columns or cells of table

> Spanning the rows or columns

- attributes rowspan or colspan

> Captions

- possible to use a heading <h2>, <h3> etc but it doesn't provide semantics
- better to use <caption>

#### 7. Useful tags

##### Some of the most useful tags
###### .

> Choosing your tags

- generic tags: p, div (block)
- semantic: header, nav, footer, figure (also block type)

> Block tags (display: block)

- containers: <article>, <aside>, <section>, <main>, ...
- <hr>
- <address>
- <blockquotes> - has `cite` attribute
- <details> with <summary>

> More tags with special or dynamic content or functionality

- <button>
- <meter> with attributes `min`, `max`, `value`
- <progress>
- <iframe>
- <bdo> attribute `dir` (ltr or rtl)
    - bi-directional orientation
- <map> with <area> creates 'clickable element in image' but needs script

### Week III
---
#### 1. Accessibility

Human factors to consider in web design.

##### Web as accessible as possible to others
###### .
Designing web without flashy contents, easy to understand.

> Overview

- learning what a web accessibility professional does
- understanding how disabilities relate to the web
- introducing the four principles of accessible interface design

> Web accessibility coordinator

- helps guide policy and purchasing decisions
- evaluate web interfaces for accessibility
- assists those with disabilities to access online infrastructure
- keep pace with changing technology

> How disabilities relate to the web

- 1 in 5 people have disability in US
- out of 60 million half are impeded using internet
- disabilities:
    - visual issues
        - blindness, low-vision, color-blindness
        - 8 million in US have difficult reading ordinary newsprint (even with glasses)
        - 1.8 mil. are completely blind
        - need to think of font size, color-contrast, font-style
    - hearing issues
        - partial to total deafness
        - 8 mil have difficult hearing normal conversation
        - 1 mil are completely deaf
        - need to think of closed-captioning
    - motor issues
        - inability to use a mouse or physical keyboard, slow response time, limited fine motor control
        - dexterity (käteosavus) issues 8 mil in US have difficult using their arms or hands
        - think of "tab" through your page
    - cognitive issues
        - learning disabilities, distractibility, dyslexia, inability to remember or focus on large amoounts of information
        - adults with ADD/ADHD: 16 mil in US
        - 38% of soldiers, 31% of Marines and 49% of National Guard members returning from combat report psychological contitions such as TBI and PTSD
        - cognitive disabilities number greater than physical and perceptual disabilities combined

###### More stats

- 8.3% in US have 2 or more disabilities
- 40k in US are both deaf and blind
- 41% of adults 65 and older have disability
- 8.7 mil people with disabilities are poor
- 70% of disabled are unemployed or underemployed

> The web offers unprecedented opportunities for disabled

- Education
- News
- Commerce
- Social
- Benefits of Web are amplified for disabled
- Web is enabling technology

> Legal aspects of making Web accessible

- DOJ is in the process of revising Title II and III of the ADA to include online resources of state and local entities
- Case law - individuals or entitiess can file civil rights complaints, e.g. Penn State, NYU, Northwestern, FSU, Target, Southwest Airlines, Priceline.com, Ramada, Kindle etc.

> What is Web accessibility

- making web accessible for the widest possible audience
- this audience includes Temporarily Able-Bodied users (TABs)
- currently, online infrastructure is hostile to those with disabilities
- inseparable from SEO, mobile, and usability: improve one and you improve others
- `best way to accomplish accessibility is to adhere to standards`

> W3C WCAG 2.0

- W3C Web Content Accessibility Guidelines are principle-, not technology-based
- the 4 principles (POUR):
    - Perceivable
    - Operable
    - Understandable
    - Robust

> Review

- designing with accessibility in mind is the right thing to do for many reasons
- adhering to standards (not flashy, cool effects) is key
- pay special attention to semantcis of tags

#### 2. Validating your code

validator.w3.org

> Three approaches

- validate by URL
- validate by filename
- validate by direct input

###### Tool for testing accessibility features
wave.webaim.org
###### Tool for testing disability features
funkify.org

#### 3. Putting your code on the web

##### Hosting your site

- hosting services
- need registered ip address to connect with your web

> free services

- little to no control of domain name
- limited tools
- advertising and redirects

> paid services

- better tools
- tech support

> host your own site

- more control
- more work

##### cPanel

- interface for managing hosted site
- public_html

##### Github pages

- allows to host a website on github
- when hosting a site in github need to create a repository with the same name as account name:
  - if account name is rebane then repository name should be "rebane.github.io"
- when uploading to github pages folder then under settings need to change source to master branch under Github pages.
