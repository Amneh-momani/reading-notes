# Links

Links are the defining feature of the web because they allow you to move from one web page to another — enabling the very idea of browsing or surfing.

### You will commonly come across the following types of links:

Links from one website to another
+ Links from one page to another on the same website
+ Links from one part of a web page to another part of the 
+ same pageLinks that open in a new browser window
+ Links that start up your email program and address a new 
+ email to someone

## Writing Links

Links are created using the **< a >** element. Users can click on anything between the opening **< a >** tag and the closing **</ a >** tag. You specify which page you want to link to using the href attribute.

Example:

     < a href="http://www.imdb.com">IMDB</ a >


The text between the opening **< a >** tag and closing **</ a >** tag is known as link text. Where possible, your link text should explain where visitors will be taken if they click on it (rather than just saying "click here").

Many people navigate websites by scanning the text for links. Clear link text can help visitors find what they want.  This will give them a more positive impression of your site and may encourage them to visit it for longer. 

## Linking to other sites:

## < a >
**< a >** Links are created using the **< a >** element which has an attribute called href. The value of the href attribute is the page that you want people to go to when they click on the link.Users can click on anything that appears between the opening **< a >** tag and the closing **</ a >** tag and will be taken to the page specified in the href attribute.

When you link to a different website, the value of the hrefattribute will be the full web address for the site, which is known as an absolute URL.Browsers show links in blue with an underline by default.

       <p>Movie Reviews: 
        <ul> 
     <li><a href="http://www.empireonline.com">Empire</a></li>  

     <li><a href="http://www.metacritic.com">Metacritic</a></li>   

     <li><a href="http://www.rottentomatoes.com">Rotten Tomatoes</a></li>   

    <li><a href="http://www.variety.com">Variety</a></li> 
                 </ul>
        </p>

## AbsoLute urLs:

URL stands for **_Uniform Resource Locator_**. Every web page has its own URL. This is the web address that you would type into a browser if you wanted to visit that specific page.An absolute URL starts with the domain name for that site, and can be followed by the path to a specific page. If no page is specified, the site will display the homepage.

## Linking to other pages on the same site:

When you are linking to other pages within the same site, you do not need to specify the domain name in the URL. You can use a shorthand known as a relative URL.If all the pages of the site are in the same folder, then the value of the href attribute is just the name of the file.

If you have different pages of a site in different folders, then you can use a slightly more complex syntax to indicate where the page is in relation to the current page. You will learn more about these on the pages 81-84.

If you look at the download code for each chapter, you will see that the index.html file contains links that use relative URLs.


      <p>  
         <ul>      
            <li><a href="index.html">Home</a></li>      
            <li><a href="about-us.html">About</a></li>
            <li><a href="movies.html">Movies</a></li>     
            <li><a href="contact.html">Contact</a></li>  
         </ul>
      </p>

## reLative urLs

Relative URLs can be used when linking to pages within your own website. They provide a shorthand way of telling the browser where to find your files.


When linking to other pages within the same site, you can use relative URLs. These are like a shorthand version of absolute URLs because you do not need to specify the domain name.

Relative URLs help when building a site on your computer because you can create links between pages without having to set up your domain name or hosting.

## EmaiL Links

### mailto:
To create a link that starts up the user's email program and addresses an email to a specified email address, you use the **< a >** element. However, this time the value of the href attribute starts with mailto: and is followed by the email address you want the email to be sent to.

On the right you can see that an email link looks just like any other link but, when it is clicked on, the user's email program will open a new email message and address it to the person specified in the link.

    <a href="mailto:jon@example.org">Email Jon</a>


## opening Links in a new window :
## target

If you want a link to open in a new window, you can use the target attribute on the opening **< a >** tag. The value of this attribute should be _blank.One of the most common reasons a web page author might want a link to be opened in a new window is if it points to another website.

 In such cases, they hope the user will return to the window containing their site after finishing looking at the other one.

     <a href="http://www.imdb.com" target="_blank">

