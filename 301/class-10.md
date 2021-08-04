# Understanding the JavaScript Call Stack

## The call stack is primarily used for function invocation (call). Since the call stack is single, function(s) execution, is done, one at a time, from top to bottom. It means the call stack is synchronous.

## (LIFO) 

_The Last In, First Out (LIFO) principle to temporarily store and manage function invocation (call)_

Example of call stack with the functions:

      function firstFunction(){
        console.log("Hello from firstFunction");
      }

      function secondFunction(){
        firstFunction();
        console.log("The end from secondFunction");
      }

      secondFunction();


## Stack Overflow

A stack overflow occurs when there is a recursive function (a function that calls itself) without an exit point. The browser (hosting environment) has a maximum stack call that it can accomodate before throwing a stack error.


Example :


        function callMyself(){
      callMyself();
      }

      callMyself();

# JavaScript error messages

## Reference errors

This is as simple as when you try to use a variable that is not yet declared you get this type os errors.


       console.log(foo) // Uncaught ReferenceError: foo is not defined


## Syntax errors

 This occurs when you have something that cannot be parsed in terms of syntax, like when you try to parse an invalid object using JSON.parse.

       JSON.parse( {'foo': 'bar'} ) // Uncaught SyntaxError: Unexpected token o in JSON at position 1


## Range errors

Try to manipulate an object with some kind of length and give it an invalid length and this kind of errors will show up.

      var foo= []
      foo.length = foo.length -1 // Uncaught RangeError: Invalid array length

## Type errors

Like the name indicates, this types of errors show up when the types (number, string and so on) you are trying to use or access are incompatible, like accessing a property in an undefined type of variable.


     var foo = {}
     foo.bar // undefined
     foo.bar.baz // Uncaught TypeError: Cannot read property 'baz' of undefined

## Breakpoint

We can use it by putting a debugger statement in your code in the line you want to break.

If we added a debugger statement and when running the code we can see the “history” before reaching that breakpoint.