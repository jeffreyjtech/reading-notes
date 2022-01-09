# Read 08 - Operators and Loops

## Operators

- A symbol which performs an operation on one, two, or, rarely, three values.
- The values used by operators are known as *operands*.
- Operators can be categorized as unary, binary, and ternary operators, respectively, depending on the number of operands needed.

### Assignment Operators

Here is a list of assignment operators and their function

- Assignment; `x = value`; Assigns the operand on the to the right-side variable
- Addition assignment; `x += value`; Adds the left-side value to the right-side variable, then assigns the result to the variable
- Subtraction assignment; `x -= value`; Subtracts the left-side value from the right-side variable, then assigns the result to the variable

Assignment operators exist which combine arithmetic, bitwise, and logical operations with assignment in the pattern of addition assignment and subtraction assignment. This includes multiplication, division, remainder, exponentiation, left-shift, right-shift, bitwise AND/XOR/OR, logical AND/OR, and logical nullish.

### Comparison Operators

Comparison operators return a logical value (true or false) based on the comparison they specify. JavaScript will attempt to convert differently typed operands into an appropriate type for the comparison. This does not apply to `===` or `!==`.

- `<` - less than
- `<=` - less than or equal to
- `>` - greater than
- `>=` - greater than or equal to
- `!=` does not equal
- `==` is equal
- `===` is equal and same type
- `!==` is equal or not equal type

### Types of Operators

All JavaScript operators belong to one of following types:

- Arithmetic `-`
- Assignment `=`
- String `+` (`+` concatenates values into a string if *any* of the values are strings)
- Comparison `==`
- Logical `&&`
- Type `typeof`
- Bitwise `&`

## Programming with loops

Loops allow a piece of code to be execeuted repeatedly with rules. There are multiple types of loops. JavaScript provides the following keywords for creating and controlling loops.

- `for`
- `do`...`while`
- `while`
- `labeled`
- `break`
- `continue`
- `for`...`in`
- `for`...`of`

## `for` Loops

The `for` loop exectutes a piece of code every time a condition expression is met, and then executes an increment expression before checking the condition expression again.

```js
for (let counter=0; counter <= 5; counter++) {
    console.log(counter)
}
```

### Breakdown of a `for` loop

`statement`: This is the code that executes on each loop if  the conditionExpression is true.

```js
console.log(counter)
```

`initialExpression`: This expression initializes and sets the initial value of the counter variable.

```js
let counter=0
```

`conditionExpression`: This expression, if false, will **stop** the `for` loop 

- This is checked *before* the statement or incrementExpression has been executed.

```js
counter <= 5
```

`incrementExpression`: This expression will be executed each time the `for` loop is executed

- This is *after* the incrementExpression has been checked for true/false **and** the statement has been executed.

```js
counter++
```

### Applying `for` loops

The `for` loop can be used in a variety of ways but one of the most popular is running through a list or table (aka an array) of data and processing each entry in some way. This can be displaying all the items in an online storefront or finding the mode of a dataset.

## `while` Loops

The `while` loop executes a block of code while the condition expression is met: It always checks the condition expression before executing the enclosed instructions.

```js
while (conditionvar) {
    console.log('I will never stop running')
}
```

### Breakdown of a `while` loop

`statement`: Works just like a for loop statement

```js
console.log('I will never stop running')
```

`condition`: If this is true, the statement is executed.

```js
conditionvar
```

### Applying `while` loops

Like other loops the `while` loop has multiple use cases but most often it's used to make continuous checks on user input while a page is open, allowing the webpage to react dynamically when the user interacts with it. It can also be used to prevent something from happening until the user interacts with the webpage in a specific way (password check).
