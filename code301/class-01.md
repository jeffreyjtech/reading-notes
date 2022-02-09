# [Read 01 - Introduction to React and Components](https://codefellows.github.io/code-301-guide/curriculum/class-01/DISCUSSION)

## [Component-Based Architecture](https://www.tutorialspoint.com/software_architecture_design/component_based_architecture.htm)

1. What is a “component”?
    - The reading defines components in many different ways so I will answer this question with my own detailed interpretation: A component is an abstract representation of specific tool within an application or software system. Components are used to organize the code-as-written of software into discrete monolithic parts with controlled internal behavior and pre-defined inputs & outputs. Components are very useful for defining software requirements without actually writing software. Sometimes, components are used as the model for the basic structure of a software language or library, but the concept of components has broad applications across software development beyond the languages purpose-made to model them.
2. What are the characteristics of a component?
    - Components are reuseable, meaning they are designed (usually) to have more than one application or work in more than one situation.
    - They're replaceable, so that similar components can take each other's place.
    - They're not context-specific. They can be used in different situations. This characteristic strengthens the above two characteristics.
    - Components are extensible, so they can provide new behavior when used with other components.
    - Encapsulated: A component does expose any of its internal processes, data, or its state.
    - Components are independent. By design, they should have minimal dependencies on other components.
3. What are the advantages of using component-based architecture?
    - The advantages of component-based architecture is that each piece of a system is modular and cellular in nature. Modular meaning that dependencies between components are not strictly pre-defined, and cellular meaning that, once the correct input(s) have been provided, a component "minds its own business" to accomplish its task. These two broad traits are conducive to reducing complexity in a system and improving its resilience when something needs to be changed.

## [What is Props and How to Use it in React](https://itnext.io/what-is-props-and-how-to-use-it-in-react-da307f500da0#:~:text=%E2%80%9CProps%E2%80%9D%20is%20a%20special%20keyword,way%20from%20parent%20to%20child)

1. What is “props” short for?
    - "Props" is short for **properties**.
2. How are props used in React?
    - Props ultimately define the data to be displayed in a component, whether it's given directly or passed down from a parent. At the code-level, a prop begins its lifecycle as an JS object. It's not technically a prop at this stage, but it will become one once it's passed into a React function/method call. At that point, the object becomes a prop and will be interpreted into React element attributes and values.
3. What is the flow of props?
    - Props flow one-way, from parent to child.

## Things I want to know more about

- What the heck is going on with these "React Element signatures" `<element />`?
  - Why is HTML markup in my JavaScript?
  - Is that even called the "React Element" signature?
  - What does it represent?
  - How is it algorithmically interpreted by React/JS?
  - Is this signature exclusive to React or is it a broader JavaScript feature which I have yet to be introduced to?
  - This article is hard to understand without knowing the composition and purpose of this yet unexplained syntax.
