# Read 02 - Express

## [An introduction to NodeJS and Express](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Express_Nodejs/Introduction)

### What is Node?

- Node is a cross-platform runtime environment for JavaScript based on the Chrome V8 engine. It's main use case is running JavaScript outside of a web browser.
- It uses "plain old JavaScript"
- Node provides Node Package Manager, otherwise known as `npm`, which is an incredible tool for installing hundred of thousands of packages written by other developers.

### What is Express?

- Express is a web framework for handling requests sent to a Node-based API, server, or application.
- It allows writing handlers for different HTTP verbs at different routes
- Set common web application settings like port assignments and response templates
- You can add just create just about any sequence of middleware for processing requests.

## [What is NPM?](https://docs.npmjs.com/getting-started/what-is-npm)

### About npm

- npm is, as per the doc linked above, the world's largest software registry, used for sharing software packages.
  - It consists of a website, a command-line interface, and a registry.
    - The website is for finding packages made by other developers, and for sharing/managing your own uploaded packages.
    - The command line interface is for interacting with npm as it exists in your local development environment.
    - The registry is a public database of packages.

### NPM features and usage

- Running packages without downloading with npx
- Creating organizations for package management, maintenance, collaborative development
- Update dependencies automatically
- Use another developers solution to a problem when necessary.
- Download tools for your project which will work out-of-the-box
- Creating and then sharing your own tools to the registry

## [What is TDD?](https://www.agilealliance.org/glossary/tdd/)

TDD stands for **Test-Driven Development**. It's a strategy for software development where testing, coding, and design are performed in lockstep with each other rather than as separate project outcomes.

A TDD-based workflow consists of the following steps:

1. Write a unit test for a feature which doesn't exist yet
2. Run the test (which should fail because there is no code to be tested)
3. Write "just enough" code to satisfy the test's requirements.
4. Refactor the code for performance, simplicity, or whatever code-related non-functional outcomes your team/project requires.
5. Repeat for each feature.

According to the article, TDD improves code quality by decreasing bugs on when features are implemented and improving the robustness and design adherence of code. In other words, code written in a TDD process is less likely to require refactoring later in the project.

Common mistakes to avoid when using TDD is a lack of frequent testing, writing tests in batches, writing tests that are too large or too small/insignificant. Furthermore, TDD requires whole-team alignment which creates it own issues, typically due to a lack of maintenance.

## [CI/CD](https://www.youtube.com/watch?v=xSv_m3KhUO8)

Continuous Integration (CI):

- A strategy for ensuring that every developer on a team can integrate their changes, catching bugs and reducing merge conflicts in the process.
- Commonly, CI uses automated testing to verify that a new build works before integration to the primary dev branch.

Continuous Delivery aka Continuous Deployment (CD):

- Continuous delivery means that code can be deployed at any time, because the continuous integration process has automatically verified that a new feature branch works.
- Several deployment tools work can with GitHub to check that CI tests have completed and then automatically deploy a verified build.
