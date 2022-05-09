# Read 33 - `<Login />` and `<Auth />`

## What is role based access control?

- Role-based access control (RBAC) is an authorization scheme which restricts the actions which can be performed on a resource based on the accessor's role with an organization.
- Roles generally correlate with roles in the business sense of the word, or groups of related roles.
  - Low-level employees will have the least access to resources on the network.
  - High-level employees, such as directors or administrators, will have the most access to resources.
- RBAC gives fairly granular control over who can access what, although not as much as attribute based access control (ABAC).
- Permission should never be over-prescribed, otherwise the whole point of the system is moot.
- Different types of designations in an RBAC tool:
  - Management role scope: Limits what resources the role group is allowed to access.
  - Management role group: The ability to add and remove members to/from the role.
  - Management role: The types of tasks that can be performed by a specific group.
  - Management role assignment: Links an individual role to a role group.
- RBAC has a number of advantages over a less robust access control scheme (or no access control scheme at all).
  - Less busy work to grant employees access to resources when they are hired or change roles.
  - Improve compliance by limiting access to sensitive customer information.
  - Creates alignment between network access and employees' roles.

## React Cookies

- The [React Cookies library](https://www.npmjs.com/package/react-cookie) is a npm package which gives React developers an easy way to store and retreive cookies.
- This library provides a `<CookiesProvider />` component for allowing components to consume the cookies via the React API.
- It also provided a `useCookies` hook. This hook returns `cookies`, `setCookie`, and `removeCookie`
- It has a `withCookies` function which mutates a React component to have cookies available via state.
- The last major aspect of this package is the Cookies object, which has methods `get`, `set`, `getAll`, and `remove`.
