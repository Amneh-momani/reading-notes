# code in a content management SyStem:

altering one template is a lot easier than changing the page for each individual product.In systems like this, when you have a large block of text that you can edit, such as a news article, blog entry or the description of a product in an e-commerce store, you will often see a text editor displayed. **Text** editors usually have controls a little like those on your word processor, giving you different options to style text, add links or insert images. 

Behind the scenes these editors are adding HTML code to your **text**, just like the code you have seen earlier in this chapter.Many of these editors will have an option that allows you to see (and edit) the code that they produce.Once you know how to read and edit this code, you can take more control over these sections of your website.In the example above, you can see that the **text** editor has a tab for Visual / HTML views of what the user enters. Other systems might have a button (which often shows angle brackets) to indicate how to access the code.

When the web was first taking off, one of the most common ways to learn about HTML and discover new tips and techniques was to look at the source code that made up web pages.

+ HTML pages are text documents.
+ XHTML uses tags (characters that sit inside angled Xbrackets) to give the information they surround special meaning.
+ Tags are often referred to as elements.
+ XTags usually come in pairs. 
+ The opening tag denotes Xthe start of a piece of content; the closing tag denotes the end.Opening tags can carry attributes, which tell us more Xabout the content of that element.
+ Attributes require a name and a value.
+ XTo learn HTML you need to know what tags are Xavailable for you to use, what they do, and where they can go.

# TEXT

When creating a web page, you add tags **(known as markup)** to the contents of the page. These tags provide extra meaning and allow browsers to show users the appropriate structure for the page.

## htmlHtMlHeadings
+ h1 largest one
+ h2
+ h3
+ h4
+ h5
+ h6 last one

## Paragraphs

+ To create a paragraph, surround the words that make up the paragraph with an opening **<p>** tag and closing **</p>** tag.

+ By enclosing words in the tags **<b>** and **</b>** we can make characters appear bold.

+ By enclosing words in the tags **<i>** and **</i>** we can make characters appear italic.
+ The **<sup>** element is used to contain characters that should be superscript such as the suffixes of dates or mathematical concepts like raising a number to a power such as 22.
+ The **<sub>** element is used to contain characters that should be subscript. It is commonly used with foot notes or chemical formulas such as H20.
+ When the browser comes across two or more spaces next to each other, it only displays one space. Similarly if it comes across a line break, it treats that as a single space too. This is known as **white space collapsing**.
+ As you have already seen, the browser will automatically show each new paragraph or heading on a new line. But if you wanted to add a line break inside the middle of a paragraph you can use the line break tag **<br />**.
+ To create a break between themes — such as a change of topic in a book or a new scene in a play ,you can add a horizontal rule between sections using the  <hr />  tag.

## <audio>

HTML5 introduced the **<audio>** element to include audio files in your pages. As with HTML5 video, browsers expect different formats for the audio.
The <audio> element has a number of attributes which allow you to control audio playback:
+ src
this attribute specifies the path to the audio file.
+ controls
This attribute indicates whether the player should display controls. If you do not use this attribute, no controls will be shown by default. You can also specify your own controls using JavaScript.
+ autoplay
The presence of this attribute indicates that the audio should start playing automatically. (It is considered better practice to let visitors choose to play audio.)
+ preload
This attribute indicates what the browser should do if the player is not set to autoplay. It can have the same values we saw on page 214 for the **video** element.

+ loop
This attribute specifies that the audio track should play again once it has finished.

## CSS 

CSS allows you to create rules that specify how the content of an element should appear. For example, you can specify that the background of the page is cream, all paragraphs should appear in gray using the Arial typeface, or that all level one headings should be in a blue, italic, Times typeface.

### BLock & Inline eLement 


_Block level elements look like they start on a new line.  Examples include the <h1>-<h6>, <p> and <div> elements.   Inline elements flow within the text and do not start on a new line. Examples include <b>, <i>, <img>, <em> and <span>.CSS works by associating rules with HTML elements. These rules govern how the content of specified elements should be displayed. A CSS rule contains two parts: a **selector** and a **declaration**._

