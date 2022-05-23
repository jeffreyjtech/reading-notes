# Redux - Asynchronous Actions

## Summary Notes

* Redux reducer functions must not have side effects, which means that most async logic such as an AJAX request or an unresolved promise are not permitted in them.
* That said, Redux does support creating middleware which runs when an action is dispatched.
  * A multi-order function with the shape `myFunction = (store) => (next) => (action) => // logic goes here` can be "wired in" as Redux middleware.
* Redux middleware which conditionally executes a callback function can be used to handle async logic before the Redux "action -> reducer -> change state" flow properly starts.
  * This middleware can be coded manually or imported as `thunk` from Redux-thunk.
  * The callback function can potentially have the shape `myAsync callback = async (dispatch, getState) => // logic goes here`
  * The goal of this function signature is to execute the Redux dispatch after the async logic has executed.
* Applying middleware is done with the `applyMiddleware` function like so:

```js
const store = createStore(rootReducer, applyMiddleware(myMiddlewareFunction))
```

* With the special thunk middleware and a "thunkified" action creator will, we can send an ajax request AND THEN dispatch an action to Redux.
  * Again, the dispatch must come last after any Promises have been rejected or resolved.
