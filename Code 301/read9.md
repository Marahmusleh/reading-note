## FUNCTIONAL PROGRAMMING
## Functional Programming Concepts:
1. What is functional programming?

* a style of building the structure and elements of computer programs.
2. What is a pure function and how do we know if something is a pure function?

* functions that accept an input and returns a value without modifying any data outside its scope.
3. What are the benefits of a pure function?

* The code is easier to test.
4. What is immutability?

* When data is immutable, its state cannot change after it’s created. If you want to change an immutable object, you can’t. Instead, you create a new object with the new value.
5. What is Referential transparency?

* this is what happens when you have pure functions and immutable data. So, for example, if one replaced a function with a number that the function would always result to, that would give it referential transparency.

## Nodejs Modules and require():
1. What is a module?

* Module in Node. js is a simple or complex functionality organized in single or multiple JavaScript files which can be reused throughout the Node. js application. Each module in Node. js has its own context, so it cannot interfere with other modules or pollute global scope.
2. What does the word ‘require’ do?

* to load and cache JavaScript modules.
3. How do we bring another module into the file the we are working in?

* Require will import the module, and enable us to use its functionality.
4. What do we have to do to make a module available?

module.export ,the part that we need to share with the other files
