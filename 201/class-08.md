
# Layout

For a long time, web page authors used < div > elements to group together related elements on the page (such as the elements that form a header, an article, footer or sidebar). Authors used class or id attributes to indicate the role of the < div > element in the structure of the page.


## new HTML5 Layout elements

HTML5 introduces a new set of elements that allow you to divide up the parts of a page. The names of these elements indicate the kind of content you will find in them. They are still subject to change, but that has not stopped many web page authors using them already.


## Key Concepts in positioning elements
**Building Blocks**

CSS treats each HTML element as if it is in its own box. This box will either be a block-levelbox or an inline box.

Block-level boxes start on a new line and act as the main building blocks of any layout, while inline boxes flow between surrounding text. You can control how much space each box takes up by setting the width of the boxes (and sometimes the height, too). To separate boxes, you can use borders, margins, padding, and background colors. 

## Block-level elements 
start on a new lineExamples include:

      <h1> <p> <ul> <li>

## inline elements 
flow in Between surrounding textExamples include:
    
     <img> <b> <i>

## Headers & Footers
### < header > < footer >

The < header > and < footer >elements can be used for :

_The main header or footer that appears at the top or bottom of every page on the site._

_A header or footer for an individual < article > or < section > within the page._
## containing Elements


If one block-level element sits inside another block-level element then the outer box is known as the containing or parent element . It is common to group a number of elements together inside a **< div >** (or other block-level) element. 

For example, you might group together all of the elements that form the header of a site (such as the logo and the main navigation). The **< div >** element that contains this group of elements is then referred to as the containing element.

### z-index
When you move any element from normal flow, boxes can overlap. The z-index property allows you to control which box appears on top.


### < article >
The < article > element acts as a container for any section of a page that could stand alone and potentially be syndicated.

This could be an individual article or blog entry, a comment or forum post, or any other independent piece of content.

If a page contains several articles (or even summaries of several articles), then each individual article would live inside its own < article > element.

The < article > elements can even be nested inside each other. For example, a blog post might live inside one < article >element and each comment on the article could live inside its own child < article > element.

### < aside >

he < aside > element has two purposes, depending on whether it is inside an < article >element or not.

When the < aside > element is used inside an < article >element, it should contain information that is related to the article but not essential to its overall meaning. For example, a pullquote or glossary might be considered as an aside to the article it relates to.


### < section >

The < section > element groups related content together, and typically each section would have its own heading.


### floating elements

Floating an element allows you to take that element out of normal flow and position it to the far left or right of a containing box. The floated element becomes a block-level element around which other content can flow.

### fixed Positioning

 This is a form of absolute positioning that positions the element in relation to the browser window, as opposed to the containing element. Elements with fixed positioning do not affect the position of surrounding elements and they do not move when the user scrolls up or down the page.

## navigation

### < nav >
The < nav > element is used to contain the major navigational blocks on the site such as the primary site navigation.Going back to our blog example, if you wanted to finish an article with links to related blog posts, these would not be counted as major navigational blocks and therefore should not sit inside a < nav > element.


At the time of writing, some of the developers that were already using HTML5 decided to use the < nav > element for the links that appear at the bottom of every page (links to things like privacy policy, terms and conditions and accessibility information). Whether this will be widely adopted is still yet to be seen.

## Creating multi-column Layouts with floats:

Many web pages use multiple columns in their design. This is achieved by using a < div >element to represent each column. The following three CSS properties are used to position the columns next to each other: 
## width

This sets the width of the columns.
### float
This positions the columns next to each other.
## margin
This creates a gap between the columns.

_A two-column layout like the one shown on this page would need two < div > elements, one for the main content of the page and one for the sidebar.Inside each of the < div >elements there can be headings, paragraphs, images, and even other < div > elements._

## screen resolution

Resolution refers to the number of dots a screen shows per inch. Some devices have a higher resolution than desktop computers and most operating systems allow users to adjust the resolution of their screens.

## page sizes
Because screen sizes and display resolutions vary so much, web designers often try to create pages of around 960-1000 pixels wide (since most users will be able to see designs this wide on their screens).

## fixed width Layouts

Fixed width layout designs do not change size as the user increases or decreases the size of their browser window. Measurements tend to be given in pixels.

### advantages:
+ Pixel values are accurate at controlling size and positioning of elements. 
+ The designer has far greater control over the appearance and position of items on the page than with liquid layouts.

+ You can control the lengths of lines of text regardless of the size of the user's window. 
+ The size of an image will always remain the same relative to the rest of the page.


### disadvantages:
+ You can end up with big gaps around the edge of a page.
+ If the user's screen is a much higher resolution than the designer's screen, the page can look smaller and text can be harder to read.

+ If a user increases font sizes, text might not fit into the allotted spaces. 
+ The design works best on devices that have a site or resolution similar to that of desktop or laptop computers.
+ The page will often take up more vertical space than a liquid layout with the same content.

## Css frameworks

CSS frameworks aim to make your life easier by providing the code for common tasks, such as creating layout grids, styling forms, creating printer-friendly versions of pages and so on. You can include the CSS framework code in your projects rather than writing the CSS from scratch.
