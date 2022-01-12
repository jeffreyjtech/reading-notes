# Read 01 - Introductory HTML and JavaScript

Reading notes for Code 201, covering various chapters from *HTML & CSS: Design and Build Websites* and *JavaScript & JQuery: Interactive Front-End Web Development* by Jon Duckett. The book titles have been abbreviated as HTML and JS in the section headings of these notes.

## HTML | Introduction

- The world-wide web is accessed in the modern day with browsers, web servers, and screen readers. 
- Screen readers and web browsers can be used on many different types of devices with different display sizes, connection speeds, and computing power. Effective modern websites need be designed with multiple devices in mind.
- HTML and CSS are the fundamental languages for composing the layout and look of webpages.
- JavaScript is one the fundamental language for adding interactive elements to webpages.
- Small websites may use just HTML, CSS, and JavaScript to provide their content. Large websites likely use a content management system to feed content into HTML, CSS, and JavaScript code. Very large websites use databases and what one might call informally "server-side" programming lanugages, such as Java, PHP, ASP.net, or Ruby, to provide content.
- These technologies are constantly evolving. In the case of HTML and CSS, the versions used today are HTML5 and CSS3. These versions are iterative upon the previous versions.
- The World Wide Web uses a network of Domain Name System (DNS) servers to keep track of the host server addresses of websites which we can connect to with our computers, other servers, and other internet-capable devices.

## HTML | Chapter 1: Structure

- Webpages are like real world documents, which need structure to effectively communicate their content and/or recieve information.
- Just as a newspaper has headings to seperate articles from each other and subheadings to seperate the sections within articles, HTML pages can headings and subheadings to organize sections heirarchically.
- HTML uses elements to define sections: `<title>My Webpage!</title>`
- Elements are made of up opening `<title>` and closing `</title>` tags which enclose content `My Webpage`
- Elements can also have attributes `<p id="section1">` to further manipulate their appearance or functionality.
- Essentially every HTML page composed "by-hand" will have the following elements and use them the same way:
  - `<body>` - This contains everything shown in the browser window.
  - `<head>` - This contains data *about* the webpage. Typically this data *alone* cannot affect the appearance of what the user sees in the browser window.
  - `<title>` - This element lies in the `<head>` and defines what the browser window or browser tab itself will be titled.
- HTML pages can be created in basic text editors, and these pages can be opened by the web browser on your PC.
- You can inspect the HTML and CSS of many websites by using a web browser's built-in inspection tools or by saving an HTML webage to your PC.
- It is important to learn what elements exist and what they can do for you to structure your webpage for effective usage.

## HTML | Chapter 8: Extra Markup

- DOCTYPE
  - The DOCTYPE element is used to tell a web browser what version of HTML you are using, as HTML5 has been preceded by previous versions and offshoots of those versions.
- Comments in HTML
  - Comments in HTML are made with the following symbols `<!-- The comment is in between -->`
- ID and class attributes
  - The ID and class attributes can be applied to any tag but do nothing by themselves.
  - ID attributes give a label to an element that CSS or JavaScript can find so they can apply (for CSS) or read/write something (for JS) on that element.
- Inline and block elements
  - All layout elements in HTML are either block or inline. The difference is simple: block elements appear on the next line after the previous element (this can be changed by attributes), and inline elements appear on the same line as the previous element.
  - The `<div>` and `<span>` elements exist as the generic block (div) and inline (span) elements. Sort of like the prototypes to other layout elements with more descriptive names. Use these when you want a subcontainer for content or as special containers for uniquely style elements.
- `<iframe>`
  - This element allows a webpage to be embedded inside of another webpage.
- `<meta>`
  - The `<meta>` element contains metadata. The attributes `content` and `name` are frequently used. This data gives information to search engines for the purpose of indexing your page.

## HTML | Chapter 17: HTML5 Layout

HTML5 has improved upon previous versions of HTML by providing semantic elements which, collectively, allows developers to lay out every block of a webpage with an element whose makes sense for what that block is doing.
These elements include:

