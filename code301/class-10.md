# Read 10 - In memory storage

## Understanding the JavaScript Call Stack

1. What is a ‘call’?
    - A call is another term for invoking a function
2. How many ‘calls’ can happen at once?
    - Technically, only one call can happen at once. This does mean calls cannot be chained together.
3. What does LIFO mean?
    - Last In, First Out
4. Draw an example of a call stack and the functions that would need to be invoked to generate that call stack.
    - 
5. What causes a Stack Overflow?
    - A recursive function with no exit point will cause a stack overflow.

## JavaScript error messages

1. What is a ‘reference error’?
    - An error caused by using a nonexistent reference, such as referring to a variable which does not exist.
2. What is a ‘syntax error’?
    - An error caused by an invalid token being inserted somewhere into JavaScript, which a JavaScript runtime cannot execute.
3. What is a ‘range error’?
    - A range error occurs when a built-in property is assigned an invalid value, such as an array's length property being assigned -1.
4. What is a ‘type error’?
    - When an statement encounters an incompatible data type, such as a property being chained onto a primitive.
5. What is a breakpoint?
    - A breakpoint is point designated during debugging to be a "freeze frame" for code execution.
6. What does the word ‘debugger’ do in your code?
    - Debugger is way of putting a breakpoint into code.
