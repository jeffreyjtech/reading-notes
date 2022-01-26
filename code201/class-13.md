# Read 13 - Local Storage

## [The Past, Present, and Future of Local Storage for Web Applications](http://diveinto.html5doctor.com/storage.html)

### Pre-HTML5

- `userData`: Internet explorer had the ability, with DHTML behavior called `userData`, to allow a web page to store 64KB of data per domain in XML format.
- "Flash cookies": Adobe's Flash 6 gained the ability to store 100KB per domain in the user's browser.
- Google's Gears plugin: Google created an open-source browser plugin which generally added more features to browsers. One was storing data in embedded SQL databases, with no "hard-coded" space limit.

### HTML5's Web Storage

- HTML5 introduced a specification called Web Storage. Web Storage allows a webpage to store key/value pairs within the web browser
- `localStorage`: This object is attached to the global `window` object and it's your access point for browser storage.
  - `.setItem()`: this method adds a key/value pair to the user's web storage. Or, overwrites an existing value with a new key.
  - `.getItem()`: this method gets a key/value pair with the value AS A STRING
    - Make sure you `.parseInt()` or `.parseFloat()` numeric returns
  - `.clear()`: deletes all key/value pairs
  - AGAIN: Values are **always** stored as strings
- Tracking changes: the `"storage"` event gets fired every time a storage method is called and and results in a value change.
  - The `"storage"` event is not cancelable. I'm not sure what that means
- `StorageEvent` object: This object will exist in storage events as a snapshot of the event which just occurred.
  - `.key`: The key that was modified
  - `.oldValue`: The overwritten value, `null` if a new item was added.
  - `.newValue`: The new value, `null` if a value was removed.
  - `.url`/`.uri`: The URL of the page which called the method
- Storage limitations: There is a limit of 5MB for each *origin*.
  - An origin is defined in [HTML documentation](https://html.spec.whatwg.org/multipage/origin.html#origin-0) to sort of mean a domain.
  - The article implies there's a want for this limit to be improved but the direction of these improvements is TBD

### Using Web Storage

- Create separate functions/events to handle the cases where the user has data stored from a past visit
- Remember that storage values are always strings which must be coerced into the appropriate type.
