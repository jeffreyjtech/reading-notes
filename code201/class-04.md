# Read 04 - HTML Links, JS Functions, and Intro to CSS Layout

>Reading notes for Code 201, covering various chapters from *HTML & CSS: Design and Build Websites* and *JavaScript & JQuery: Interactive Front-End Web Development* by Jon Duckett. The book titles have been abbreviated as HTML and JS in the subheadings of these notes.

## HTML | Chapter 4: Ch.4 “Links” (pp.74-93)

- Anchor element `<a href="https://google.com>Google link</a>`
  - The anchor element is the element used to turn text into hyperlinks. The `href` property determines the address (aka the URL) the hyperlink leads to.
- URLs (*Uniform Resource Locator*) are the semantic addresses of resources on the internet and ethernet directory.
  - Absolute: An absolute URL starts with HTTP or HTTPS and requires a full path from domain to file or page.
  - Relative: A relative URL starts at the current directory of the HTML file and will find any files in the same folder. Various shortcuts can be written into relative URLs to point to parent and child directories.
- Misc URL properties
  - `mailto`: The mailto attribute causes the hyperlink to open an email blank email in the user's email client of choice. The address provided by the link will populate the `to` field.
  - `target`: The target atrribute specifies which part of the target document to open.
- Linking to elements on a page: using `#` followed by a valid `id`, a hyperlink can jump to the ID'd element on the same webpage.

## HTML | Chapter 15: “Layout” (pp.358-404)

<!--this chapter is a whopper-->

### Positioning elements

- CSS's default positioning scheme
  - Normal flow: Block elements are layed out top-to-bottom and inline elements are layed out left-to-right along lines.
- The `position` attribute: The position attribute, which is `static` by default on all elements, can be set to `relative`, `absolute`, or `fixed` to change how an element fits into the normal flow of a document.
  - `relative` positioning: This positioning allows block elements to be placed relative to where it would be placed in normal flow. This must be combined with a length value assigned to a `top`, `bottom`, `left`, or `right` property to actually move the element.
  - `absolute` positioning: This positioning removes an element completely from normal flow. Other elements will ignore it and it will occupy a permanent position on the HTML document.
  - `fixed` positioning: This has almost the same effect as `absolute`, except the element will occupy a permanent position on the *browser window*.
- The `z-index`: The z-index value is how one sets a sort of "bring-to-front" or "move-to-back" rendering behavior. Elements with a given z-index occlude elements with lower z-index and are occluded by elements with higher z-indexes
- The `float` atrribute: The float atrribute allows elements to have other elements to brush up against them.
  - The `clear` atrribute: the clear attribute, with a value of `left`, `right`, `top` or `bottom`, combines with the float attribute to prevent elements from being adjacent to the given side.
  - `float` and parent elements: Floated elements do not increase the size of parent elements, which must be worked around with CSS or additional HTML elements.

### Display and page sizes

- Display and page sizes
- Fixed width vs liquid layouts
- 960px grid system

### Using multiple CSS files

- Importing `.css` files

## JS | Chapter 3 (first part): “Functions, Methods, and Objects” (pp.86-99 ONLY)

### Functions

- Declaration
- Invocation
- Paremeters and arguments
- Anonymouse functions
- Immediately Invoked Function Expression (IIFE)

### Variable Scope

- Global vs Local variables

## Article: “6 Reasons for Pair Programming”

1. Greater Efficiency
2. Engaged Collaboration
3. Learning from fellow students
4. Social skills
5. Job interview readiness
6. Work enviroment readiness
