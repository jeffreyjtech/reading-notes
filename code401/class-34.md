# Read 34 - API Integration

## Review, Research, and Discussion

1. Bearer tokens are issued by an authentication server or by the auth features of an API. They contain encoded information which verify the identity of the bearer.
1. Express middleware are the functions which process requests and define the response to a request in an Express API. They can be fully modularized, chained to one another, and attached to mini-apps which can then be attached to the top-level Express app. Error-handling middleware can also be defined for an Express API, allowing custom responses to bad requests and other failures.
1. A JWT is a open-standard encoded **J**SON **w**eb **t**oken. A JWT contains JSON objects, a subset of which are claims. Claims are cryptographically secured so as to prevent tampering or forgery.

## Vocabulary Terms

- Role-based access control: Role-based access control is an authorization scheme for controlling access to resources in a network. Each client is given a role which defines what resources they can access and what they can do with said resource. For example a "reader" role for an API would only grant authorization for GET requests to front-facing resources.
- HTTP cookie: An HTTP cookie is a piece of data which is sent to a client's browser and stores some data which is sent back to the server upon its request. HTTP cookies are used for session management, user personalization, and tracking. [source](https://www.educative.io/blog/http-cookies)

## Preview

**Which 3 things had you heard about previously and now have better clarity on?**

1. Cookies: I had heard of cookies before, tons of times in fact, but I didn't know how they factored into serving web content until now.
1. Express middleware: Each time I read about Express middleware, learn that it's used for more and more things in Express's framework.
1. Tokens: It does not hurt to learn more about tokens and JWT. They're very important to making functional authorization/authentication systems, which are critical to public-facing websites that store any amount of user data and any API which needs to track accessors.

**Which 3 things are you hoping to learn more about in the upcoming lecture/demo?**

1. Cookies: I want to learn when it's most appropriate to use cookies.
1. Role-based access control: I want to see more design patterns for implementing RBAC.
1. JWT: How much data about the bearer should really be encoded in a JWT?

**What are you most excited about trying to implement or see how it works?**

Definitely additional design patterns for RBAC and ACL authorization implementations.