+ Links are created using the **< a >** element.
+ The **< a >** element uses the href attribute to indicate the page you are linking to.
+ If you are linking to a page within your own site, it is best to use relative links rather than qualified URLs.
+ You can create links to open email programs with an email address in the "to" field.
+ You can use the id attribute to target elements within a page that can be linked to.


# Layout

## Key Concepts in positioning eLements
**Building Blocks**

CSS treats each HTML element as if it is in its own box. This box will either be a block-levelbox or an inline box.

Block-level boxes start on a new line and act as the main building blocks of any layout, while inline boxes flow between surrounding text. You can control how much space each box takes up by setting the width of the boxes (and sometimes the height, too). To separate boxes, you can use borders, margins, padding, and background colors. 

## Block-level elements 
start on a new lineExamples include:

      <h1> <p> <ul> <li>

## inline elements 
flow in Between surrounding textExamples include:
    
     <img> <b> <i>

## containing Elements


If one block-level element sits inside another block-level element then the outer box is known as the containing or parent element.It is common to group a number of elements together inside a **< div >** (or other block-level) element. 

For example, you might group together all of the elements that form the header of a site (such as the logo and the main navigation). The **< div >** element that contains this group of elements is then referred to as the containing element.

### z-index
When you move any element from normal flow, boxes can overlap. The z-index property allows you to control which box appears on top.

### floating elements

Floating an element allows you to take that element out of normal flow and position it to the far left or right of a containing box. The floated element becomes a block-level element around which other content can flow.

### fixed Positioning

 This is a form of absolute positioning that positions the element in relation to the browser window, as opposed to the containing element. Elements with fixed positioning do not affect the position of surrounding elements and they do not move when the user scrolls up or down the page.

## Creating multi-coLumn Layouts with fLoats:

Many web pages use multiple columns in their design. This is achieved by using a <div>element to represent each column. The following three CSS properties are used to position the columns next to each other: 
## width

This sets the width of the columns.
### float
This positions the columns next to each other.
## margin
This creates a gap between the columns.

_A two-column layout like the one shown on this page would need two < div > elements, one for the main content of the page and one for the sidebar.Inside each of the < div >elements there can be headings, paragraphs, images, and even other < div > elements._

## screen resoLution

Resolution refers to the number of dots a screen shows per inch. Some devices have a higher resolution than desktop computers and most operating systems allow users to adjust the resolution of their screens.

## page sizes
Because screen sizes and display resolutions vary so much, web designers often try to create pages of around 960-1000 pixels wide (since most users will be able to see designs this wide on their screens).

## fixed width Layouts

Fixed width layout designs do not change size as the user increases or decreases the size of their browser window. Measurements tend to be given in pixels.

### advantages:
+ Pixel values are accurate ●at controlling size and positioning of elements. 
+ The designer has far greater ●control over the appearance and position of items on the page than with liquid layouts.

+ You can control the lengths ●of lines of text regardless of the size of the user's window. 
+ The size of an image will ●always remain the same relative to the rest of the page.


### disadvantages:
+ You can end up with big gaps around the edge of a page.
+ If the user's screen is a much higher resolution than the designer's screen, the page can look smaller and text can be harder to read.

+ If a user increases font sizes, text might not fit into the allotted spaces. 
+ The design works best on devices that have a site or resolution similar to that of desktop or laptop computers.
+ The page will often take up more vertical space than a liquid layout with the same content.

## Css frameworks

CSS frameworks aim to make your life easier by providing the code for common tasks, such as creating layout grids, styling forms, creating printer-friendly versions of pages and so on. You can include the CSS framework code in your projects rather than writing the CSS from scratch.

# Functions, Methods, and Objects:
Browsers require very detailed instructions about what we want them t o do. Therefore, complex scripts can run to hundreds (even thousands) of lines. Programmers use functions, methods, and objects to organize their code. 

### Functions
Functions let you group a series of statements together to perform a specific task. If different parts of a script repeat the same task, you can reuse the function (rather than repeating the same set of st atements). 

### GETTING MULTIPLE VALUES OUT OF A FUNCTION 

