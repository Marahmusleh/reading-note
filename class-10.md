### Error Handling & Debugging

When writing a long script, nobody gets everything right in their first attempt. The error
messages that a browser gives look cryptic at first, but they can help you determine what
went wrong in your JavaScript and how to fix it. In this chapter you will learn about:
+ THE CONSOLE & DEV TOOLS
Tools built into the browser
that help you hunt for errors.
9 ERROR HANDLING & DEBUGGING
+ COMMON PROBLEMS
Common sources of errors,
and how to solve them.
+ HANDLING ERRORS
How code can deal with
potential errors gracefully.

# UNDERSTANDING SCOPE

In the interpreter, each execution context has its own va ri ables object.
It holds the variables, functions, and parameters available within it.
Each execution context can also access its parent's v a ri ables object. 

![img](http://3.bp.blogspot.com/-8mU9S5o9tbw/T3Infj_gSEI/AAAAAAAAB1s/wxQ9Puke-44/s1600/js_scope.png)

The inner functions can access the outer functions and their
variables. For example, the greetUser() function
can access the time variable that was declared in the
outer greeting() function.
Each time a function is called, it gets its own
execution context and va r i ables object.
Each time an outer function calls an inner function,
the inner function can have a new variables object.
But variables in the outer function remain the same.

# ERROR OBJECTS CONTINUED

**Syntax Error**
*SYNTAX IS NOT CORRECT*
This is caused by incorrect use of the rules of the
language. It is often the result of a simple typo.
```
MISMATCHING OR UNCLOSED QUOTES
document .write ("Howdyl );
SyntaxError: Unexpect ed EOF
MISSING CLOSING BRACKET
document .getElementByid('page' I
SyntaxErr or : Expected token ' ) '

```

**ReferenceError**
*VARIABLE DOES NOT EXIST*
This is caused by a variable that is not declared or is
out of scope.

```
VARIABLE IS UNDECLARED
var wi dth = 12 ;
var area = width * llt!ftNU! ;
ReferenceError: Can ' t find vari able:
height
NAMED FUNCTION IS UNDEFINED
document.write ( randomFunction() ) ;
ReferenceError: Can't find variable :
randomFunction 

```

+ Debugging is the process of finding errors. It involves a
process of deduction.
+ The console helps narrow down the area in which the
error is located, so you can try to find the exact error.
+ JavaScript has 7 different types of errors. Each creates
its own error object, which can tell you its line number
and gives a description of the error.
+ If you know that you may get an error, you can handle
it gracefully using the try, catch, finally statements.
Use them to give your users helpful feedback. 
