# Read 07 - HTML Tables; JS Constructor Functions

>Reading notes for Code 201, covering various chapters from *HTML & CSS: Design and Build Websites* and *JavaScript & JQuery: Interactive Front-End Web Development* by Jon Duckett. The book titles have been abbreviated as HTML and JS in the subheadings of these notes.

## [Domain Modeling](https://github.com/codefellows/domain_modeling#domain-modeling)

Domain modeling is the process of creating a conceptual model for a specific problem. In other words, it means to model your problem domain. Domain models are used in software development to VVQ the understanding of a problem between stakeholders. A good domain model makes it easy for a software development team and other teams/organizations to stay on the same page about what's being built.

Elements of a good OOP domain model:

- A constructor to create multiple objects to do the thing.
- A layout of properties with keys and values
- A method for each job we want the object(s) to do.
  - These should be as specific as possible, doing one job well.
- A scheme for storing the objects as variables.

## HTML | Chapter 6: “Tables” (pp.126-145)

- Four key elements of creating tables:
  1. `<table>`: The parent element for all other table-related elements
  2. `<tr>`: The parent element for cell `<td>` and heading-cell `<th>` elements.
  3. `<td>`: The element which contains content for a single cell.
  4. `<th>`: The element which contains content for a heading-cell, such as column or row labels.
- Table rows `<tr>` aren't always the direct children of the table `<table>`
  - `<thead>`, `<tbody>`, `<tfoot>` can be used to group rows for large tables and screen reader meta-data.
- Cells can span multiple columns or rows with `colspan` and `rowspan` attributes.
- Old HTML may use outdated inline styling and attributes. CSS can and should be used to style tables instead.

## JS | Chapter 3: “Functions, Methods, and Objects” (pp.106-144)

- Creating objects with constructor notation
  - Single object instantiation
  - Multiple object instantiation using constructor function
- Modifying objects
  - Dot `.` notation
  - Square bracket `[]` notation
- `this`
- Arrays and Objects
  - Arrays are objects
  - Arrays can store objects
- Built-in objects
  - Browser
  - DOM
  - JavaScript
- Primitives in JavaScript
- Math object and its methods
- Date object
