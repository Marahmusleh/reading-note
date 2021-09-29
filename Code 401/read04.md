# Object-Oriented Programming

## What Is an Object?

An object is a software bundle of related state and behavior. Software objects are often used to model the real-world objects that you find in everyday life. 

An object stores its state in fields (variables in some programming languages) and exposes its behavior through methods (functions in some programming languages)Methods operate on an object's internal state and serve as the primary mechanism for object-to-object communication. Hiding internal state and requiring all interaction to be performed through an object's methods is known as **data encapsulation** — a fundamental principle of object-oriented programming.

### Bundling code into individual software objects provides a number of benefits, including:

* Modularity: The source code for an object can be written and maintained independently of the source code for other objects. Once created, an object can be easily passed around inside the system.
* Information-hiding: By interacting only with an object's methods, the details of its internal implementation remain hidden from the outside world.
* Code re-use: If an object already exists (perhaps written by another software developer), you can use that object in your program. This allows specialists to implement/test/debug complex, task-specific objects, which you can then trust to run in your own code.
* Pluggability and debugging ease: If a particular object turns out to be problematic, you can simply remove it from your application and plug in a different object as its replacement. 

## What is a class?

 A class is the blueprint from which individual objects are created.

When the individual objects are created, they inherit all the variables and methods from the class.

>You can also create an object of a class and access it in another class. This is often used for better organization of classes (one class has all the attributes and methods, while the other class holds the main() method (code to be executed)).

class declarations can include these components, in order:

* Modifiers such as public, private, and a number of others that you will encounter later. (However, note that the private modifier can only be applied to Nested Classes.)
* The class name, with the initial letter capitalized by convention.
* The name of the class's parent (superclass), if any, preceded by the keyword extends. A class can only extend (subclass) one parent.
* A comma-separated list of interfaces implemented by the class, if any, preceded by the keyword implements. A class can implement more than one interface.
* The class body, surrounded by braces, {}.

### Enum Types

An enum type is a special data type that enables for a variable to be a set of predefined constants. The variable must be equal to one of the values that have been predefined for it. Common examples include compass directions (values of NORTH, SOUTH, EAST, and WEST) and the days of the week.

Because they are constants, the names of an enum type's fields are in uppercase letters.

In the Java programming language, you define an enum type by using the enum keyword. For example, you would specify a days-of-the-week enum type as:

```
public enum Day {
    SUNDAY, MONDAY, TUESDAY, WEDNESDAY,
    THURSDAY, FRIDAY, SATURDAY 
}
```
## Binary, Decimal and Hexadecimal Numbers:
* Decimals:
Every digit in a decimal number has a "position", and the decimal point helps us to know which position is which. The position just to the left of the point is the "Ones" position. Every position further to the left is 10 times bigger, and every position further to the right is 10 times smaller.

* Bases:
The Decimal Number System is also called "Base 10", because it is based on the number 10. with these 10 symbols but notice something interesting: there is no symbol for "ten". "10" is actually two symbols put together, a "1" and a "0".

*Counting with Different Number Systems:*
But you don't have to use 10 as a "Base". You could use 2 ("Binary"), 16 ("Hexadecimal"), or any number you want to. For example:
>In binary you count "0,1,..." but then you run out of symbols! So you add 1 on the left and then start again at 0: 10,11 ...

So the general rule is: Count up until just before the "Base Number", then start at 0 again, but first you add 1 to the number on your left.

* Binary Numbers:
are just "Base 2" instead of "Base 10". So you start counting at 0, then 1, then you run out of digits ... so you start back at 0 again, but increase the number on the left by 1.

Hexadecimal Numbers:
They look the same as the decimal numbers up to 9, but then there are the letters ("A',"B","C","D","E","F") in place of the decimal numbers 10 to 15. So a single Hexadecimal digit can show 16 different values instead of the normal 10.