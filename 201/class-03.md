# LISTS

### HTML provides us with three different types:
+ **Ordered lists**

 are lists where each item in the list is numbered. For example, the list might be a set of steps for a recipe that must be performed in order, or a legal contract where each point needs to be identified by a section number.
 + **Unordered lists**

are lists that begin with a bullet point (rather than characters that indicate order).

+ **Definition  lists**

are made up of a set of terms along with the definitions for each of those terms.

## Ordered Lists

### < ol >

The ordered list is created with the **< ol >** element.


### < li >

Each item in the list is placed between an opening **< li >** tag and a closing **</ li >** tag. (The listands for list item.)

Example:

    < ol > 

        < li >Chop potatoes into quarters</ li >

        < li >Simmer in salted water for 15-20 
        minutes until tender</ li >

        < li >Heat milk, butter and nutmeg</ li >
        < li >Drain potatoes and mash</ li >
        < li >Mix in the milk mixture</ li >
    </ ol >


## Un Ordered Lists

### < ul >
The unordered list is created with the **< ul >** element.
### < li >
Each item in the list is placed between an opening **< li >** tag and a closing **</ li >** tag. (The listands for list item.)_Browsers indent lists by default._

## definition Lists

### < dl >
The definition list is created with the < dl > element and usually consists of a series of terms and their definitions.
Inside the < dl > element you will usually see pairs of < dt > and < dd > elements.


### < dt > 
This is used to contain the term being defined (the definition term).

### < dd >
This is used to contain the definition.

## nested Lists

You can put a second list inside an **< li >** element to create a sub-list or nested list.

### notes:

 _There are three types of HTML lists:_
+ ordered, unordered, and definition.
+ Ordered lists use numbers.
+ Unordered lists use bullets.Definition lists are used to define terminology.
+ Lists can be nested inside one another.

# Boxes
### Box Dimensions
**width, height**

By default a box is sized just big enough to hold its contents. To set your own dimensions for a box you can use the height and width properties.

The most popular ways to specify the size of a box are to use pixels, percentages, or ems. Traditionally, pixels have been the most popular method because they allow designers to accurately control their size.When you use percentages, the size of the box is relative to the size of the browser window or, if the box is encased within another box, it is a percentage of the size of the containing box.When you use ems, the size of the box is based on the size of text within it.

 Designers have recently started to use percentages and ems more for measurements as they try to create designs that are flexible across devices which have different-sized screens.

 Example:


    div.box 
    {  height: 300px; 
     width: 300px; 
     background-color: #bbbbaa;}

     p{
      height: 75%; 
       width: 75%; 
       background-color: #0088dd;}

###  limiting Width

**min-width, max-width**

Some page designs expand and shrink to fit the size of the user's screen. In such designs, the min-width property specifies the smallest size a box can be displayed at when the browser window is narrow, and the max-width property indicates the maximum width a box can stretch to when the browser window is wide.

These are very helpful properties to ensure that the content of pages are legible (especially on the smaller screens of handheld devices). For example, you can use the max-width property to ensure that lines of text do not appear too wide within a big browser window and you can use the min-width property to make sure that they do not appear too narrow.

### limiting height
**min-height, max-height**

In the same way that you might want to limit the width of a box on a page, you may also want to limit the height of it. This is achieved using the min-height and max-height properties.

If the box is not big enough to hold the content, and the content expands outside the box it can look very messy. 

### overflowing content

+ overflow

The overflow property tells the browser what to do if the content contained within a box is larger than the box itself.
 It can have one of two values.
 + hidden
 
 This property simply hides any extra content that does not fit in the box.
 + scroll


 This property adds a scrollbar to the box so that users can scroll to see the missing content.

## border, margin & padding

### Border
Every box has a border (even if it is not visible or is specified to be 0 pixels wide). The border separates the edge of one box from another.

### Margin
Margins sit outside the edge of the border. You can set the width of a margin to create a gap between the borders of two adjacent boxes.

### Padding
Padding is the space between the border of a box and any content contained within it. Adding padding can increase the readability of its contents.

## change inline/Block

**display**

The display property allows you to turn an inline element into a block-level element or vice versa, and can also be used to hide an element from the page.The values this property can take are:

**inline**

This causes a block-level element to act like an inline element.

**block**

This causes an inline element to act like a block-level element.

**inline-block**

This causes a block-level element to flow like an inline element, while retaining other features of a block-level element.

**none**

This hides an element from the page. In this case, the element acts as though it is not on the page at all (although a user could still see the content of the box if they used the view source option in their browser).

## Box shadow

The box-shadow property allows you to add a drop shadow around a box. It works just like the text-shadow property that you met on page 288. It must use at least the first of these two values as well as a color:

+ horizontal offset
+ vertical offset
+ Blur Distance
+ spread of shadow

# Basic JavaScript Instructions

## USING QUOTES INSIDE A STRING

Because strings can live in single or double quotes, if you just want to use double quotes in the string, you could surround the entire string in single quotes.

 If you just want to use single quotes in the string, you could surround the string in double quotes.

 You can also use a technique called escaping the quotation characters. This is done by using a backwards slash (or "backslash") before any type of quote mark that appears within a string (as shown on the fourth line of this code sample). The backwards slash tells the interpreter that the following character is part of the string, rather than the end of it.

## USING A VARIABLE TO STORE A BOOLEAN

A Boolean variable can only have a value of true or fa 1 se, but this data type is very helpful. 

It is rare that you would want to write the words true or false into the page for the user to read, but this data type does have two very popular uses: 

**First**, Booleans are used when the value can only be true/ fa 1 se. You could also think of these values as on/off or 0/1: true is equivalent to on or 1, fa 1 se is equivalent to off or 0 .

**Second**, Booleans are used when your code can take more than one path. Remember, different code may run in different circumstances.

## SHORTHAND FOR CREATING VARIABLES

_Programmers sometimes use shorthand to create variables. Here are three variations of how to declare variables and assign them values:_

 1. Variables are declared and values assigned in the same statement.

2. Three variables are declared on the same line, then values assigned to each. 

3. Two variables are declared and assigned values on the same line. Then one is declared and assigned a value on the next line. 

## CHANGING THE VALUE OF A VARIABLE

Once you have assigned a value to a variable, you can then change what is stored in the variable later in the same script.

 Once the variable has been created, you do not need to use the var keyword to assign it a new value. You just use the variable name, the equals sign (also known as t he assignment operator), and the new value for that attribute. 

# Decisions and Loops

## LOGICAL OPERATOR

### AND
The logical AND is used to see if the user's score is greater than or equal to t he pass mark in both of the rounds of the test. The result is stored in a variable called passBoth. 

### NOT

The logical NOT will invert the result of the Boolean variable so it is false. It is then written into t he page. 

### OR

 The logical OR operator to find out if the user has passed at least one of the two rounds.

## IF STATEMENTS

The if statement evaluates a condition . If the condition evaluates to true , any statements in the subsequent code block are executed.

## Switch 

A switch statement starts with a variable called the switch valus. each case indicates a possible value for this variable and the code that should run if the variable matches that value.

## SHORT CIRCUIT VALUES

Logical operators are processed left to right. They short-circuit (stop) as soon as they have a result -  but they return the value that stopped the processing (not necessarily true or fa1se). 

## LOOPS
 
 loops check a condition . if it return true, a code block will run . then the condition will be checked again and if it still returns true, the code block will run again .