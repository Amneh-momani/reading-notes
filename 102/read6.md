## Function declarations :

A _function definition_ (also called a **function declaration**, or **function statement**) consists of the function keyword, followed by:

+ The name of the function.

+ A list of parameters to the function, enclosed in parentheses and separated by commas.

+ The JavaScript statements that define the function, enclosed in curly brackets, {...}.

If you pass an object (a non-primitive value, such as **Array** or a user-defined object) as a parameter and the function changes the object's properties, that change is visible outside the function.

# Function expressions :

_functions can also be created by a function expression._

Such a function can be anonymous; it does not have to have a name. For example:

**const square = function(number) { return number * number }
var x = square(4)**

# Calling functions :

Defining a function does not execute it. Defining it names the function and specifies what to do when the function is called.

Calling the function actually performs the specified actions with the indicated parameters.

**note :** Functions must be in scope when they are called, but the function declaration can be hoisted .

**note :** A function can call itself.

# Function scope :

Variables defined inside a function cannot be accessed from anywhere outside the function, because the variable is defined only in the scope of the function. However, a function can access all variables and functions defined inside the scope in which it is defined.

In other words, a function defined in the **global** scope can access all variables defined in the global scope. A function defined inside another function can also access all variables defined in its parent function, and any other variables to which the parent function has access.

**note : **A function can refer to and call itself. There are three ways for a function to refer to itself:

+ The function's name
+ arguments.callee
+ An in-scope variable that refers to the function

Within the function body, the following are all equivalent:

+ bar()
+ arguments.callee()
+ foo()

A function that calls itself is called a **recursive function** .

# Nested functions and closures :

You may **nest** a function within another function. The nested (inner) function is private to its containing (outer) function.

It also forms a closure. A **closure** is an expression (most commonly, a function) that can have free variables together with an environment that binds those variables.

# Name conflicts :

When two arguments or variables in the scopes of a closure have the same name, there is a name **conflict**.

 More nested scopes take precedence. So, the inner-most scope takes the highest precedence, while the outer-most scope takes the lowest. This is the scope chain. The first on the chain is the inner-most scope, and the last is the outer-most scope.

 # Function parameters :

* **Default parameters** : parameters of functions default to undefined.

* **Rest parameters** :The rest parameter syntax allows us to represent an indefinite number of arguments as an array.

# Arrow functions :

* **Shorter functions** : In some functional patterns, shorter functions are welcome.

* **No separate this** : Until arrow functions, every new function defined its own this value (_a new object in the case of a constructor, undefined in strict mode function calls, the base object if the function is called as an "object method"_).

# Function Invocation :

The code inside the function will execute when "something" invokes (calls) the function:

When an event occurs (when a user clicks a button)
When it is invoked (called) from JavaScript code
Automatically (self invoked)

## important notes:

* A JavaScript function is executed when "something" invokes it (calls it).

* The code to be executed, by the function, is placed inside curly brackets: {}

* Function parameters are listed inside the parentheses () in the function definition.

* Function arguments are the values received by the function when it is invoked.

* Inside the function, the arguments (the parameters) behave as local variables.

* **Function Return** :When JavaScript reaches a return statement, the function will stop executing.

* You can use the same code many times with different arguments, to produce different results.
