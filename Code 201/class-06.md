## WHAT IS A FUNCTION?
Functions let you group a series of statements together to perform a
specific task. If different parts of a script repeat the same task, you can
reuse the function (rather than repeating the same set of statements). 

A JavaScript function is defined with the function keyword, followed by a name, followed by parentheses ().

Function names can contain letters, digits, underscores, and dollar signs (same rules as variables).

The parentheses may include parameter names separated by commas:
(parameter1, parameter2, ...)

The code to be executed, by the function, is placed inside curly brackets: {}

```
function name(parameter1, parameter2, parameter3) {
  // code to be executed
}
```
## Calling a Function
The code inside the function will execute when "something" invokes (calls) the function:

+ When an event occurs (when a user clicks a button)
+ When it is invoked (called) from JavaScript code
+ Automatically (self invoked)

### Document Object Model

**The Document Object Model (DOM)** specifies
how browsers should create a model of an HTML
page and how JavaScript can access and update the
contents of a web page while it is in the browser window.

**THE DOM TREE IS A MODEL OF A WEB PAGE**
*As a browser loads a web page, it creates a model of that page.
The model is called a DOM tree, and it is stored in the browsers' memory.
It consists of four main types of nodes.*
BODY OF HTML PAGE
```
<html>
<body>
<di v id="page">
<hl id="header">List</hl>
<h2>Buy groceries</h2>
<ul >
<li id="one" class="hot"><em>fresh</em> figs</li>
<li id="two" class="hot">pine nuts</l i>
<l i id="three" class="hot">honey</l i >
<l i id="four">balsamic vinegar</l i>
</ ul >
<script src="js/l i st.js "></scri pt>
</ div>
</ body>
</ html > 

```

**THE DOCUMENT NODE**
Above, you can see the HTML code for a shopping list, and on the right hand page is its DOM tree.
Every element, attribute, and piece of text in the HTML is represented by its own DOM node.
At the top of the tree a document node is added; it represents the entire page.

Each node is an object with methods and properties.
Scripts access and update this DOM tree (not the source HTML file).
Any changes made to the DOM tree are reflected in the browser. 

![img](https://upload.wikimedia.org/wikipedia/commons/thumb/5/5a/DOM-model.svg/1200px-DOM-model.svg.png)

# WORKING WITH THE DOM TREE
Accessing and updating the DOM tree involves two steps:
1- Locate the node that represents the element you want to work with.
2- Use its text content, child elements, and attributes.

# SELECTING ELEMENTS USING ID ATTRIBUTES 

getElementByid () allows you to select a single element node
by specifying the value of its id attribute.
This method has one parameter: the value of the id attribute on
the element you want to select. This value is placed inside quote
marks because it is a string. The quotes can be single or double
quotes, but they must match.

```
II Select the element and store it in a variable.
var el = document.getElementByid('one');
II Change the value of the class attribute.
el.className ='cool ' ; 
```
A Nodelist is a collection of element nodes. Each
node is given an index number (a number that starts
at zero, just like an array).

When a DOM query returns a Nodelist, you may
want to:
• Select one element from the NodeList.
• Loop through each item in the Nodelist and
perform the same e statements on each of the
element nodes. 

*Here you can see four different DOM queries that all return a Nodelist.
For each query, you can see the elements and their index numbers in the
Nodelist that is returned.*

+ getElementsByTagName('hl ' ) 
+ getElementsByTagName('li ') 
+ getElementsByClassName('hot') 
+ querySe l ectorA 11 ( ' l i [id] ' ) 

**SELECTING AN ELEMENT FROM A NODELIST**
Nodelists have a method called item() which will return
an individual node from the Node list. 
There are two ways to select an element from a Nodelist:
The item() method and array syntax.
Both require the index number of the element you want. 

> var elements = document.getElementsByClassName('hot')
if (elements.length>= 1) {
var firstltem = elements.item(O);
} 

# HOW TO GET/UPDATE ELEMENT CONTENT

To work with the content of elements you can: 

+ Navigate to the text nodes. This works best
when the element contains only text, no other
elements.
• Work with the containing element. This allows
you to access its text nodes and child elements.
It works better when an element has text nodes
and child elements that are siblings. 


# ACCESSING & CHANGING A TEXT NODE 
To work with text in an element,
first the element node is accessed and then its text node.

The text node has a property called node Value which returns the text in that text node.

## What is the hardest thing about writing code?

There are many common answers to this question:

-Learning a new technology
-Naming things
-Testing your code
-Debugging
-Fixing bugs
-Making software maintainable

 If understanding the problem domain is the hardest part of programming and you want to make programming easier, you can do one of two things:

+ Make the problem domain easier
+ Get better at understanding the problem domain

You can often make the problem domain easier by cutting out cases and narrowing your focus to a particular part of the problem.

