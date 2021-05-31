# Domain Modeling

Domain modeling is the process of creating a conceptual model in code for a specific problem. A model describes the various entities, their attributes and behaviors, as well as the constraints that govern the problem domain. An entity that stores data in properties and encapsulates behaviors in methods is commonly referred to as an object-oriented model.


## Model epic fails videos

Imagine you've been tasked to build a program that models the popularity of epic fail videos. After months of painstaking research, you've determined that the two essential metrics for gauging popularity are an epic rating and whether or not the video has animals.

## Define a constructor and initialize properties

To define the same properties between many objects, you'll want to use a constructor function. Below is a table that summarizes a JavaScript representation of an **EpicFailVideo** object.

Here's an implementation of the **EpicFailVideo** constructor function.

      var EpicFailVideo = function(epicRating, hasAnimals) {
       this.epicRating = epicRating;
       this.hasAnimals = hasAnimals;
     }

     var parkourFail = new EpicFailVideo(7, false);
     var corgiFail = new EpicFailVideo(4, true);

     console.log(parkourFail);
     console.log(corgiFail);


**_This is object-oriented programming in JavaScript at its most fundamental level._**

+ The new keyword instantiates (i.e. creates) an object.
+ The constructor function initializes properties 
inside that object using the this variable.
+ The object is stored in a variable for later use.

##Calculate daily Likes


Popularity of a video is measured in Likes. And the formula for calculating Likes is the number of viewers times the percentage of viewers who'll Like a video. In other words, **viewers times percentage**.

To calculate the number of viewers per day, generate a random number between 10 and 30 and then multiply it by the epic rating of that video.

**notes :**

+ When modeling a single entity that'll have many instances, build self-contained objects with the same attributes and behaviors.
 
+ Model its attributes with a constructor function that defines and initializes properties.
 
+ Model its behaviors with small methods that focus on doing one job well.
 
+ Create instances using the **new** keyword followed by a call to a constructor function.
 
+  Store the newly created object in a variable so you can access its properties and methods from **outside**.
+ Use the **this** variable within methods so you can access the object's properties and methods from **inside**.

# Table
A table represents information in a grid format. Examples of tables include financial reports, TV schedules, and sports results.

Grids allow us to understand complex data by referencing information on two axes.

Each block in the grid is referred to as a **table cell**. In HTML a table is written out row by row.


## Table structure

## < table >

The < table > element is used to create a table. The contents of the table are written out row by row.

## < tr >
You indicate the start of each row using the opening < tr > tag. (The tr stands for table row.)
 It is followed by one or more < td > elements (one for each cell in that row). 

 At the end of the row you use a  closing </ tr > tag.
 
 ## < td >
 Each cell of a table is represented using a < td >element. (The td stands for table data.)
 At the end of each cell you use a closing </ td > tag.

## headings

## < th >
The < th > element is used just like the  < td > element but its purpose is to represent the heading for either a column or a row. (The th stands for table heading.) Even if a cell has no content, you should still use a < td > or < th > element to represent the presence of an empty cell otherwise the table will not render correctly.


_The colspan attribute can be used on a < th > or < td > element and indicates how many columns that cell should run across._

The rowspan attribute can be used on a < th > or < td > element to indicate how many rows a cell should span down the table.

## < thead >
The headings of the table should sit inside the < 

thead > element.

 ## < tbody >
 The body should sit inside the < tbody > element.
 


 ##  < tfoot >
 The footer belongs inside the < tfoot > element.

 ## border 
 The border attribute was used on both the < table > and < td >elements to indicate the width of the border in pixels.

 _The bgcolor attribute was used to indicate background colors of either the entire table or individual table cells._

## Notes:

+ The < table > element is used to add tables to a web page.
+ A table is drawn out row by row. Each row is created with the < tr > element.
+ Inside each row there are a number of cells represented by the < td > element (or < th > if it is a header).
+ You can make cells of a table span more than one row or column using the rowspan and colspan attributes.
+ For long tables you can split the table into a < thead >, < tbody >, and < tfoot >.


