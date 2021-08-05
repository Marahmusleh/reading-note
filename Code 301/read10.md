## Read: Class 10 - In memory storage
## The JavaScript Call Stack:
1. What is a ‘call’?
* The call stack is primarily used for function invocation (call)

2. How many ‘calls’ can happen at once?
* It is single-threaded. Meaning it can only do one thing at a time. (happen once at time)

3. What does LIFO mean?
* Stands for Last in First out, it means that the last function that gets pushed into the stack is the first to be pop out, when the function returns.

4. Draw an example of a call stack and the functions that would need to be invoked to generate that call stack
```
  throw new Error('Stack Trace Error');
}

function secondFunction(){
  firstFunction();
}

function thirdFunction(){
  secondFunction();
}

thirdFunction();
```
5. What causes a Stack Overflow?
* A stack overflow occurs when there is a recursive function (a function that calls itself) without an exit point. The browser (hosting environment) has a maximum stack call that it can accommodate before throwing a stack error.

## JavaScript error messages:
1. What is a ‘reference error’?
* This is as simple as when you try to use a variable that is not yet declared you get this type os errors.

2. What is a ‘syntax error’?
* this occurs when you have something that cannot be parsed in terms of syntax.

3. What is a ‘range error’?
* Try to manipulate an object with some kind of length and give it an invalid length and this kind of errors will show up.

4. What is a ‘type error’?
* this types of errors show up when the types (number, string and so on) you are trying to use or access are incompatible, like accessing a property in an undefined type of variable.

5. What is a breakpoint?
* In the debugger window, you can set breakpoints in the JavaScript code. At each breakpoint, JavaScript will stop executing, and let you examine JavaScript values. After examining values, you can resume the execution of code (typically with a play button).

6. What does the word ‘debugger’ do in your code?
* A debugger is a software tool that can help the software development process by identifying coding errors at various stages of the operating system or application development. Some debuggers will analyze a test run to see what lines of code were not executed.

## Things I want to know more about
*I knew most of that mentioned in these articles through Course and some of it from before... but what is strange that this is the first time I focus on what is stack overflow!
 what I want to learn about is effective way to detect the errors and handle it properly.
