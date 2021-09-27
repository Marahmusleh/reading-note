# Packages and Import

Package = directory. Java classes can be grouped together in packages. A package name is the same as the directory (folder) name which contains the .java files. You declare packages when you define your Java program, and you name the packages you want to use from other libraries in an import statement.

## Package declaration

The first statement, other than comments, in a Java source file, must be the package declaration.
Package declaration syntax
The statement order is as follows. Comments can go anywhere.
```
Package statment (optional).
Imports (optional).
Class or interface definitions.
// This source file must be Drawing.java in the illustration directory.

package illustration;

import java.awt.*;

public class Drawing {
    . . .
}
```
## Common imports
There are 166 packages containing 3279 classes and interfaces in Java 5. However, only a few packages are used in most programming. GUI programs typically use at least the first three imports.

```
import java.awt.*;	Common GUI elements.
import java.awt.event.*;	The most common GUI event listeners.
import javax.swing.*;	More common GUI elements. Note "javax".
import java.util.*;	Data structures (Collections), time, Scanner, etc classes.
import java.io.*;	Input-output classes.
import java.text.*;	Some formatting classes.
import java.util.regex.*;	Regular expression classes.
```

* Q: Does importing all classes in a package make my object file (.class or .jar) larger?

A: No, import only tells the compiler where to look for symbols.

* Q: Is it less efficient to import all classes than only the classes I need?

A: No. The search for names is very efficient so there is no effective difference.

# Loops

In programming languages, looping is a feature which facilitates the execution of a set of instructions until the controlling Boolean-expression evaluates to false.

1- For Loops

A for loop is a control structure that allows us to repeat certain operations by incrementing and evaluating a loop counter.

2- While Loop

The while loop is Java's most fundamental loop statement. It repeats a statement or a block of statements while its controlling Boolean-expression is true.

3- Do-While Loop

The do-while loop works just like the while loop except for the fact that the first condition evaluation happens after the first iteration of the loop.