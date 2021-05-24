# Operators :

**_JavaScript has the following types of operators._**

JavaScript has both binary and unary operators, and one special ternary operator, the conditional operator.

* A binary operator requires two operands, one before the operator and one after the operator  **3+4 or x*y**.

* A unary operator requires a single operand, either before or after the operator  **x++ or ++x**.

## Assignment operators :

**_An assignment operator assigns a value to its left operand based on the value of its right operand._**

The simple assignment operator is equal **(=)**, which assigns the value of its right operand to its left operand. That is, **x = y** assigns the value of **y** to **x** , assignments like x = y have a return value.

**Note :** The return values are always based on the operands’ values before the operation.

## Destructuring :

**_It's extract data from arrays or objects using a syntax that mirrors the construction of array and object literals._**

## Comparison operators :

**_A comparison operator compares its operands and returns a logical value based on whether the comparison is true. _**

The operands can be numerical, string, logical, or object values.

* Equal (==)
* Not equal (!=)
* Strict equal (===)
* Strict not equal (!==)
* Greater than (>)
* Greater than or equal (>=)
* Less than (<)
* Less than or equal (<=)

**Note :** => is not an operator, but the notation for Arrow functions.

## Arithmetic operators :

**_An arithmetic operator takes numerical values and returns a single numerical value._**

 The standard arithmetic operators are :
 * addition (+)
 * subtraction (-)
 * multiplication (*)
 * division (/)

 ## Bitwise operators :

**_A bitwise operator treats their operands as a set of 32 bits (zeros and ones)._**

Bitwise operators perform their operations on such binary representations, but they return standard JavaScript numerical values.

## Logical operators :
**_
Logical operators are typically used with Boolean (logical) values; when they are, they return a Boolean value._**

 However, the && and || operators actually return the value of one of the specified operands, so if these operators are used with non-Boolean values, they may return a non-Boolean value. 

/////

# for statement :

**_A for loop repeats until a specified condition evaluates to false. The JavaScript for loop is similar to the Java and C for loop._**

for (initialExpression ; conditionExpression ; incrementExpression)
 {
statement
 } 

 * initialExpression ... This expression usually initializes one or more loop counter.
 * conditionExpression ... If the value of conditionExpression is true, the loop statements execute. If it is false, the for loop terminates.
 * statement ... To execute multiple statements, use a block statement ({ ... }) to group those statements.
 

# do...while statement :
The do...while statement repeats until a specified condition evaluates to false.

do
  statement
while (condition);

# while statement :

**_A while statement executes its statements as long as a specified condition evaluates to true._**

 A while statement looks like :

 while (condition){
 
  statement

 }

 If the condition becomes false, statement within the loop stops executing and control passes to the statement following the loop.

 To execute multiple statements, use a block statement ({ ... }) to group those statements.


Avoid infinite loops. Make sure the condition in a loop eventually becomes false—otherwise, the loop will never terminate.






