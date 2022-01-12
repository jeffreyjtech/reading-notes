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

## JS | Chapter 4: “Decisions and Loops” (pp.145-162)
