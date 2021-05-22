# HTML-CSS:
## how PeopLe access the web:
+ Browsers

People access websites using software called a web browser. Popular examples include Firefox, Internet Explorer, Safari, Chrome, and Opera.
+ web servers

When you ask your browser for a web page, the request is sent across the Internet to a special computer known as a web server which hosts the website.
+ screen readers

Screen readers are programs that read out the contents of a computer screen to a user. They are commonly used by people with visual impairments.

**All websites use HTML and CSS, but content management systems, blogging software, and e-commerce platforms often add a few more technologies into the mix.**

## how the web works
When you visit a website, the web server hosting that site could be anywhere in the world. In order for you to find the location of the web server, your browser will first connect to a Domain Name System (DNS) server.

## Structuring word documents
The use of headings and subheadings in any document often reflects a hierarchy of information. For example, a document might start with a large heading, followed by an introduction or the most important information.

## Html uses elements to describe the structure of pages
Tags act like containers. They tell you something about the information that lies between their opening and closing tags.

### Attributes tell us more about eLements
Attributes provide additional information about the contents of an element. They appear on the opening tag of the element and are made up of two parts: a **name** and a **value**, separated by an equals sign.

**note:** HTML5 allows you to use uppercase attribute names and omit the quotemarks, but this is not recommended.

### Forms
 Whenever you want to collect information from Xvisitors you will need a form, which lives inside a <form> element.Information from a form is sent in name/value pairs.XEach form control is given a name, and the text the Xuser types in or the values of the options they select are sent to the server.HTML5 introduces new form elements which make it Xeasier for visitors to fill in forms.
 
### Images
You can specify the dimensions of images using CSS. XThis is very helpful when you use the same sized images on several pages of your site.Images can be aligned both horizontally and vertically Xusing CSS.You can use a background image behind the box Xcreated by any element on a page. Background images can appear just once or be Xrepeated across the background of the box.You can create image rollover effects by moving the Xbackground position of an image.To reduce the number of images your browser has to Xload, you can create image sprites.

### TraditionaL HTML Layouts
For a long time, web page authors used <div> elements to group together related elements on the page (such as the elements that form a header, an article, footer or sidebar). Authors used class or id attributes to indicate the role of the <div> element in the structure of the page.

### new HTML5 Layout element
HTML5 introduces a new set of elements that allow you to divide up the parts of a page. The names of these elements indicate the kind of content you will find in them. They are still subject to change, but that has not stopped many web page authors using them already.

# JAVASCRIPT IN THE BROWSER:
 Being able to change the content of an HTML page w hile it is loaded in the browser is very powerful. The examples below rely on the ability to:
 + **Access** the content of the page
 + **Modify** t he content of the page
 + **Program** rules or instructions the browser can follow
 + **React** to events triggered by the user or browser 

 ## HTML elements:
 HTML elements are added to the content of a page to describe its structure. An element consists of the opening and closing tags,plus content.

 + <p class="add">content</p>

 ## CSS rules:
 CSS uses rules to indicate how the contents of one or more elements should be displayed in the browser.Each rule has a selector and a declaration block.

 + .add{color:red;}

 ## A SCRIPT IS A SERIES OF INSTRUCTIONS :
 A script is a series of instructions that a computer can follow to achieve a goal. 

 You could compare scripts to any of the following:
 + RECIPES 
 By following the instructions in a recipe, one-by-one in t he order set out, cooks can create a dish they have never made before.

 + HANDBOOKS
  Large companies often provide handbooks for new employees that contain procedures to follow in certain situations. 

  + MANUALS 
  Mechanics often refer to car repair manuals when servicing models they are not familiar with. These manuals contain a series of tests to check the key functions of the car are working, along with details of how to fix any issues that arise. 

### notes:
+ _**Scripts are made up of instructions a computer can follow step-by-step.**_

+ _**A browser may use different parts of the script depending on how the user interacts with the web page.**_

+ _**Scripts can run different sections of the code in response to the situation around them.**_

## Designing A Script tasks:

Once you know the goal of your script, you can work out the individual tasks needed to achieve it.This high-level view of the tasks can be represented using a flowchart.

## Designing A Script steps:

Each individual task may be broken down into a sequence of steps.When you are ready to code the script ,these steps can then be translated into individual lines of code.....

+ step1: remove used bedding
+ step2: wipe all surfaces
+ step3: vacuum floors
+ step4: fit new bedding
+ step5: remove used towels and soaps
+ step6: clean toilet, bath , skin ,surfaces
+ step7: place new towels and soaps
+ step8: wipe bathroom floor

## FROM STEPS TO CODE:
Every step for every task shown in a flowchart needs to be written in a language the computer can understand and follow.

 _You need to get to grips wit h the_: 
 + **Vocabulary**: The words that computers understand 
 + **Syntax**: How you put those words together to create instructions computers can follow

 ## OBJECTS & PROPERTIES:


 ### OBJECTS (THINGS)
  In computer programming, each physical thing in the world can be represented as an object.

  Each object can have its own:
   + Properties 
   + Events 
   + Methods 

 ### PROPERTIES (CHARACT ERISTICS)
  
  Both of the cars share common characteristics. In fact, all cars have a make, a color, and engine size. You could even determine their current speed. Programmers call these characteristics the properties of an object.

## How A browser sees a web page:
In order to understand how you can change the content of an HTML page using JavaScript, you need to know how a browser interprets the HTML code and applies styling to it.
+ 1)receive a page as HTML code.
+ 2)create a model of the page and store it in memory.
+ 3)use a rendering engine to show the page screen.