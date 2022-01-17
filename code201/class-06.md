# Read: 06 - JS Object Literals; The DOM

## [Understanding the problem domain is the hardest part of programming](https://simpleprogrammer.com/understanding-the-problem-domain-is-the-hardest-part-of-programming)

In software development, problem domain is the model of a problem that you have built up through research and analysis of the problem itself. When you are working with a familiar or well-documented problem domain, coding features is easy. Coding without a defined problem domain is like building a plane while it's in the air, or trying to answer to a question that you only heard half of.

Unfortunately, programmers are often in situations where the bigger picture is not entirely apparent to them but they must perserve anyways. Narrowing your focus on a specific part of a problem is a good path forward from these situations. Another path forward is to know the right questions to ask so that you understand enough of the problem domain to get to work. When time permits, this information gathering can be invaluable, as you'll be prepared for the next steps in the project.

## [What’s the difference between primitive values and object references in JavaScript?](https://betterprogramming.pub/intermediate-javascript-whats-the-difference-between-primitive-values-and-object-references-e863d70677b)

### Data Types in JavaScript

All data types in JavaScript fall under one of two categories: Primitive values and object references

#### Primitive values

The following data types are primitive value types

- Boolean
- Null
- Undefined
- Number
- BigInt
- String
- Symbol

#### Object-based data types

The following data types are objects:

- Objects
- Arrays
- Functions
- Dates

#### Why is it important to know the difference?

The differentiation between primitives and object references is important for a few key reasons:

- Primitive data values are immutable: Using strings as an example, while the individual elements in an array can be changed, the individual characters in a string value cannot be changed without re-assigning the whole string. It's this limitation which makes primitives immutable and object references mutable.
- Object "data types" are just references: Without special keywords being used, making a copy of an object, through an assignment of one object to one you have just instatiated, will result in mirror objects which actually share the same underlying values and cannot be changed individually.
- Object references and equality operators: Objects references do not contain values directly, which results in type-strict equality operators `===` to returning false on objects which don't refer to the same underlying data. The properties of "mirror" objects will return true. A simple solution to this is that seperate objects which need their properties compared can have those properties converted into a suitable primitive data type.

## JS | Chapter 3: “Object Literals” (pp.100-105)

### Objects, Properties, and Values

Objects group together variables and functions into a model, which can then be re-used or referenced in other parts the code.

- Variables built into an object are called properties.
- Functions built into an object are called methods.

Properties are an example of a key-value pair. This is a common model across programming as a whole which, to use my own words, is the pairing between a labelled container and its contents.

There are several ways to create objects but literal notation is the easiest: the instatiation keyword (let or var) is followed by the object's name, then assigned to a set of properties and methods enclosed in curly brackets.

Dot notations is the method of accessing object properties and methods by using the object's name followed by a dot and the property/method name. `house.address` `house.isOccupied()`

## JS | Chapter 5: “Document Object Model” (pp.183-242)

### The DOM

> Document Object Model

The DOM is the model with which all major web browsers store data about a page. The DOM consists of a tree with various nodes.

DOM Nodes come in 4 types:

- The Document Node: The webpage's node.
  - The one node to rule them all. The document node is the root for any DOM.
- Element Nodes: Represent HTML elements
- Attribute Nodes: Represent HMTL attributes.
  - While HTML attributes "live" inside HTML elements, in the DOM, attribute nodes are not children of their elements' nodes.
- Text Nodes: Represent the content enclosed by HTML elements.

The DOM tree is manipulated in JavaScript by locating a node and then working with it. These steps are normally done with seperate JS statements. Best practice when querying the DOM is to store the returned location in a variable.

- `querySelector()` `getElementbyId()` are two similar methods which search an entire document and return an individual element.
- Most other methods will return a node list.
  - Live node lists
  - Static node lists
- The `item()` method is used to select an element from a node list.
- Using the node list with an index, as an array, is another way of selecting an element.
- Methods exist for finding node lists by class attributes, tag name and CSS selectors.
- Node lists can be looped through like any other kind of array.
- Nodes have parents, siblings, and children. By refering to these related elements, one can "traverse the DOM"

### Manipulating Nodes and their contents

Multiple properties in the node object can be used to manipulate its content, and even enclosed HTML.

- `innerText`
- `textContent`
- `innerHTML`

Elements can be added with the DOM. This normally involves 3 steps:

1. `createElement()`: Define the element node
2. `createTextNode()`: Define the content
3. `appendChild()`: Put it into the DOM.

Use DOM manipulation tools carefully when user-generated content is involved. Don't let malicious code get worked into your site!

### Attribute nodes

- `.hasAttribute()`: This method returns true/false if an element node has an attribute with the passed-in name:
- `.className()` and `.setAttribute()` are used to set class names and attributes respectively.
- `.removeAttribute()` removes an attribute.
