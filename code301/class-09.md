# Read 09 - Functional Programming

## [Functional Programming Concepts](https://medium.com/the-renaissance-developer/concepts-of-functional-programming-in-javascript-6bc84220d2aa)

1. What is functional programming?
    - Functional programming is an programming paradigm where all computation is modelled as a mathematical function. The state of an execution sequence should only effect and be affected within the function that is being performed.

    ***

2. What is a pure function and how do we know if something is a pure function?
    - A pure function returns the same result if given the same argument(s) (AKA functions are deterministic) and they cause no observable side effects. A pure function will never use a mutable global variable to perform an operation, cannot read the contents of a file (file contents can change), and do not generate or otherwise use random numbers.

    ***

3. What are the benefits of a pure function?
    - Pure functions are easier to test and easier to predict. They can be an effective tool for managing complexity as their usage minimizes the possible number of states that the program can be in at a given moment.

    ***

4. What is immutability?
    - Immutability is the quality of data or logic which cannot be changed after it has been created.

    ***

5. What is Referential transparency?
    - Referential transparency is the quality of a function which returns the same result for the same input.

    ***

## [Node JS Tutorial for Beginners](https://www.youtube.com/watch?v=xHLd36QoS4k)

1. What is a module?
    - A module is a group of code which has a specific, aligned purpose in the application. In practice, a module takes the shape of a plain ol' JavaScript file.

    ***

2. What does the word ‘require’ do?
    - `require`, functioning similar to `import`, is a function which makes JavaScript from another file available in the current execution sequence.

    ***

3. How do we bring another module into the file the we are working in?
    - The `require` function is called with the working module's path as the argument and assigned to a variable. For example, `const timerThingy = require('./myTimer');`.

    ***

4. What do we have to do to make a module available?
    - Modules need a statement with the `module.exports` property assigned to make anything available from the module. An example would be `module.exports = myTimer`.

    ***

## Things I want to know more about

How is functional programming applied in web development? And is function programming applicable to the construction of dynamic websites which rely on user data? Would that architecture, by its nature, prevent the use of pure function for many operations?