# Functions, Methods, and Objects
Objects group together a set of variables and functions to create a model of a something you would recognize from the real world. In an object, variables and functions take on new names. 

## IN AN OBJECT: VARIABLES BECOME KNOWN AS PROPERTIES
If a variable is part of an object, it is called a **property**. Properties te ll us about the object, such as the name of a hotel or the number of rooms it has. Each individual hotel might have a different name and a different number of rooms.

## IN AN OBJECT: FUNCTIONS BECOME KNOWN AS METHODS
If a function is part of an object, it is called a **method**. Methods represent tasks that are associated with the object. For example, you can check how many rooms are available by subtracting the number of booked rooms from t he total number of rooms. 

## CREATING OBJECTS USING CONSTRUCTOR SYNTAX

       var hotel =new Object(); hotel.name= 'Park';
        hotel.rooms= 120; hotel .booked = 77;
         hotel .checkAvailability = function() return this.rooms -  this.booked; } ;
         JAVASCRIPT var elName = document.getElementByid('hotelName');
         elName.textContent = hotel.name;
         var elRooms = document. getElementByid('rooms');
         elRooms. textContent = hotel. checkAvailability(}; 

On t he right, an empty object called hote 1 is created using the constructor function. Once it has been created, three properties and a method are then assigned to the object.

 ( If the object already had any of these properties, this would overwrite the values in t hose properties.) To access a property of this object, you can use dot notation, just as you can with any object.
 
  For example, to get the hotel's name you could use: hotel .name Similarly, to use the method, you can use the object name followed by the method name: hotel.checkAvailability() 


  ## WAYS TO CREATE OBJECTS

  CREATE THE OBJECT, THEN ADD PROPERTIES & METHODS

  + LITERAL NOTATION :
              
         var hotel  = {} hotel .name= 'Quay';
         hotel .rooms = 40; hotel.booked= 25;
          hotel.checkAvailability =function() return this.rooms-this.booked; } ; 
+ OBJECT CONSTRUCTOR NOTATION  :

      var hotel =new Object(); hotel.name=  ' Quay'; hotel .rooms = 40; hotel. booked= 25; hotel.checkAvailability =function() return this.rooms -this.booked; } ; 

## THIS 
The keyword **this** is commonly used inside functions and objects. Where the function is declared alters what this means. It always refers to one object, usually the object in which the function operates. 


## RECAP: STORING DATA
In JavaScript, data is  represented using name/value pairs. To organize your data, you can use an array or object to group a set of related values. In arrays and objects the name is also known as a key. 

### VARIABLES 
A variable has just one key (the variable name) and one value. 

Variable names are separated from their value by an equals sign (the assignment operator): 
        
          var hotel= 'Quay'; 

### ARRAYS 

Arrays can store multiple pieces of information. Each piece of information is separated by a comma. The order of the values is important because items in an array are assigned a number (called an index). 

Values in an array are put in square brackets, separated by commas: 
          
    var hotels = [ ' Quay' , 'Park', ' Beach', 'Bloomsbury' ] 


## STRING OBJECT

Whenever you have a value that is a string, you can use the properties and methods of the String object on that value. Example :
    
         var saying ='Home sweet home';


These properties and methods are often used to work with text stored in variables or objects. 

Each character in a string is automatically given a number, called an **index number**. Index numbers always start at zero and not one (just like for items in an array). 

## NUMBER OBJECT

Whenever you have a value that is a number, you can use the methods and properties of the Number object on it. 

## COMMONLY USED TERMS: 
+  A n integer is a w hole number (not a fraction).
 +  A real number is a number that can contain a fractional part. 
 +  A floating point number is a real number that uses decimals to represent a fraction. The term floating point refers to the decimal point. 
 +  Scientific notation is a way of writing numbers that are too big or too small to be conveniently written in decimal form.


 ## DECIMAL NUMBERS
 As with the String object the properties and methods of the Number  object can be used with with any value that is a number. 

 _originalNumber.toFixed(3) will round the number stored in the variable original Number t o three decimal places._

 **JavaScript also has several built-in objects such as String, Number, Math, and Date. Their properties and methods offer functionality that help you write scripts.**  
 