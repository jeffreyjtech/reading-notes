# Context API

## Summary Notes

- The React Context API a tool for passing data between components without the strict parent-to-child constraints of props.
- It is most useful for when sibling components need to share data between each other, and it would not be prudent for the parent to have access to this.
- The `React.createContext` method will take in a default value for the context you wish to store.
- It will also return a Context object, which itself has a Provider component.
  - When this Provider Component is inserted into the DOM, any child components can become consumers for the context provider.
- You can also export the object used to the create the context.
