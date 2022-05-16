# Read 37 - Redux - Combined Reducers

## Summary Notes

* State in Redux, as it's most often used, is a collection of state "slices" which each have a reducer.
* In order to use multiple reducers to create a single store, the `combinedReducers` function from Redux is used.
  * `combineReducers` is a higher-order reducer function which takes in multiple reducer functions and returns a new reducer function.
  * `combineReducers` is a utility function which may not cover all use cases, it enforces rules to help developers avoid common errors.
* State shape can be with the `createStore` function
  * It takes in an optional `preloadedState` object as a 2nd argument.
* `combineReducers` takes in an object which has key-value pairs `sliceName: myReducerFunction`
  * The key name will define the name of the slice as the store object is accessed in consumers of state.
  * In other words, the state produced by `combineReducers` namespaces the states of each reducer under their keys.
* Any reducer given to `combineReducers` must:
  * Return the `state` parameter for an unrecognized argument
  * Never return `undefined`
  * Return the initial state if the `state` parameter is undefined.
* An action in multiple reducers can be triggered by one dispatch, so long as the action names are the same.
