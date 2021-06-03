# Error Handling & Debugging

## ORDER OF EXECUTION
To find the source of an error, it helps to know how scripts are processed. The order in which statements are executed can be complex; some tasks cannot complete until another statement or function has been run.

## EXECUTION CONTEXTS

The JavaScript interpreter uses the concept of **execution contexts**. There is  one global execution context; plus, each function creates a new execution context. They correspond to variable scope.

Every statement in a script lives in one of three execution contexts: 

+ GLOBAL CONTEXT 
+ FUNCTION CONTEXT
+ EVAL CONTEXT (NOT SHOWN)

### VARIABLE SCOPE 
The first two execution contexts correspond with the notion of scope:

+ GLOBAL SCOPE
+ FUNCTION-LEVEL SCOPE 

## EXECUTION CONTEXT & HOISTING
Each time a script enters a new execution context, there are two phases of activity: 
+ 1: PREPARE
+ A)The new scope is created 
+ B) Variables, functions, and arguments are created 
+ C)The value of the this keyword is determined 


+ 2: EXECUTE
+ A)Now it can assign values to variables
+ B)Reference functions and run their code
+ C)Execute statements 

Understanding that these two phases happen helps with understanding a concept called **hoisting**. You may have seen that you can: 

Call functions before they have been declared ,Assign a value to a variable that has not yet been declared .

This is because any variables and functions within each execution context are created before they are executed. The preparation phase is often described as taking all of the variables and functions and hoisting them to the top of the execution context. Or you can think of them as having been prepared. Each execution context also creates its own **variables object** . This object contains details of all of the variables, functions, and parameters for that execution context.


_In the interpreter, each execution context has its own variables object. It holds the variables, functions, and parameters available within it. Each execution context can also access its parent's variables object._

_The console will show you when t here is an error in your JavaScript. It also displays the line where it became a problem for the interpreter._


If a JavaScript statement generates an error, then it throws an exception. At that point, the interpreter stops and looks for exception-handling code. 

**Note** : Error objects can help you find where your mistakes are and browsers have tools to help you read them. 

### EvalError
INCORRECT USE OF eval() FUNCTION The eval () function evaluates text through t he interpreter and runs it as code (it is not discussed in this book). It is rare that you would see this type of error, as browsers often throw other errors when they are supposed to throw an Eval  Error. 

### URIError
INCORRECT USE OF URI FUNCTIONS If these characters are not escaped in URls, they will cause an error: / ? & I :   ; CHARACTERS ARE NOT ESCAPED decodeURI('
http://bbc.com/news.phplla=l'); URlError: URI error 


HOW TO DEAL WITH ERRORS :
+ HANDLE ERRORS GRACEFULLY 
+ DEBUG THE SCRIPT TO FIX ERRORS 


_You can indicate that a breakpoint should be triggered only if a condition that you specify is met. The condition can use existing variables._

## DEBUGGER KEYWORD
You can create a breakpoint in your code using just the debugger keyword. When the developer tools are open, this will automatically create a breakpoint.

 You can also place the debugger keyword within a conditional statement so that it only triggers the breakpoint if the condition is met. This is demonstrated in the code below. 

## HANDLING EXCEPTIONS

If you know your code might fail, use try, catch, and finally. Each one is given its own code block. 

**TRY** First, you specify the code that you think might throw an exception within the try block. 

**CATCH** If the try code block throws an exception, catch steps in with an alternative set of code. 

**FINALLY** The contents of the finally code block will run either way - whether the try block succeeded or failed. 

If you know something might cause a problem for your script, you can generate your own errors before the interpreter creates them. To create your own error, you use the following line:

 **throw new Error('message');**

 This creates a new Error object (using the default Error object). The parameter is the message you want associated with the error. This message should be as descriptive as possible.

_Browsers that have a console have a console object, which has several methods that your script can use to display data in the console. The object is  documented in the Console API._ 

## Notes

+ If you understand execution contexts (which have two stages) and stacks, you are more likely to find the error in your code. 

+ Debugging is the process of finding errors. It involves a process of deduction. 
+ The console helps narrow down the area in  which the error is located, so you can try to find the exact error. 
+ JavaScript has 7 different types of errors. Each creates its own error object, which can tell you its line number and gives a description of the error. 
+ If you know that you may get an error, you can handle it gracefully using the try, catch, finally statements. Use them to give your users helpful feedback.