**Selectors** indicate which element the rule applies to. The same rule can apply to more than one element if you separate the element names with commas.

**Declarations** indicate how the elements referred to in the selector should be styled. Declarations are split into two parts (a property and a value), and are separated by a colon.


CSS declarations sit inside curly brackets and each is made up of two parts: a **property** and a **value**, separated by a colon. You can specify several properties in one declaration, each separated by a semi-colon.

_**Properties** indicate the aspects of the element you want to change. For example, color, font, width, height and border._

_**Values** specify the settings you want to use for the chosen properties. For example, if you want to specify a color property then the value is the color you want the text in these elements to be._

## <link>

The **<link>** element can be used in an HTML document to tell the browser where to find the CSS file used to style the page. It is an empty element (meaning it does not need a closing tag), and it lives inside the **<head>** element. It should use three attributes:hrefThis specifies the path to the CSS file (which is often placed in a folder called css or styles).typeThis attribute specifies the type of document being linked to. The value should be text/css.relThis specifies the relationship between the HTML page and the file it is linked to. The value should be stylesheet when linking to a CSS file.An HTML page can use more than one CSS style sheet. To do this it could have a **<link>** element for every CSS file it uses. For example, some authors use one CSS file to control the presentation (such as fonts and colors) and a second to control the layout.

## <style>
You can also include CSS rules within an HTML page by placing them inside a **<style>** element, which usually sits inside the **<head>** element of the page. The **<style>** element should use the type attribute to indicate that the styles are specified in CSS. The value should be text/css.When building a site with more than one page, you should use an external CSS style sheet. This:Allows all pages to use the ●same style rules (rather than repeating them in each page).Keeps the content separate ●from how the page looks.Means you can change the ●styles used across all pages by altering just one file (rather than each individual page).

# <SCRIPT>
When the browser comes across a <script> element, it stops to load the script and then checks to see if it needs to do anything. 

### STATEMENTS 
A script is a series of instructions that a computer can follow one-by-one. Each individual instruction or step is known as a **statement**. Statements should end with a semicolon. 

_STATEMENTS ARE INSTRUCTIONS AND EACH ONE STARTS O N A NEW LINE A  statement is an individual instruction that the computer should follow. Each one should start on a new line and end with a semicolon. This makes your code easier to read and follow. The semicolon also tells the JavaScript interpreter when a step is over, indicating that it should move to the next step._

**note:** You should write comments to explain what your code does. They help make your code easier to read and understand. This can help you and others who read your code.

+ MULTI-LINE COMMENTS 
To write a comment that stretches over more than one line, you use a multi-line comment, starting with the/* characters and ending with the* /  characters. Anything between these characters is not processed· by the JavaScript interpreter. 

+ SINGLE-LINE COMMENTS 
In a single-line comment, anything that follows the two forward slash characters I/ on that line will not be processed by the JavaScript interpreter. Single-line comments are often used for short descriptions of what the code is doing. 

A script w ill have to temporarily st ore the bits of info rmation it needs to do its job. It can storet his data in **variables**. 

## DATA TYPES

+ JavaScript distinguishes between numbers, strings, and **true** or **false** values known as Booleans. 

+ NUMERIC DATA TYPE The numeric data type handles numbers. **0.75** 

+ STRING DATA TYPE The strings data t ype consists of letters and other characters. **'H. 1 ' Ivy! 1 '** 
+ BOOLEAN DATA TYPE Boolean data types can have one of two values: true or false. **true**

## Decisions and Loops

There are many several places ina script where decision are made that determine which lines of code should br run next. flowcharts can help you plan for these occasions.

### there are two components to a decision:
+ 1- An expression is evaluated, which returns a value
+ 2- A conditional statement says what to do in a given situation

