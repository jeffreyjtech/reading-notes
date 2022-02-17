# Read 04 - React and Forms

## [React Docs - Forms](https://reactjs.org/docs/forms.html)

1. What is a ‘Controlled Component’?
    - It is a component which uses state data at all times to control its rendering behavior. Otherwise, a component would have to use two separate sets of logic, one for the initial render and another for updates initiated by user interaction.
2. Should we wait to store the users responses from the form into state when they submit the form OR should we update the state with their responses as soon as they enter them? Why.
    - It depends. Waiting to store the response limits UI responsiveness but reduces the amount of rendering needed when a user is interacting with something. Instantly storing the response can enable a greater degree of UI responsiveness. The desired amount of responsiveness and rendering work are both dependent on how someone wants to implement a feature.
3. How do we target what the user is entering if we have an event handler on an input field?
    - As long as our event handler has an `event` parameter, `event.target.value` will evaluate to the current contents of the input field.

## [The Conditional (Ternary) Operator Explained](https://codeburst.io/javascript-the-conditional-ternary-operator-explained-cac7218beeff)

1. Why would we use a ternary operator?
    - Ternary operators allow simple if/else conditional logic to be written in a shorter form. It's less code which accomplishes the same thing in one line which would otherwise take up 5, and that's less stuff to write.
2. Rewrite the following statement using a ternary statement:

```javascript
if(x===y){
  console.log(true);
} else {
  console.log(false);
}
```

- `(x===y) ? console.log(true) : console.log(false);`
