# Read 02 - State and Props

## React Lifecycle

1. Based off the diagram, what happens first, the ‘render’ or the ‘componentDidMount’?
    - The render
2. What is the very first thing to happen in the lifecycle of React?
    - The mounting phase, which starts with calling the constructor
3. Put the following things in the order that they happen: `componentDidMount`, `render`, `constructor`, `componentWillUnmount`, `React Updates`
    1. `constructor`
    2. `render`
    3. `React Updates` 
        - (this answer assumes that "React Updates" is short for React is updating or manipulating the DOM, otherwise this would be after `componentDidMount`)
    4. `componentDidMount`
    5. `componentWillUnmount`
4. What does componentDidMount do?
    - The componentDidMount method is a common, but optional, lifecycle method in React components. It's invoked immediately after a component is mounted ([reference](https://reactjs.org/docs/react-component.html#componentdidmount)). In other words, this method is called when the component has finally been inserted into the DOM node tree.

## Things I want to know more about

- The definition for componentDidMount's in [the reading](https://medium.com/@joshuablankenshipnola/react-component-lifecycle-events-cb77e670a093) mentions that it's a "good place to set up any subscriptions". What are "subscriptions" in this context?
