# Read 36 - Application State with Redux

## Summary Notes

* Redux stores application state in a single object, called the state or state tree
* All changes to state in Redux are explicit.
* The state object is technically read only, it must be modified by dispatching an action.
* It is important to know what a pure function is for Redux
  * A pure function does not have any side effects, and their output must depend solely on the arguments provided.
* Actions are also just objects, and in them we store information about the action's type and payload using properties of that name.
* Actions are typically created using action creator functions which are exported to other modules in our code.
  * Conceptually action creators are meant to create an interface layer between our other modules and Redux, so our modules are not coupled to implementation details that come from using Redux.
* Actions are ultimately used in a reducer function, which we create in order to change state as needed by a given action.
  * The reducer function must always return a state object.
* The Redux library provides a function `createStore()` which takes in a reducer function and returns a store object.
* The `dispatch()` method on the store object will create an action if it's provided an object with a `type` and (optionally) a `payload` property.
  * The `type` is a string which should enable some conditional logic in the reducer function.
  * The `payload` property can be anything, whatever needs to be provided to the reducer function for state to be changed as we need it to be.
