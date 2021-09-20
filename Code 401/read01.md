# Java Basics

## Variables 

The Java programming language defines the following kinds of variables:

* Instance Variables (Non-Static Fields) Technically speaking, objects store their individual states in "non-static fields", that is, fields declared without the static keyword. Non-static fields are also known as instance variables because their values are unique to each instance of a class (to each object, in other words).
* Class Variables (Static Fields) A class variable is any field declared with the static modifier; this tells the compiler that there is exactly one copy of this variable in existence, regardless of how many times the class has been instantiated. A field defining the number of gears for a particular kind of bicycle could be marked as static since conceptually the same number of gears will apply to all instances. The code static int numGears = 6; would create such a static field. Additionally, the keyword final could be added to indicate that the number of gears will never change.
* Local Variables Similar to how an object stores its state in fields, a method will often store its temporary state in local variables. The syntax for declaring a local variable is similar to declaring a field (for example, int count = 0;). There is no special keyword designating a variable as local; that determination comes entirely from the location in which the variable is declared — which is between the opening and closing braces of a method. As such, local variables are only visible to the methods in which they are declared; they are not accessible from the rest of the class.
* Parameters,Example: main method:
Recall that the signature for the main method is public static void main(String[] args). Here, the args variable is the parameter to this method.parameters are always classified as "variables" not "fields". 

## Naming 

* Variable names are case-sensitive, **always begin the variable names with a letter, not "$" or "_". White space is not permitted.**
* Subsequent characters may be letters, digits, dollar signs, or underscore characters. **use full words instead of cryptic abbreviations. Doing so will make your code easier to read and understand. the name you choose must not be a keyword or reserved word.**
* **If the name you choose consists of only one word, spell that word in all lowercase letters. If it consists of more than one word, capitalize the first letter of each subsequent word.** If your variable stores a constant value, such as static final int NUM_GEARS = 6, the convention changes slightly, capitalizing every letter and separating subsequent words with the underscore character. By convention, the underscore character is never used elsewhere.

### What are the eight primitive data types supported by the Java programming language? 
byte, short, int, long, float, double, boolean, char

## Default Values
*It's not always necessary to assign a value when a field is declared. Fields that are declared but not initialized will be set to a reasonable default by the compiler. Generally speaking, this default will be zero or null, depending on the data type. Relying on such default values, however, is generally considered bad programming style.*

## Arrays
*An array is a container object that holds a fixed number of values of a single type. The length of an array is established when the array is created. After creation, its length is fixed. You have seen an example of arrays already, in the main method of the "Hello World!" application. This section discusses arrays in greater detail.*

```
class ArrayDemo {
    public static void main(String[] args) {
        // declares an array of integers
        int[] anArray;

        // allocates memory for 10 integers
        anArray = new int[10];
           
        // initialize first element
        anArray[0] = 100;
        // initialize second element
        anArray[1] = 200;
   

        System.out.println("Element at index 0: "
                           + anArray[0]);
        System.out.println("Element at index 1: "
                           + anArray[1]);
     
    }
} 
The output from this program is:

Element at index 0: 100
Element at index 1: 200

```

> Similarly, you can declare arrays of other types:

* byte[] anArrayOfBytes;
* short[] anArrayOfShorts;
* long[] anArrayOfLongs;
* float[] anArrayOfFloats;
* double[] anArrayOfDoubles;
* boolean[] anArrayOfBooleans;
* char[] anArrayOfChars;
* String[] anArrayOfStrings;

> You can also place the brackets after the array's name:
float anArrayOfFloats[];

## Operators

* Postfix: expr++ expr--
* Unary: ++expr --expr +expr -expr ~ !
* Multiplicative: * / %
* Additive: + -
* Relational: < > <= >= instanceof
* Equality: == !=
* Logical AND: &&
* Logical OR: ||
* Ternary: ? :
* Bitwise AND: &
* Bitwise exclusive OR: ^
* Bitwise inclusive OR: |
* Shift: << >> >>>
* Assignment: = += -= *= /= %= &= ^= |= <<= >>= >>>=

```

Simple Assignment Operator
=       Simple assignment operator
Arithmetic Operators
+       Additive operator (also used
        for String concatenation)
-       Subtraction operator
*       Multiplication operator
/       Division operator
%       Remainder operator
Unary Operators
+       Unary plus operator; indicates
        positive value (numbers are 
        positive without this, however)
-       Unary minus operator; negates
        an expression
++      Increment operator; increments
        a value by 1
--      Decrement operator; decrements
        a value by 1
!       Logical complement operator;
        inverts the value of a boolean
Equality and Relational Operators
==      Equal to
!=      Not equal to
>       Greater than
>=      Greater than or equal to
<       Less than
<=      Less than or equal to
Conditional Operators
&&      Conditional-AND
||      Conditional-OR
?:      Ternary (shorthand for 
        if-then-else statement)
Type Comparison Operator
instanceof      Compares an object to 
                a specified type 
Bitwise and Bit Shift Operators
~       Unary bitwise complement
<<      Signed left shift
>>      Signed right shift
>>>     Unsigned right shift
&       Bitwise AND
^       Bitwise exclusive OR
|       Bitwise inclusive OR


```
## Expressions, Statements, and Blocks

* Operators may be used in building expressions, which compute values.
* Expressions are the core components of statements.
* Statements may be grouped into blocks.
* The following code snippet is an example of a compound expression.
 1 * 2 * 3
* Statements are roughly equivalent to sentences in natural languages, but instead of ending with a period, a statement ends with a semicolon.
* A block is a group of zero or more statements between balanced braces and can be used anywhere a single statement is allowed.
Exercises
```
aValue = 8933.234; // assignment statement
aValue++; // increment statement
System.out.println("Hello World!"); // method invocation statement
Bicycle myBike = new Bicycle(); // object creation statement
```

## Control Flow Statements

* The most basic control flow statement supported by the Java programming language is the if-then statement.
* The switch statement allows for any number of possible execution paths.
* The do-while statement is similar to the while statement, but evaluates its expression at the bottom of the loop.
 ### How do you write an infinite loop using the for statement?
Answer:

for ( ; ; ) {

}
### How do you write an infinite loop using the while statement?
Answer:

while (true) {

}

## Compiling Java
It is the the action a computer takes to gather the human-readable code and translate it into the 1's and 0's required to make it machine-readable.

## Making Sense of Java’s API Documentation

### Searching for a term
You can find things in the API documentation in a number of different ways. Each way is convenient in one situation or another. For example, Java has a method named System.out.println. What follows describes two ways to look up the System.out.println method:
* You can use this index to find terms for Java's API documentation, Visit [Java™ Platform
Standard Ed. 8](https://docs.oracle.com/javase/8/docs/api/). This article also gives an explanation of how to use this index, and search for a specific package or class.
* To create the API documentation, the captains of Java ran a program called javadoc. The javadoc program took lines like these right out of the PrintStream.java file and used the lines to make the documentation that you see in your web browser.When you download the JDK, you get the javadoc program as part of the deal.