Functions can return more than one value using an array. For example, this function calculates the area and volume of a box. 

First, a new function is created call ed get Size(). The area of the box is calculated and stored in a variable called area. 

The volume is calculated and stored in a variable called vo 1 ume. Both are then placed into an array called shes. 

This array is then returned to the code that called the getSize() function, allowing the values to be used. 

     function getSize(width, height, depth) {
          var area = width * height; }
           var volume = width * height * depth;
            var sizes= [area,  volume]; 
           return sizes;
            var areaOne =  getSize(3, 2, 3)[0]; 
           var volumeOne = getSize(3, 2, 3)[1]; 

## VARIABLE SCOPE

The location where you declare a variable will affect where it can be used within your code. If you declare it within a function, it can only be used within that function. This is known as the variable's scope. 

## LOCAL VARIABLES
When a variable is created inside a function using the var keyword, it can only be used in that function. It is called a local variable or function-level variable. It is said to have local scope or function-level scope. It cannot be accessed outside of the fu nction in which it was declared. Below, area is a local variable. 

## GLOBAL VARIABLES 

If you create a variable outside of a function, then it can be used anywhere within the script. It is called a global variable and has global scope. In the example shown, wa 11 Size is a global variable. 

      function getArea(width, height)
       var area = width * height; 
       return area;
        var wallSize = getArea(3, 2);
        document. write(wa 11 Si ze); 


## Objects
Objects group together a set of variables and functions to create a model of a something you would recognize from the real world. In an object, variables and functions take on new names. 

If a function is part of an object, it is called a **method** . Methods represent tasks that are associated with the object. For example, you can check how many rooms are available by subtracting the number of booked rooms from t he total number of rooms. 

If a variable is part of an object, it is called a **property**. Properties te ll us about the object, such as the name of a hotel or the number of rooms it has. Each individual hotel might have a different name and a different number of rooms. 

## Programmers use a lot of name/value pairs: 
+ HTML uses attribute names and values.  
+ CSS uses property names and values.

## In JS:

+ Variables have a name and you can assign them a value of a string, number, or Boolean. 
+ Arrays have a name and a group of values. ( Each item in an array is a name/value pair because it has an index number and a value.) 
+ Named functions have a name and value that is a set of statements to run if the function is called.

# 6 Reasons for Pair Programming

##  1. Greater efficiency

It is a common misconception that pair programming takes a lot longer and is less efficient. In reality, when two people focus on the same code base, it is easier to catch mistakes in the making. Research indicates that pair programing takes slightly longer, but produces higher-quality code that doesn’t require later effort in troubleshooting and debugging (let alone exposing users to a broken product). So, in the long-run, it’s often actually more efficient than two people working on separate features.

## 2. Engaged collaboration

When two programmers focus on the same code, the experience is more engaging and both programmers are more focused than if they were working alone. It is harder to procrastinate or get off track when someone else is relying on you to complete the work. Popping open your Facebook timeline is just that less enticing when someone else is looking at your screen

## 3. Learning from fellow students

Everyone has a different approach to problem solving; working with a teammate can expose developers to techniques they otherwise would not have thought of. If one developer has a unique approach to a specific problem, pair programming exposes the other developer to a new solution.

## 4. Social skills

Pair programming is great for improving social skills. When working with someone who has a different coding style, communication is key. This can become more difficult when two programmers have different personalities. Pair programming not only improves programming skills, but can also help programmers develop their interpersonal skills. When just grabbing the keyboard and taking over isn’t an option, getting good at finding the right words is a skill unto itself.
## 5. Job interview readiness

A common step in many interview processes involves pair programming between a current employee and an applicant, either in person or through a shared screen. They will carry out exercises together, such as code challenges, building a project or feature, or debugging an existing code base. By doing so, companies can get a better feel for how an applicant will fit into the team and their collaboration style.
## 6. Work environment readiness

Many companies that utilize pair programing expect to train fresh hires from CS-degree programs on how they operate to actually deliver a product. Code Fellows graduates who are already familiar with how pairing works can hit the ground running at a new job, with one less hurdle to overcome.