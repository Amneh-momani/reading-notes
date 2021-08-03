# Functional Programming Concepts

## the functional programming is :

 a programming paradigm — a style of building the structure and elements of computer programs — that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data .

 ## pure function:

 + It returns the same result if given the same arguments (it is also referred as deterministic)
 +  It does not cause any observable side effects

 ## Pure functions benefits:

_The code’s definitely easier to test. We don’t need to mock anything. So we can unit test pure functions with different contexts:_

+ Given a parameter **A** → expect the function to return value **B**
+ Given a parameter **C** → expect the function to return value **D**

## immutability:

_Unchanging over time or unable to be changed._

## Referential transparency:

is when if a function consistently yields the same result for the same input:

Example :
       
       const square = (n) => n * n;
        square(2); // 4


# Node JS Tutorial for Beginners #6 - Modules and require()

## module:
 
we split our code up into logical modules and we have diffeenet moduale for every bit of code and it has many functions  

**require** is a function which we can pass whatever we want to becomes the path to the module that we required  so that's way how can  we bring another module into the file the we are working in.


note : _we have to do to make a module available by using_ **module.exports**