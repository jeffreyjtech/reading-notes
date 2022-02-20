Read 03 - Passing Functions as Props

## [React Docs - lists and keys](https://reactjs.org/docs/lists-and-keys.html)

1. What does .map() return?
    - Well, first, `.map()` invokes a given function for each element in an array. The return of `.map()` is an array of each return value from each invocation of the sub-function.
2. If I want to loop through an array and display each value in JSX, how do I do that in React?
    - Any technique for iterating through an array works, but `.map()` does what you need "out of the box". Take an array of data which you wish to process into components or JSX elements, process it into an array of JSX elements `.map()` and mapping function, then insert the resulting array into a parent JSX element using curly brackets. Make sure to give a unique key to each JSX element in the computed array.
3. Each list item needs a unique ____.
    - Key.
4. What is the purpose of a key?
    - The purpose of a key is to allow React to properly identify and track elements in arrays of JSX elements.

## [The Spread Operator](https://medium.com/coding-at-dawn/how-to-use-the-spread-operator-in-javascript-b9e4a8b06fab)



## [How to Pass Functions Between Components](https://www.youtube.com/watch?v=c05OL7XbwXU)
