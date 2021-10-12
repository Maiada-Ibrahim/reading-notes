# Read: 03 - Maps, primitives, File I/O
![](https://docs.microsoft.com/en-us/windows/win32/memory/images/fmap.png)
##  primitives
java has two Type System 
- primitives such as int, boolean 
- reference types such as Integer, Boolean as we known
we can convert between this type as this example :

                  Integer j = 1;          // autoboxing
                   int i = new Integer(1); // unboxing
we called this convarting  (autoboxing/unboxing) as the example

### space and fast
The reference types are objects, they live on the heap and are relatively slow to access so when we choose the type data we must try to choose correct type becasue the same data could take more space and slower if you choose reference types at byte and int not correct and at single-element arrays of primitive types are almost always more expensive (except for long and double) than the corresponding reference type.

 the primitive types live in the stack while the reference types live in the heap. This is a dominant factor that determines how fast the objects get be accessed.

 ## Default Values
 Default values of the primitive types are 0 (in the corresponding representation, i.e. 0, 0.0d etc) for numeric types, false for the boolean type, \u0000 for the char type. For the wrapper classes, the default value is null.

 so we prefer use primitive types because the Default values belong to its contant

 ## so after this Comparison the primitive types are much faster and require much less memory but reference types using with arametrized types (generics),  in the Java collections or the Reflection API.


--------------------------------------------------------------

## Exceptions in Java (read the first three sections on the left: What is an Exception, The Catch or Specify Requirement, Catching and Handling Exceptions)
Exceptions are errors that occur at runtime and disrupt the normal flow of execution of instructions in a program.

An exception object is created by the method in which an error occurs which is then handed over to the runtime system. This process is called throwing an exception. The object contains the details of the error, its type, etc.

An exception handler is the code that executes after an exception is encountered. The runtime method searches the call stack to find an appropriate method containing the code for handling the exception. The runtime system after receiving the exception tries to find a suitable way to handle it.

When the type of exception thrown matches the type of exception that can be handled, the exception is passed on to the handler so as to catch the exception. The three types of exceptions are:

checked exceptions, errors and runtime exceptions.

---------------------------------------------------------------

# Scanner
 class was introduced. This class accepts a File, InputStream, Path and, String objects, reads all the primitive data types and Strings (from the given source) token by token using regular expressions. By default, whitespace is considered as the delimiter (to break the data into tokens).

 how reading the contents of a file 
To read the contents of a file, Scanner class provides various constructors.
1. Scanner(File source)
Used to read data from the file represented by the given File object.
2. Scanner(InputStream source)
Used to read data from the specified InputStream.
3. Scanner(Path source)
Used to read data from the file represented by the specified file object.