# Read 03 - HTML Lists, Control Flow with JS, and the CSS Box Model

>Reading notes for Code 201, covering various chapters from *HTML & CSS: Design and Build Websites* and *JavaScript & JQuery: Interactive Front-End Web Development* by Jon Duckett. The book titles have been abbreviated as HTML and JS in the subheadings of these notes.

## HTML | Chapter 3: “Lists” (pp.62-73)

HTML has elements for inserting lists of different types into HTML documents:

- Unordered lists `<ul>`: Unordered lists will lay out the list items `<li>`, one per line, with a bullet point on the left.
- Ordered lists `<ol>`: Ordered list will lay out the list items `<li>`, one per line, with an automatic sequential number starting at 1 on the left.
- Definition list `<dl>`: Definition lists will list terms `<dt>`, each followed by a definition `<dd>`.
- Nested lists `<ul> <ul>` `<ol> <ol>`: Lists can be nested within each other. The inner list will be indented and may have a different bullet or numbering style.

## HTML | Chapter 13: “Boxes” (pp.300-329)

CSS can interact with the "boxes" laid out by HTML to change their size. Different size properties exist with different effects:

- Dimensions: HTML boxes can have their `height` and `width` properties set forcibly with CSS. Percentages, pixels, and other units can be used.
- Limiting width: `min-width` and `max-width` allow a box to shrink or expand with the window *up to* their given values.
- Limiting height: `min-height` and `max-height` perform the same function as the width limiters except for height.
- Overflow: If a box's text cannot fit due to limited height, it will extend past the bottomn of the element, possibly over other elements. The `overflow` property can be set to `hidden` or `scroll` to hide distended content or make it visible by a scroll-bar
- Inline/block display: The `display` property can be assigned a value to force an element into block, inline, or inline-block "mode".
  - `display` can be set to none to hide the element AND remove it from element flow.
  - setting inline elements to block display can have unintended consequences.
- Hiding boxes: the `visibility` property can be set to hidden to hide the element *without* removing it from element flow. A white box can take it's place. `visibility` can be set to visible as well, returning the element to normal.

### Padding and margin

Padding and margin properties are used to add whitespace inside of and outside of a box, respectively. Every box can also have a border of varying thickness. This border is primarily for visual separation of items using lines/dots/color, but it's thickness is added onto the box's total size'

Centering a box can be done with left-margin and right-margin auto.

### CSS3

CSS3 provides new features (new in 2011) for boxes and borders:

- Border images: Images can be used as borders.
- Box shadows: Drop shadows can be added around the edges of boxes.
- Rounded corners: Border corners can be rounded.
- Elliptical shapes: Border corners can be given elliptical, asymetric shapes.

## JS | Review from Reading 02 - Chapter 2: “Basic JavaScript Instructions” (pp.70-73)

### Arrays

- Creating an array: Arrays are commonly created in one of two ways
  - Assignment: Instantiating the array with it's named with an assignment of a set of values in [] separated by commas
    - `let myArr = [1,2,3];`
  - Array constructor:  The built in Array() function will accept a set of arguments and return an array with the given arguments.
    - `let myArr = new Array(1,2,3);`
- Index: Each value in an array occupies a slot, an address of sorts. That address is the value's index.
- Accessing / changing array values: Changing values in an array means assigning a value to an array's index `myArr[9] = 11`. Accessing an array is done similarly `product = factor * myArr[3]`

## JS | Chapter 4: “Decisions and Loops” from switch statements on (pp.162-182)

### Typing in JS

- Type coercion: JavaScript will try to convert strings into numbers when evaluating comparisons, and numbers into strings when it wants a string, and numbers and strings into bool when it wants bool.
- Weak typing: JavaScript will be able to evaluate most values and expressions into true or false, because value types can be changed as needed. This is based on their truthiness and falsyness.
- Truthy and Falsy: All values have truthy and falsy-ness to enable the above behavior.

The following values are falsy:

- bool false
- the number 0
- empty strings
- empty variables
- NaN

All other values, objects, any and all arrays, you name it, are truthy.

### `switch` statement

```javascript
switch (steak){

  case 'rare': 
    //some code
    break;

  case 'medium-rare':
    //some code
    break;

  default:
    //default code
    break;
}
```

The switch statement takes a switch value and checks it if equals any of the cases in the following codeblock. The matching case's code is executed. If none match, the default case is executed. Each case including default must end with a `break` statement.

### Loops

A small collection of keywords in JavaScript allow a codeblock to be run repeatedly when given a true condition statement. These are known as loops. The specific syntax that makes up a functioning loop statement depends on the keyword being used: Two of which are `for` and `while`.

#### Loop-related keywords and concepts

- `break`: The keyword `break` will "pop" execution flow out of a loop codeblock immediately. Any remaining code inside of the codeblock will be skipped. Code execution will move to the next statement after the closing bracket of the loop's codeblock.
- `continue`: `continue` works similarly to `break`, except `continue` skips the remaining codeblock *without* breaking out of the loop. The loop may continue if the it's condition remains true.
- A loop which is used incorrectly will run forever. Hence the term, infinite loop. A page with an infinite loop may stop responding, crash the user's web browser, or take an unacceptable time to load if it loads at all. Try not to do this!

### `for` loops

```javascript
for (let i = 0; i < 10; i++){
  console.log(i);
}
```

The for loop requires 3 statements in parentheses (), separated by semicolons, and a codeblock enclosed in curly brackets {}. An initialization statement `let i = 0`, a condition `i < 10`, and a final expression `i++`. The example for loop will print out 0 through 9 in the console.

#### `for` loop execution flow

1. First, the initialization statement is evaluated
2. Second, the condition is evaluated to be true or false
3. Third, *IF* the conditon is true, the codeblock is executed.
4. Fourth, the final expression is evaluated.
5. The remaining loops will run through steps 2 through 4 until the condition becomes false.
    - Conditional logic in the for loop may also direct to a `break` statement to break out of the for loop.

### `while` loops

```javascript
let cookies = 10;
while (cookies > 0){
  console.log('I ate a cookie');
  cookie--;
}
```

While loops require less setup than for loops. A while loop starts as long as the condition is true. It will continue to loop until the condition becomes false or a `break` statement is encountered.

`do...while`: Do while is a variant of the while loop which will always run it's codeblock once, and then start loop if the condition is true.

- This one liner is should be valid do...while loop `let i = 3; do{i--;} while (i > 0);`
