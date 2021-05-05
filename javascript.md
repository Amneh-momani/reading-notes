
## An assignment operator assigns:

x = y assigns the value of y to x.
which assigns the value of its right operand to its left operand.

## Return value and chaining

assignments like x = y have a return value.

* const z = (x = y); // Or equivalently: const z = x = y;

* console.log(z); // Log the return value of the assignment x = y.
* console.log(x = y); // Or log the return value directly.

The return value matches the expression to the right of the = sign.That means that (x = y) returns y, (x += y) returns the resulting sum x + y, (x **= y) returns the resulting (power x ** y), and so on.

In the case of logical assignments, (x &&= y), (x ||= y), and (x ??= y), the return value is that of the logical operation without the assignment, so x && y, x || y, and x ?? y.

When chaining these expressions, each assignment is evaluated right-to-left.
** w = z = x = y is equivalent to w = (z = (x = y)) or x = y; z = y; w = y **.

# Destructuring:
 extract data from arrays or objects using a syntax that mirrors the construction of array and object literals.

 // with destructuring
 var foo = ['one', 'two', 'three'];

// without destructuring
var one   = foo[0];
var two   = foo[1]; 

# Control flow:

Code is run in order from the first line in the file to the last line.such as conditionals and loops.

** if (field==empty) {
    promptUser();
} else {
    submitForm();
} **

Control flow means that when you read a script, you must not only read from start to finish but also look at program structure and how it affects order of execution. control structures can dictate complex flows of processing even with only a few lines of code.

## operator types:
* The addition operator (+) adds numbers

_The += assignment operator can also be used to add (concatenate) strings:_


*The multiplication operator (*) multiplies numbers.

* JavaScript Comparison Operators

*JavaScript Logical Operators





