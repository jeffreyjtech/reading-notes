# Read 03 - Express REST API

## [Review: ES6 Classes](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes)

- Classes are templates for building objects.
- In the inner workings of JavaScript, classes are special types of functions.
- Class declarations are not hoisted, regardless of the type of declaration
- Classes, like functions, can be created and assigned to variable names via **class expressions**.
- Class body and methods:
  - Classes must have one and only one `constructor()` function which defines with parameters it can take in when instantiated and other logic that should be executed at that time.
    - The `super` keyword can be used to call the constructor of the super class
  - Classes can have static properties defined used the `static` keyword.
    - `static name = "Jeffrey"`
- `Extend`ing Classes
  - Subclasses can be created using the `extends` keyword.
    - `myAmazingClass extends myLastAmazingClass`
  
## [Using Express Routing](https://expressjs.com/en/guide/routing.html)

- Routing is how an app's endpoints respond to client requests
- Routes are defined in express using methods of the `app` object.
  - These are derived from HTTP methods. A few examples:
  - `app.get()`
  - `app.post()`
  - `app.delete()`
- Route paths define the address that must be used to hit a certain endpoint.
  - Route paths can be defined in Express using certain regex operators for flexible path definitions.
- Route parameters are named URL segments that capture values which occupy that spot in the URL chain.
  - `/myroute/:param1/:param2/:param3`
  - dots and hyphens can also be used as delimiters for additional parameters
  - `/myroute/:normalparam-dashparam.dotparam`
- The callback method provided to a route method is the **middleware** which defines the function to be executed when a request comes in on that route.
  - Multiple callbacks can be provided to a route, either as additional arguments or in an Array.
- The `express.Router` class is used to create modular mountable route handlers.
  - A `Router` instance is a complete middleware and routing system, and, for this reason, is also known as a mini-app.

## [Express Routing](https://www.digitalocean.com/community/tutorials/learn-to-use-the-new-router-in-expressjs-4)

- The Express `Router` is a mini express application.
- The `Router` has methods and usage very similar to Express's `app` object.
- As with normal express `app`s, can you define paths with parameters.
- The `.param()` method allows us to set a specific piece of middleware to run when that path+param combination is hit.
- The `.route()` method also exists on the `app` object.
  - Chaining HTTP methods onto this method is possible, and you can create a route set in very few lines of code.
