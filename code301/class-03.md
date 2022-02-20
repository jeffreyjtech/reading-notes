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

1. What is the spread operator?
    - It expands an iterable object, typically an array, for use in expressions which need non-array collections of data. "Non-array collections of data" means things like key-value pairs in an object, the multiple arguments of a function call, the list of values in an array assignment.
2. List 4 things that the spread operator can do.
    - The spread operator can expand an array into multiple arguments in a function call
    - It can expand an array into another array.
    - It can be used to combine objects.
    - It can add items to a list.
3. Give an example of using the spread operator to combine two arrays.

    - ```js
      let arrayOne = [1,2,3];
      let arrayTwo = [4,5,6];

      let combinedArray = [...arrayOne,...arrayTwo];
      ```

4. Give an example of using the spread operator to add a new item to an array.

    - ```js
      let arrayThree = [7,8,9];

      let arraySevenToTen = [arrayThree,10];
      ```

5. Give an example of using the spread operator to combine two objects into one.

    - ```js
      let objectA = {potato: patato};
      let objectB = {tomato: tamato}

      let combinedObject = {...objectA,...objectB}
      ```

## [How to Pass Functions Between Components](https://www.youtube.com/watch?v=c05OL7XbwXU)

1. In the video, what is the first step that the developer does to pass functions between components?
    - Ans
2. In your own words, what does the `increment` function do?
    - Ans
3. How can you pass a method from a parent component into a child component?
    - Ans
4. How does the child component invoke a method that was passed to it from a parent component?
    - Ans