- `<aside>`
- `<header>`
- `<nav>`
- `<section>`
- `<article>`
- `<footer>`

Their use is well demonstrated by the following diagram from W3 schools on their [HTML5 Semantic elements page](https://www.w3schools.com/html/html5_semantic_elements.asp), which is itself based on the [HTML Sections spec](https://html.spec.whatwg.org/multipage/sections.html#sections) by [WHATWG](https://html.spec.whatwg.org/multipage/acknowledgements.html#ipr).

![Semantic element general layout](https://www.w3schools.com/html/img_sem_elements.gif)

Older web browsers will need additional information to style these semantic elements properly.

## HTML | Chapter 18: Process & Design

- The process of creating a website should start with these fundamental questions:
  - Who will be using your website? Who is your audience? What are the demographics of your audience? What are the differences between these groups? How do I verify my hypotheses to the previous questions?
  - Why will they use my website? Is to find reference information? Recent events? A broad subject or a narrow topic? Cat pictures?
  - How are they going to use my site? Frequently? Infrequently? From a computer or a mobile device? What information might the user want the site to keep track of from visit to visit?
- Brainstorming and drafting is the next two steps in creating a website. Here are some techniques:
  - Draft site maps! These are tree-like layouts of what pages and what types of content belong together, and how they should be connected to each other heirarchically.
  - Draft wireframes! These are a "visual draft" of how a given page on the site might look.
- Use design to get your message across
  - Visual heirarchy - Large, high contrast, elements will pop out to the user and should contain the big thing you want them to look at.
  - Grouping - Elements can be visually grouped with borders, aligned across an axis, or made into shapes, to denote that their contents are related.
  - Consistency - Keep visual elements of similar importance levels the same within pages. Pages across your whole site should probably have the same number of levels to their content heirarchy. A given heirarchical level shared by two pages should have similar content between the pages.
  - The heading/subheading heirachy of a given page needs to be carefully selected to manifest the contect heirachy you have envisioned.
- Navigation: A good navbar is almost always a good thing on a website. It should be consise, consistent, and interactive, so the user always knows where they are and can see the "categories" of your site in a quick-to-read, visually appealing layout.

## JS | Introduction

- JavaScript provides interactivity to HTML pages by giving them one or more of the following features
  - Access: The ability to access data from the user.
  - Modify: The ability to modify content on the webpage
  - Program: The ability to process its inputs and outputs.
  - React: The ability to react to the user's actions.

## JS | Chapter 1: The ABC of Programming

This chapter is centered around the "ABC" of programming. Each is an answer to 1 of 3 questions.

### A : What is a script and how do I create one?

- A script is a series of instructions. Like how to make bread, or build a car, scripts provide instructions for a page to do one of the Access-Modify-Program-React features above.
  - Designing a script
    1. Task: The process for designing a script starts with an idea of the task to be performed, in human terms. It helps to make a flowchart at this first step.
    2. Step: Then you break the task down into individual steps. A list or another flowchart are good for visualising this as well.
    3. Code: Break down your steps further and/or interpret them heuristically into what the instructions should look like in your script
  - Remember that computers are programmatic. Instructions need to be specific, granular, and use their vocabulary properly.

### B : How do computers fit in with the world around them?

- Computers model the real world with data. In JavaScript, and many other programming languages, use the following prototypes for constructing their models:
  - Objects: An object is like a real world object, it has attributes and things it can do.
    - Properties: Properties are the attributes of objects in JS.
    - Methods: Methods are the functions (a very important word for the future) that an object is able to perform.
  - Events: Events are a form of input which can force a webpage to react on-demand to something happening.
- The various components of a web browser are built-in objects with built-in methods that JavaScript can interact with.

### C : How do I write a script for a webpage?

- HTML, CSS and JavaScript build on top of each other to provide content, styling, and interactivity respectively.
- JavaScript can be written in a plain text editor, either as a seperate file `.js` or directly into an HTML file using the `<script>` element.
- Storing a script in a seperate file has the advantage of allowing your page to load with the JavaScript stripped off, whenever that might be necessary.
