# What's a Table?

A table represents information in a grid format.
Examples of tables include financial reports, TV
schedules, and sports results.

**Basic Table Structure**
```
 <table>
 <tr>
 <td>15</td>
 <td>15</td>
 <td>30</td>
 </tr>
 <tr>
 <td>45</td>
 <td>60</td>
 <td>45</td>
 </tr>
 <tr>
 <td>60</td>
 <td>90</td>
 <td>90</td>
 </tr>
</table>

```
There are three elements that help distinguish between the
main content of the table and the first and last rows (which can
contain different content). These elements help people
who use screen readers and also allow you to style these sections
in a different manner than the rest of the table (as you will see
when you learn about CSS).

```
<thead>
The headings of the table should
sit inside the <thead> element.
<tbody>
The body should sit inside the
<tbody> element.
<tfoot>
The footer belongs inside the
<tfoot> element.
```

+ Width & Spacing
The width attribute was used on the opening < table > tag to
indicate how wide that table should be and on some opening
< th > and < td > tags to specify the width of individual cells.
The value of this attribute is the width of the table or cell in pixels.
The columns in a table need to form a straight line, so you often
only see the width attribute on the first row (and all subsequent
rows would use that setting).
  
# WHAT IS AN OBJECT? 

*Objects group together a set of variables and functions to create a model
of a something you would recognize from the real world. In an object,
variables and functions take on new names.*
  
+ If a variable is part of an object, it is called a
**property** .
+ If a function is part of an object, it is called a **method.**
Methods represent tasks that are associated with
the object.

```
var hote l = {
name: 'Quay',
rooms: 40,
booked : 25,
checkAvailability: function() {
return this.rooms - this.booked;
}
} ;
var el Name = document .getElementByld('hotelName');
elName.textContent =hotel .name;
var elRooms = document.getElementByid{'rooms');
elRooms.textContent = hotel .checkAvailability(); 

```
# CREATING MANY OBJECTS:CONSTRUCTOR NOTATION

>Sometimes you will want several objects to represent similar things.
Object constructors can use a function as a template for creating objects.
First, create the template with the object's properties and methods.

# THIS (IT IS A KEYWORD) 

The keyword this is commonly used inside functions and objects.
Where the function is declared alters what this means. It always refers
to one object, usually the object in which the function operates. 

**A FUNCTION IN GLOBAL SCOPE**
When a function is created at the top level of a script
(that is, not inside another object or function), then it
is in the global scope or global context.
The default object in this context is the window
object. so when this is used inside a function in the
global context it refers to the window object.

**GLOBAL VARIABLES**
All global variables also become properties of the
window object. so when a function is in the global
context, you can access global variables using the
window object, as well as its other properties.

# WHAT ARE BUILT-IN OBJECTS?

Browsers come with a set of built-in objects that represent things like the
browser window and the current web page shown in that window. These
built-in objects act like a toolkit for creating interactive web pages. 

The first thing you need to do is get to know what tools are available.
You can imagine that your new toolkit has three compartments: 

+ BROWSER OBJECT MODEL
+ DOCUMENT OBJECT MODEL
+ GLOBAL JAVASCRIPT OBJECTS

  
