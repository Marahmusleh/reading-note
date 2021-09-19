## Functions

*Functions are one of the fundamental building blocks in JavaScript. A function in JavaScript is similar to a procedure—a set of statements that performs a task or calculates a value, but for a procedure to qualify as a function, it should take some input and return an output where there is some obvious relationship between the input and the output. To use a function, you must define it somewhere in the scope from which you wish to call it.*

**Defining functions**
* Function declarations

A function definition (also called a function declaration, or function statement) consists of the function keyword, followed by:

+ The name of the function.
+ A list of parameters to the function, enclosed in parentheses and separated by commas.
+ The JavaScript statements that define the function, enclosed in curly brackets, {...}.
 
 
**Function expressions**

While the function declaration above is syntactically a statement, functions can also be created by a function expression.
Such a function can be anonymous; it does not have to have a name. For example, the function square could have been defined as:

>const square = function(number) { return number * number }
var x = square(4) // x gets the value 16

However, a name can be provided with a function expression. Providing a name allows the function to refer to itself, and also makes it easier to identify the function in a debugger's stack traces:

## Calling functions
Defining a function does not execute it. Defining it names the function and specifies what to do when the function is called.

Calling the function actually performs the specified actions with the indicated parameters.