# FUNCTIONAL PROGRAMMING
# What is functional programming?
Functional programming is a programming paradigm — a style of building the structure and elements of computer programs — that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data 
# What is a pure function and how do we know if something is a pure function?
![](https://miro.medium.com/max/875/0*FMur6URY7yAVjeuP)
It returns the same result if given the same arguments (it is also referred as deterministic)
It does not cause any observable side effects
It returns the same result if given the same arguments
Imagine we want to implement a function that calculates the area of a circle. An impure function would receive radius as the parameter, and then calculate radius * radius * PI:
# What are the benefits of a pure function?
The code’s definitely easier to test. We don’t need to mock anything. So we can unit test pure functions with different contexts
# What is immutability?
Unchanging over time or unable to be changed.
# What is Referential transparency?
![](https://miro.medium.com/max/875/0*K0VAbQjAwmKZb1at)
Basically, if a function consistently yields the same result for the same input, it is referentially transparent.


## What is a module?
essentially another javascript file
## What does the word ‘require’ do?
on the global object in nodejs so can use it whereever we sre so
## How do we bring another module into the file the we are working in?
use require
## What do we have to do to make a module available?
module dot exports and sit this equal to what ever we went