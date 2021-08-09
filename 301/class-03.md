# Passing Functions as Props
- ## What does .map() return?
### We return a \<li> element for each item. Finally, we assign the resulting array of elements to listItems

- ## If I want to loop through an array and display each value in JSX, how do I do that in React?
map()

- ## Each list item needs a unique  key .
- ## What is the purpose of a key?
Keys help React identify which items have changed, are added, or are removed. Keys should be given to the elements inside the array to give the elements a stable identity


## [check her to read more ](https://reactjs.org/docs/lists-and-keys.html)
----------------------------------------------
## What is the spread operator?
refers to the use of an ellipsis of three dots (…) to expand an iterable object into the list of arguments.
## List 4 things that the spread operator can do.
- Take trying to find the largest number in an array with Math.max():
- Concatenating or combining arrays
-Using Math functions
- Using an array as arguments
- Adding an item to a list
## Give an example of using the spread operator to combine two arrays.
               const myArray = [`🤪`,`🐻`,`🎌`]
               const yourArray = [`🙂`,`🤗`,`🤩`]
               const ourArray = [...myArray,...yourArray]
               console.log(...ourArray) // 🤪 🐻 🎌 🙂 🤗 🤩

## Give an example of using the spread operator to add a new item to an array.
            const fewFruit = ['🍏','🍊','🍌']
            const fewMoreFruit = ['🍉', '🍍', ...fewFruit]
            console.log(fewMoreFruit) //  Array(5) [ "🍉", "🍍", "🍏", "🍊", "🍌" ]

## Give an example of using the spread operator to combine two objects into one.
        const objectOne = {hello: "🤪"}
        const objectTwo = {world: "🐻"}
        const objectThree = {...objectOne, ...objectTwo, laugh: "😂"}
        console.log(objectThree) // Object { hello: "🤪", world:  "🐻", laugh: "😂" }
        const objectFour = {...objectOne, ...objectTwo, laugh: () => {console.log("😂".repeat(5))}}
       objectFour.laugh() // 😂😂😂😂😂


## [check her to read more ](https://medium.com/coding-at-dawn/how-to-use-the-spread-operator-in-javascript-b9e4a8b06fab)

## In the video, what is the first step that the developer does to pass functions between components?
creat  increment function
## In your own words, what does the increment function do?
pass inforimation btween components when we change or update some thing
## How can you pass a method from a parent component into a child component?
use state 
## How does the child component invoke a method that was passed to it from a parent component?
 increment method

## [check her to see the vidio ](https://www.youtube.com/watch?v=c05OL7XbwXU)
## Things I want to know more about
I didnt under stand the vedio I need to kow how How does the child component invoke a method that was passed to it from a parent component?