# Read: 01 - Java Basics
![](https://blog.uniquez.co/wp-content/uploads/2021/01/word-image-30.jpeg)
# Language Basics
- ## Variables
1. Instance Variables (Non-Static Fields)
2. Class Variables (Static Fields)
3. Local Variables
4. Parameters

- Operators



|Operator| Precedence|
| --------- |------------ |
postfix|	expr++ expr--|
|unary	|++expr --expr +expr -expr ~ !
|multiplicative|	* / %
|additive	|+ -
|shift|	<< >> >>>
|relational|	< > <= >= instanceof
|equality	|== !=
|bitwise AND|	&
|bitwise exclusive OR|	^
|bitwise inclusive OR	|
|logical AND|	\&&
|logical OR|	\| \|
|ternary	|? :
|assignment	|= += -= *= /= %= &= ^= |= <<= >>= >>>=


## Reddit thread on compiling
###  What does it mean to compile code?
As you may know, everything in a computer is represented by a series of 1's and 0's (which themselves represent high and low voltages on transistors, but that's a topic for another time). When the computer runs a program, the program itself is made of a bunch of 1's and 0's.

However, since we still need humans to write our programs, putting everything in 1's and 0's (called machine language) would be very difficult. So we made higher level languages like Java and C# to write code in. These languages look a lot more like English, so they're a lot easier to write and maintain.

When you compile code, the compilor (usually another program) takes the program the human wrote, and converts it into the program the computer can understand (i.e. converts from Java to machine language). The very short version could be, yes, compile means to make the code executable.

Something you may run into is people saying code does or does not compile. This means the compilor they used checks to make sure their program is written correctly according to the rules of the programming language. For example, most programming languages make you put a semicolon (;) at the end of every line. A very common mistake is to forget that semicolon, so when you try and compile the compilor gives you an error.

It's also important to note that just because the code compiles doesn't mean it works. It's sort of like how 3 + 4 < 5 is an equation that has the right form, but it is incorrect.


## Compiling
![](https://imgs.xkcd.com/comics/compiling.png)



## Java’s API Documentation
Once upon a time, people judged programming languages (including Java) solely by their grammatical features. Does an if statement do what you expect it to do? Are looping statements easy to use? Are methods implemented efficiently?

Nowadays, things are a bit different. Java has a whole collection of grammatical features, but Java is much more than just a big set of grammar rules. Java has a standard Application Programming Interface —a huge library consisting of over 4,000 classes, each with its own functionality, its own limitations, and its own rules for effective use.


### Searching for a term
You can find things in the API documentation in a number of different ways. Each way is convenient in one situation or another. For example, Java has a method named System.out.println. What follows describes two ways to look up the System.out.println method.
- Using the index
1. Visit docs.oracle.com/javase/8/docs/api/.
2. Click the INDEX link at the top of the page to open the index
3. In the P section, do a search for println to find the println entries.
4. Pick one of the println entries.
5. Click the link for the entry that you’ve chosen.


- Using the list of classes
1. Visit [docs.oracle.com/javase/8/docs/api/](docs.oracle.com/javase/8/docs/api/).
2. Find the page that documents the System class.
3. On the documentation page for the System class, find the out variable.
4. In the table’s out row, click the PrintStream link.
5. On the documentation page for PrintStream, find println(String).