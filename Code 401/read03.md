# Java Primitives VS Objects

**Java system types**: 

* Autoboxing:
* convert the primitive type to the reference type.
* Unboxing:
* convert the reference type to the reference type.
**Primitive type**
variables which stored in the memory.
>Examples:
int
double
float

**Reference type**
reference to the index which stored in the heap.
>Examples:
Integer
Double
Float

# Exceptions in Java
Exceptionis is an event that occurs during the execution of a program that disrupts the normal flow of instructions.
Catch means that catch the problem and handle it.
* Types of exceptions:  
* 1 checked exception.
* 2 Unchecked exeption:
* error
* runtime exception
* Try-with-resources Statement
The try-with-resources statement is a try statement that declares one or more resources. A resource is an object that must be closed after the program is finished with it. The try-with-resources statement ensures that each resource is closed at the end of the statement. Any object that implements java.lang.AutoCloseable, which includes all objects which implement java.io.Closeable, can be used as a resource.

## How to Throw Exceptions
Before you can catch an exception, some code somewhere must throw one. Any code can throw an exception: your code, code from a package written by someone else such as the packages that come with the Java platform, or the Java runtime environment. Regardless of what throws the exception, it's always thrown with the throw statement.
>throw someThrowableObject;

## Using Scanner to read in a file in Java:

* Objects of type Scanner are useful for breaking down formatted input into tokens and translating individual tokens according to their data type.(3)

* Scanner also supports tokens for all of the Java language's primitive types (except for char).