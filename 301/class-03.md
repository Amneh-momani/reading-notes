## React Docs - lists and keys
+ 1- It returns the elements from the array with or without any opration and it returns all of the array's element even if it wasn't defined 
+ 2- By using map method or Foreach and decide the arguments that you want to pass it and using props if it was more than one element
+ 3- by using a string then it will be like a key to become the list item unique and decide it whenever we want to use it 
+ 4-when we want creating lists of elements then we need to include a **key** is a special string attribute.

## The Spread Operator
_Spread operator to the rescue and it looks similar to rest parameters, also using **...**, but does quite the opposite._
So it's a three dots to expand an iterable object into the list of arguments.

The **...** spread operator is useful for many different routine tasks in JavaScript, including the following:
+ Copying an array
+ Concatenating or combining arrays
+ Using Math functions
+ Using an array as arguments
+ Adding an item to a list

Example of spread operator to combine two arrays:

          const myArray = [`🤪`,`🐻`,`🎌`]
          const yourArray = [`🙂`,`🤗`,`🤩`]
          const ourArray = [...myArray,...yourArray]
          console.log(...ourArray) // 🤪 🐻 🎌 🙂 🤗 🤩

Example of spread operator to add a new item to an array:

         const fewFruit = ['🍏','🍊','🍌']
         const fewMoreFruit = ['🍉', '🍍', ...fewFruit]
         console.log(fewMoreFruit) //  Array(5) [ "🍉", "🍍", "🍏", "🍊", "🍌" ]


Example of operator to combine two objects into one:

          const objectOne = {hello: "🤪"}
          const objectTwo = {world: "🐻"}
          const objectThree = {...objectOne, ...objectTwo, laugh: "😂"}
          console.log(objectThree) // Object { hello: "🤪", world: "🐻", laugh: "😂" }
          const objectFour = {...objectOne, ...objectTwo, laugh: () => {console.log("😂".repeat(5))}}
          objectFour.laugh() // 😂😂😂😂😂


## How to Pass Functions Between Components

The first step that the developer does to pass functions between components is creating a function and passing the objects by it so it will show which object that we want to pass by it's properites 

The increment is a function which has an array to match updates of the app itself then return these updates which happened in the app .

 we can pass a method from a parent component into a child component by using **props** so we have to make extends from the child component to the parent component.

 The child component invoke a method that was passed to it from a parent component by calling a child function in the parent component and pass it to the child by props 

## Lifting State Up
There's many components need to reflect the same changing data so we should raising joint status to the closest common ancestor.

Example:

          function BoilingVerdict(props) {
            if (props.celsius >= 100) {
              return <p>The water would boil.</p>;
            }
            return <p>The water would not boil.</p>;
          }

          
