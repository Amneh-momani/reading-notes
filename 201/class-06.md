# Understanding The Problem Domain Is The Hardest Part Of Programming

## The hardest thing about writing code:
+ Learning a new technology
+ Naming things
+ Testing your code
+ Debugging
+ Fixing bugs
+ Making software maintainable

# A familiar problem
In a good portion of my Pluralsight courses I show the viewer how to build the “Protein Tracker” application.

I am often asked why I keep demonstrating how to build the same simple application over and over again in each of my courses.

When I first started using the Protein Tracker example in my Android course, I was just looking for a simple example of an application that could be easily understood and implemented.

The idea behind the Protein Tracker application is that it allows a user to set a goal for the amount of protein to consume in a day.  The user can add protein amounts which are added to a total protein count that is tracked for that user.

Very simple functionality, easily explainable, but most importantly, easily understood.

**_By creating a familiar problem domain, I found that both the tasks of me teaching a new technology and the viewer learning that technology were much easier, because it is very difficult to learn more than one thing at once._**

## So what am I trying to say here?

Simply that by taking away the problem domain, or making it so trivial that it is easily understood, I am able to make both teaching and learning easier.

## Programming is easy if you understand the problem domain

A long time ago, I worked for Hewlett Packard writing software for multi-function printers.

Most of the work at the time was basic waterfall development.  There wasn’t much Agile happening there—at least at the time I was there.

I remember writing a tab control for the user interface of a printer and having the complete pixel perfect specs handed to me before I began to write any code.  I was also given all the possible use cases and told exactly how it should function and what it should do under just about every circumstance.

I was essentially given the entire problem domain in the form of a spec that was clear and unambiguous.  **_I was easily able to learn that problem domain and because of it, I was able to write the code very easily as well_**.

If understanding the problem domain is the hardest part of programming and you want to make programming easier, you can do one of two things:

+ 1-Make the problem domain easier
+ 2-Get better at understanding the problem domain

**You can often make the problem domain easier by cutting out cases and narrowing your focus to a particular part of the problem.**

## Quick update on my new product

many developers don’t realize how much of an impact marketing themselves and branding can have on their opportunities.  I’m hoping to help developers learn not only how valuable marketing and branding is, but how to do it most effectively.

# Object Literals

Literal nation is the easiest and most popular war to create objects.

you accsess the properites or methods of an object using dot notation .also by using square brackets.

To access a property or method of an object you use the name of the object , followed by a period , then the name of the property or method you want to access.This is known as **dot notation**.

The period is known as the **member operator**.

# Document Object Model
The Document Object Model (DOM) specifies how browsers should create a model of an HTML page and how JavaScript can access and update the contents of a web page while it is  in the browser window. 

The **DOM** is neither part of HTML, nor part of JavaScript; it is a separate set of rules. It is implemented by all major browser makers, and covers two primary areas: 

You will hear people call the DOM an **Application Programming Interface ( API)**.

The DOM is called an object model because the model (the DOM tree) is made of objects. 

## THE DOM TREE IS A MODEL OF A WEB PAGE 
As a browser loads a web page, it creates a model of t hat page. The model is called a DOM t ree, and it is stored in the browsers' memory. It consists of four main types of nodes. 

_Each node is an object with methods and properties. Scripts access and update this DOM tree (not the source HTML file). Any changes made to the DOM tree are reflected in  the browser._

## WORKING WITH THE DOM TREE
Accessing and updating the DOM tree involves two steps: 
+ 1: Locate the node that represents the element you want to work with.
+  2: Use its text content, child elements, and attributes. 

The terms **elements** and **element nodes** are used interchangeably but when people say the DOM is working with an element, it is actually working with a node that represents that element. 

## ACCESSING ELEMENTS

DOM queries may return one element, or they may return a Nodelist, which is a collection of nodes. 

### GROUPS OF ELEMENT NODES

If a method can return more than one node, it will always return a Nodelist , which is a collection of nodes (even if it only finds one matching element). You then need to select the element you want from this list using an index number (which means the numbering star ts at 0 like the items in an array). 

### FASTEST ROUTE
Finding the quickest way to access an element within your web page w ill make the page seem faster and/or more responsive. This usually means evaluating the minimum number of nodes on the way to the element you want to work with. 

**METHODS THAT RETURN A SIN GLE ELEMENT NODE:**

+ getElementByld('id')


      Selects an individual element given the value of its i d attribute . The HTML must  have an id attribute in order for it to be selectable. 

+ querySelector('css selector')

         Uses CSS selector syntax t hat would select one or more element s . This method returns only the first of t  he matching elements. 

**M ETHODS THAT RETURN ONE OR MORE ELEMENTS (AS A NODELIST):**

+ getElementsByClassName('c lass') 

         Selects one or more elements given t he value of their cl ass attribute. The HTML must have a cl ass attribute fo r it to be selectable. T his method is faster t han querySe 1ectorA11 (). 

+ getElementsByTagName('tagName') 

         Selects all elements on t he page with the specified tag name. This met hod is faster than querySe 1ectorA11 (). 

+ querySelectorAll ('css select or')

        Uses CSS selector syntax to select one or more element s and returns all of those t hat match.


## SELECTING ELEMENTS USING CLASS ATTRIBUTES 

The getElementsByClassName() method allows you to select elements whose class attribute contains a specific value. 

## LOOPING THROUGH A NODELIST

If you want to apply the same code to numerous elements, looping through a Nodelist is a powerful technique.
 
 It involves finding out how many items are in the Nodelist, and then setting a counter to loop through them, one-by-one. 


 ## ADDING ELEMENTS USING DOM MANIPULATION 

 DOM manipulation offers another t echnique to add new content to a page (rather than i nnerHTML). It involves three steps: 

+ 1)CREATE THE ELEMENT **createElement ()** 

+ 2)GIVE IT CONTENT **createTextNode()** 
+ 3)ADD IT TO THE DOM
**appendChild()**

## CHECK FOR AN ATTRIBUTE AND GET ITS VALUES

Before you work with an attribute, it is good practice to check whether it exists. This will save resources if the attribute cannot be found. 

The hasAttribute() method of any element node lets you check if an attribute exists. The attribute name is given as an argument in the parentheses. 