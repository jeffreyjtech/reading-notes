# Read 05 - Putting it all together

## [React Docs - Thinking in React](https://reactjs.org/docs/thinking-in-react.html)

1. **What is the single responsibility principle and how does it apply to components?**
    - A component should really only do one thing. A large component which you're about to add more features to might be better if broken up into smaller subcomponents.
    ---
2. **What does it mean to build a ‘static’ version of your application?**
    - Create a version of your application which renders the data you're given, but has no interactivity.
    ---
3. **Once you have a static application, what do you need to add?**
    - Add the minimal amount of state required to achieve the desired interactive features.
    ---
4. **What are the three questions you can ask to determine if something is state?**
      1. Is it given from a parent via props? If so, it's not state.
      2. Is it static in the colloquial sense? If so, it's not state.
      3. Can it be processed from other data available to the component, such as another state or props? If so, it isn't state.
    ---
5. **How can you identify where state needs to live?**
    - Generally, state should live in the parent component that contains any and all children which will be affected by it. It can then use that state to govern it's children.
    ---

## [Higher-Order Functions](https://eloquentjavascript.net/05_higher_order.html#h_xxCc98lOBK)

1. **What is a “higher-order function”?**
    - A higher order function is one that can use multiple different functions to perform a similar task with each function or mutate each function in a similar way.
    ---
2. **Explore the greaterThan function as defined in the reading. In your own words, what is line 2 of this function doing?**
    - Line 2 is returning a new function, with a parameter `m`, which uses the higher-order parameter `n` as the reference value to compare `m` against.
    ---
3. **Explain how either map or reduce operates, with regards to higher-order functions.**
    - `map` uses a lower order function to create a new array from an existing array.
    ---

## Things I want to know more about

- What other strategies are there for using React besides the 5-step strategy in the reading? Those steps seem geared to make a brand new component set. The careful considerations at each step seem a bit optimistic if you're working on a complex, living codebase.

- Will we practice using higher order functions 301 or 401?
