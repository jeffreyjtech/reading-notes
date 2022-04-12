# Read 11 - Event Driven Applications

## Reading Material

[Event Driven Programming](https://alligator.io/nodejs/event-driven-programming/)

[Node docs: events](https://nodejs.org/api/events.html)

## Summary Notes

- Event-driven programming is a pattern for programming employed to handle asynchronous behavior in an application while avoid issues of complexity and collision.
- The event-handler-event-queue system in the web browser is the perfect example of event-driven programming
  - Nothing happens until a user interacts with the webpage or a time-based event fires
- Key concepts to event driven programming:
  - The event handler, which is a callback function defined by the developer which is invoked when an event is triggered.
  - The event loop, which continuous listens for event triggers and calls the attached handler(s) for a given event.
- Node natively provides the `EventEmitter` module/object for using event-driven programming between modules within a single application layer.
  - The `.emit()` method sends out the trigger for the event in the first argument, with the payload-to-send in the 2nd argument.
  - The `.on()` method attaches a callback function to an event.
  - The `.removeListener()` method removes a specific callback from an event.
  - The `.removeAllListeners()` method removes all callbacks from an event.
- Object-oriented programming and event-driven programming are complementary paradigms:
  - Using events allows objects to interact with each other with next-to-no coupling, they just need to share an event name and expected payload shape.
  - Objects can interact with each other, even if they're operating in completely separate scopes.
