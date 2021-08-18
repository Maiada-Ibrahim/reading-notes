# In memory storage
![](https://cdn-media-1.freecodecamp.org/images/1*-WOpjPy_2Idl4jIAzPokRQ.jpeg)
## What is a ‘call’?
The call stack is primarily used for function invocation (call). Since the call stack is single, function(s) execution, is done, one at a time, from top to bottom. It means the call stack is synchronous.
## How many ‘calls’ can happen at once?
one at a time, from top to bottom. It means the call stack is synchronous.
## What does LIFO mean?
a call stack is a data structure that uses the Last In, First Out (LIFO) principle to temporarily store and manage function invocation (call).
![](https://cdn-media-1.freecodecamp.org/images/QgR2uIk7tW0YNz0Xm8g0jAPeRFI0e4sCejsv)
## Draw an example of a call stack and the functions that would need to be invoked to generate that call stack.
     function firstFunction(){
      console.log("Hello from firstFunction");
    }

     function secondFunction(){
     firstFunction();
      console.log("The end from    secondFunction");
     }

     secondFunction();
## What causes a Stack Overflow?
A stack overflow occurs when there is a recursive function (a function that calls itself) without an exit point. The browser (hosting environment) has a maximum stack call that it can accomodate before throwing a stack error.
The callMyself() will run until the browser throws a “Maximum call size exceeded”. And that is a stack overflow.


-------------------------
# JavaScript error messages && debugging
## What is a ‘refrence error’?
- This is as simple as when you try to use a variable that is not yet declared you get this type os errors.

## What is a ‘syntax error’?
this occurs when you have something that cannot be parsed in terms of syntax, like when you try to parse an invalid object using JSON.parse.
## What is a ‘range error’?
Try to manipulate an object with some kind of length and give it an invalid length and this kind of errors will show up.
An array for instance cannot have a negative length, why would you mess with the array length? Some people use it to set an array to empty
## What is a ‘tyep error’?
Like the name indicates, this types of errors show up when the types (number, string and so on) you are trying to use or access are incompatible, like accessing a property in an undefined type of variable.
## What is a breakpoint?
Tool in debugging the breakpoint can also be achieved by putting a debugger statement in your code in the line you want to break.
## What does the word ‘debugger’ do in your code?
To debug your JS code, the easiest and maybe the most common way its to simply console.log() the variables you want to check or, by using chrome developer tools, open your page with your JS code (press cmd+o in macOS or Ctrl+o in Windows) and choose your file to debug, click the line you wanna debug and refresh your page again (F5).