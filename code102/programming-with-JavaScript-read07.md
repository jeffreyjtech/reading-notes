# Read 07 - Programming with JavaScript

## Control Flow

The control flow is the order in which statements executed in a script. Code is run in order of the first line to the last line. Many structures, such as functions, `if...else`, `while`, and `for` change control flow. In order to follow the sequence of events that occur as a script is executed, one must carefully consider the changes in control flow created by code structures.

## Functions

- Any operation we tell our JavaScript to do, which is even a little complicated and is something we want to repeat, will probably be best written as a function.
- Functions can be "called" in multiple locations throughout our JavaScript to repeat the operations we've written them with, and potentially return a resulting value.
- Our code can perform complicated operations multiple times without us, the programmers, writing that operation out every time.
  - Fun fact: you can invoke JS functions in the browser console; the console will prompt you to enter arguments and log the return value.

### JS function signature

```js
// "function" keyword, followed by it's name, followed by parantheses (arguments), then curly brackets {operations}

function myIncrementFunction(number) {
  // the function's operations
  number++
  return number
}
```

This structure, aka the JavaScript function signature, *declares* a function so that it can be *invoked* (aka called) later in the code.

- A function invoke might look like `myIncrementFunction(valueIwantincremented)`.
- This particular function also includes a `return` value. 
- The pair of parentheses `()`, with or without an argument enclosed, is the critical indicator to JavaScript that you are invoking a function, not just referencing to is as an object.

### Parameters and Arguments

- *Arguments* are the values passed into the function when it is invoked, enclosed in the invocation's parentheses.
- *Parameters* are the variables we define in the parentheses in our function declaration.
- Parameters give functions a "bucket" in which to recieve arguments.
- Functions can recieve any data type as an argument, including functions (aka a callback)
- Because JS is loosely-typed, type-checking the arguments given by a function call must be done manually with operators like `typeof` or `===` inside the function.

### Return

```js
return 'someReturnString'
```

- The `return` keyword breaks out of the function, and it brings you back to where you called the function.
- If a value (string, number, variable) immediately follows the `return` keyword, that is the "return value".

### Local Variables

When needed, variables can be instantiated inside of a function to prevent access in other parts of your code.

## Expressions

- A line of code or JS operation that evaluates to a value. Expressions are made up of operators and operands (the values to be operated upon). 

### Valid Operands

- Any value that can be interpreted by JavaScript can be used as an operand.
- Variables can be used as operands
- Function calls can be used as operands
- Object properties can be used as operands
- etc.

```js
additionresult = 1 + 2 + myadditionfunction()
```

### Operators

A symbol which performs an operation on one or two values.

- `<` - less than
- `>` - greater than
- `+` - add
- `-` - subtract
- `*` - multiply
- `/` - divide
- `&&` - logical AND
- `||` - logical OR
- `!` - logical NOT
- `!=` does not equal
- `==` is equal
- `===` is equal and same type
- `!==` is equal or not equal type
- *[and more](https://www.w3schools.com/js/js_operators.asp)*
- JavaScript expressions *generally* follow this order of operations (refer to the [complete MDN list](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Operator_Precedence)):
  1. **P**arentheses
  2. Functions 
  3. NOT
  4. **EMDAS**
  5. Comparative
  6. Logical
  7. Assignment

> **Use parentheses liberally in complex expressions.**

All JavaScript operators belong to one of following types:

- Arithmetic `-`
- Assignment `=`
- String `+` (`+` concatenates values into a string if *any* of the values are strings)
- Comparison `==`
- Logical `&&`
- Type `typeof`
- Bitwise `&`