# Read 28 - Component Lifecycle / useEffect() Hook

## Using the Effect Hook

- The `useEffect` Hook provides a tool for creating side effects during certain points of the component lifecycle.
- To compare to React component built-in methods, `useEffect` is a combination of `componentDidMount`, `componentDidUpdate`, and `componentWillUnmount`.
- This essentially means a callback provided to `useEffect` will run every time after the component renders/re-renders.
- If your callback function returns a function, the `useEffect` hook will run that function-in-a-function as a cleanup function when a component unmounts.
- Effects are also great for enforcing single-responsibility principle onto lifecycle methods, as disparate side-effects can be added as separate hooks instead of being forced into a single `componentDidUpdate()` codeblock

This class-component gets greatly improved with `useEffect`:

```js
class FriendStatusWithCounter extends React.Component {
  constructor(props) {
    super(props);
    this.state = { count: 0, isOnline: null };
    this.handleStatusChange = this.handleStatusChange.bind(this);
  }

  componentDidMount() {
    document.title = `You clicked ${this.state.count} times`;
    ChatAPI.subscribeToFriendStatus(
      this.props.friend.id,
      this.handleStatusChange
    );
  }

  componentDidUpdate() {
    document.title = `You clicked ${this.state.count} times`;
  }

  componentWillUnmount() {
    ChatAPI.unsubscribeFromFriendStatus(
      this.props.friend.id,
      this.handleStatusChange
    );
  }

  handleStatusChange(status) {
    this.setState({
      isOnline: status.isOnline
    });
  }
```

Goes to this:

```js
function FriendStatusWithCounter(props) {
  const [count, setCount] = useState(0);
  useEffect(() => {
    document.title = `You clicked ${count} times`;
  });

  const [isOnline, setIsOnline] = useState(null);
  useEffect(() => {
    function handleStatusChange(status) {
      setIsOnline(status.isOnline);
    }

    ChatAPI.subscribeToFriendStatus(props.friend.id, handleStatusChange);
    return () => {
      ChatAPI.unsubscribeFromFriendStatus(props.friend.id, handleStatusChange);
    };
  });
  // ...
}
```

- If `useEffect` is provided a 2nd argument which matches the name of a `useState` variable, the `useEffect` callback will only execute when that state variable is manipulated.
- Effects are run on each update in order to ensure that cleanup effects are easy to create and apply consistently.
- A common source of bugs in class components is a failure to cleanup when components perform an update, which the `useEffect` hook easily solves by making it easy to handle that situation without writing extra code.

This class-based component codeblock with cleanup

```js
  componentDidMount() {
    ChatAPI.subscribeToFriendStatus(
      this.props.friend.id,
      this.handleStatusChange
    );
  }

  componentDidUpdate(prevProps) {
    // Unsubscribe from the previous friend.id
    ChatAPI.unsubscribeFromFriendStatus(
      prevProps.friend.id,
      this.handleStatusChange
    );
    // Subscribe to the next friend.id
    ChatAPI.subscribeToFriendStatus(
      this.props.friend.id,
      this.handleStatusChange
    );
  }

  componentWillUnmount() {
    ChatAPI.unsubscribeFromFriendStatus(
      this.props.friend.id,
      this.handleStatusChange
    );
  }
```

Can be written in many less lines with `useEffect()`

```js
function FriendStatus(props) {
  // ...
  useEffect(() => {
    // ...
    ChatAPI.subscribeToFriendStatus(props.friend.id, handleStatusChange);
    return () => {
      ChatAPI.unsubscribeFromFriendStatus(props.friend.id, handleStatusChange);
    };
  });
```
