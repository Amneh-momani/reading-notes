# Forms

Traditionally, the term 'form' has referred to a printed document that contains spaces for you to fill in information.

_The best known form on the web is probably the search box that sits right in the middle of Google's homepage._

## Form Controls

There are several types of form controls that you can use to collect information from visitors to your site.

### 1) adding text
### 2) making choice  
### 3) submitting forms
### 4) uploading files


## how Forms Work
A user fills in a form and then presses a button to submit the information to the server.

The name of each form control is sent to the server along with the value the user enters or selects.

The server processes the information using a programming language such as PHP, C#, VB.net, or Java. It may also store the information in a database.

The server creates a new page to send back to the browser based on the information received.


A form may have several form controls, each gathering different information. The server needs to know which piece of inputted data corresponds with which form element.


## Form structure

+ < form > Form controls live inside a < form > element. This element should always carry the action attribute and will usually have a method and id attribute too.

+ action Every < form > element requires an action attribute. Its value is the URL for the page on the server that will receive the information in the form when it is submitted.

+ method Forms can be sent using one of two methods: get or post.

+ id
the value is used to identify the form distinctly from other elements on the page (and is often used by scripts — such as those that check you have entered information into fields that require values)

+ The < input > element is used to create several different form controls. The value of the type attribute determines what kind of input they will be creating.

+ The size attribute should not be used on new forms. It was used in older forms to indicate the width of the text input (measured by the number of characters that would be seen).

+ maxlength you can use the maxlengthattribute to limit the number of characters a user may enter into the text field. 

+ The name attribute indicates the name of the password input, which is sent to the server with the password the user enters.

+ The < textarea > element is used to create a mutli-line text input. Unlike other input elements this is not an empty element. It should therefore have an opening and a closing tag. 

+ The value attribute indicates the value that is sent to the server for the selected option. 

+ The checked attribute can be used to indicate which value (if any) should be selected when the page loads. The value of this attribute is checked. Only one radio button in a group should use this attribute.
+ he < option > element is used to specify the options that the user can select from. The words between the opening < option >and closing </ option > tags will be shown to the user in the drop down box.

+ The selected attribute can be used to indicate the option that should be selected when the page loads. The value of this attribute should be selected.
+ The for attribute states which form control the label belongs to.  Note how the radio buttons use the id attribute. The value of the id attribute uniquely identifies an element from all other elements on a page.

## < fieldset >
You can group related form controls together inside the < fieldset > element. This is particularly helpful for longer forms.

Most browsers will show the fieldset with a line around the edge to show how they are related. The appearance of these lines can be adjusted using CSS.

## Form validation
You have probably seen forms on the web that give users messages if the form control has not been filled in correctly; this is known as **form validation**.

## type="email"
If you ask a user for an email address, you can use the email input. Browsers that support HTML5 validation will check that the user has provided information in the correct format of an email address. Some smart phones also optimize their keyboard to display the keys you are most likely to need when entering an email address (such as the @ symbol).

## notes:
+ Whenever you want to collect information from visitors you will need a form, which lives inside a <form> element.
+ Information from a form is sent in name/value pairs.
+ Each form control is given a name, and the text the user types in or the values of the options they select are sent to the server.

## Lists, Tables & Forms

### list-style-type
The list-style-type property allows you to control the shape or style of a bullet point (also known as a **marker**). 

It can be used on rules that apply to the < ol >, < ul >, and < li >elements.

### list-style-image

You can specify an image to act as a bullet point using the list-style-image property.The value starts with the letters url and is followed by a pair of parentheses. Inside the parentheses, the path to the image is given inside double quotes.

### list-style-position
Lists are indented into the page by default and the list-style-position property indicates whether the marker should appear on the inside or the outside of the box containing the main points. 

This property can take one of two values:

+ outside
+ inside 

### list-style
As with several of the other CSS properties, there is a property that acts as a shorthand for list styles. It is called list-style, and it allows you to express the markers' style, image and position properties in any order.

## Table properties
**width** to set the width of the table

**padding** to set the space between the border of each table cell and its content

**text-transform** to convert the content of the table headers to uppercase

**letter-spacing, font-sizeto** add additional styling to the content of the table headers

**border-top, border-bottom** to set borders above and below the table headers

**text-align** to align the writing to the left of some table cells and to the right of the others

**background-color** to change the background color of the alternating table rows

**:hover** to highlight a table row when a user's mouse goes over it

## empty-cells

It can take one of three values:
+ show : This shows the borders of any empty cells.
+ hide  : This hides the borders of any empty cells.
+ inherit  : If you have one table nested inside another, the inherit value instructs the table cells to obey the rules of the containing table.

## styling text inputs

**font-size** sets the size of the text entered by the user.

**color** sets the text color, and **background-color** sets the background color of the input.

**border** adds a border around the edge of the input box, and **border-radius** can be used to create rounded corners (for browsers that support this property).

The **:focus** pseudo-class is used to change the background color of the text input when it is being used, and the **:hover** psuedo-class applies the same styles when the user hovers over them.

**background-image** adds a background image to the box. Because there is a different image for each input, we are using an attribute selector looking for the value of the id attribute on each input.

# Events

When you browse the web, your browser registers different types of events. It's the browser's way of saying, " Hey, this just happened." Your script can then respond to these events.

Events are said to **trigger** a function or script. When t he click event fires on the element in this diagram, it could trigger a script that enlarges the selected item

When the user interacts with the HTML on a web page, there are three steps involved in getting it to trigger some JavaScript code. Together these steps are known as **event handling.**

1)Select t he element node(s) you want the script to respond to. 


2)Indicate which event on the selected node(s) will trigger the response. 

3)State the code you want to run when the event occurs.

_Event handlers let you indicate which event you are waiting for on any particular element. There are three types of event handlers._

DOM **event handlers** were introduced in the original specification for the DOM. They are considered better than HTML event handlers because they let you separate the JavaScript from the HTML. 

**Event listeners** were introduced in an update to the DOM specification (DOM level 2, released in the year 2000). They are now the favored way of handling events. 

_All modern browsers understand this way of creating an event handler, but you can only attach one function to each event handler._

## THE EVENT OBJECT

When an event occurs, the event object tells you information about the event, and the element it happened upon. 

## EVENT DELEGATION

Creating event listeners for a lot of elements can slow down a page, but event flow allows you to listen for an event on a parent element. 