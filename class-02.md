# Read 02 - Basics of HTML, CSS & JS

>Reading notes for Code 201, covering various chapters from *HTML & CSS: Design and Build Websites* and *JavaScript & JQuery: Interactive Front-End Web Development* by Jon Duckett. The book titles have been abbreviated as HTML and JS in the subheadings of these notes.

## HTML | Chapter 2: "Text" (pp.40-61)

Webpages can be enhanced with structural markup and semantic markup. Markup is the collective term for elements that modify the appearance of text.

### Structural Markup

The following tags are examples of structural markup:

- Headings: `<h1>` through `<h6>`
- Paragraph: `<p>`
- Italics, Bold, Subscript, and Superscript: `<i>`, `<b>`, `<sub>`, `<sup>`

### Semantic Markup

The following tags are examples of semantic markup

- Definition: `<dfn>`
- Emphasis: `<em>`
- Abbreviation: `<abbr>`
- Citation: `<cite>`
- Deletion and Insertion: `<del>` & `<ins>`

## HTML | Chapter 10: "Introducing CSS" (pp.226-245)

> Cascading Style Sheet

CSS is the language by which you define rules to change the appearance and layout of the "boxes" that compose an HTML file. CSS can be inserted with the `<style>` element, inline as an attribute inside of an element, or linked in from a .css file. The simplest CSS rule has a selector, a property, and a value assigned to that property:

```css
p{
  color: green;
  /* this will change the text color of any <p> element green*/
}
```

There are several different types of selectors depending on how they discriminate between elements. Certain CSS properties are inherited automatically from a parent element to child elements. To explain what "child" and "parent" mean, elements within an element are it's children and that container element is the parent. The "Cascading" in *Cascading Style Sheet* refers to how multiple CSS files, the `<style>` element, and inline CSS can all apply to a single HTML file to impart properties in a cascading and deterministic manner. In other words CSS has an "order of operations" for finding the final properties for an element.

## JS | Chapter 2: “Basic JavaScript Instructions” (pp.53-84)

JavaScript consists of statements `let name = 'string';`. A statement is a single line of code. Ending each line with a semicolon `;` helps with readability. Curly braces `{}` and the code within are called codeblocks.

Comments come in inline `// comment` and block `/* comment */` variants and are very useful for explaning a piece of code. This can be a reminder to yourself or an explanation to someone else reading your code.

Variables are used to store data in JavaScript. Variables have to be created with either the `var` or `let` keyword, followed by the variable name. Then data has to be assigned with an assignment operator `=`. Data in JavaScript has the following types: `string` for storing text, `number` for storing numbers, and `bool` for storing boolean values (true or false).

Arrays are a special type of variable. Arrays are lists of variables which (hopefully) belong together as a group. Arrays are created with code which might look like this:

```javascript
let foods;
foods = ['pizza','sushi','fried potatoes','dog kibble'];

console.log(foods[1])
```

The code above creates an array of strings with 4 items. The way to use a given item is to write the array's name followed immediately by a number in square brackets `foods[1]`. Each item in an array has an index, which where it lies in the list's sequence. ***Indexes start at zero.*** `foods[1]` will interpret into whatever lies in index 1, which is the string `'sushi'`.

### Expresions and operators

Operators are the symbols which inform JavaScript that you want it to manipulate two values in some fundamental way. Adding two numbers requires using the addition `+` operator. Subratction has `-`, division has `/` and so on.

Operators belong to categores such as arithmetic operators, assignment operators, comparitive operators, and more.

Expressions are a sequences of values and operators which evaluate into a single value. Expressions are a fundamental concept in almost any programming language as, by adding 1 plus 1 to make 2, you've just made an expression.

## JS | Chapter 4: “Decisions and Loops” (pp.145-162)

Decisions in a JS script can be made with the following tools:

- Comparative operators: Comparitive operators compare the values of two variables and return true if the comparison stipulated by the operator is true.
  - `'black' === 'black'` would evaluate to true.
  - `5 > 6` would evaluate to false.
- Logical Operators: These operators, such as logical AND `&&` and logical OR `||` and logical NOT `!`, perform a logic test on one or two boolean values to result in a boolean result. Boolean operators have truth tables which define how their input(s) relate to their output.
- Conditions and condition statements: These operators come together to make condition statements, used by statements like `if` and `switch` to make decisions on whether a codeblock of our choice will be run or skipped.
- If statements: If statements check a condition enclosed in parenthesesk, and if it's true the codeblock in curly brackets is executed
 `if (isTrue){console.log('true');}`
- If...else statements: `if...else` statements add on a fallback code block which is executed if the `if`'s conditional statement is false.
 `if (isTrue){console.log('The if's conditon was true');} else {console.log('Else the if's condition must be false')}`
