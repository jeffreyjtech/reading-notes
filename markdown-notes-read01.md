# Markdown reading notes

## What is Markdown?

Markdown is an easy-to-use, portable markup language for creating formatted and readable documents.
Markdown alone supports the following features, as found on [Markdown's Basic Syntax](https://www.markdownguide.org/basic-syntax/):

- Headings (6 levels)
- Paragraphs
- Bold and italics
- Blockquotes
- Inline code
- Codeblocks
- Ordered and unordered lists
- Embedded images
- Hyperlinks
- Footnotes

[Markdown on GitHub](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax) has *yet more* features including but not limited to:

- Relative links
- Emojis :+1:
- Mentioning people and teams
- Referencing issues and pull requests
- Task lists

## What can you do with Markdown?

With the above features, you can write well-organized documents using simple markdown symbols. Markdown supports the most important elements of a basic HTML page or a document created with a typical word processor. With GitHub's excellent support for Markdown documents, they can be immediately published without writing any HTML.

## Breakdown of a Markdown document

This set of notes is itself a markdown document, viewable as a [raw document](./markdown-notes-read01.md). The above list about "Markdown on GitHub" looks like this:

    [Markdown on GitHub](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax) has *yet more* features including but not limited to:

    - Relative links
    - Emojis :+1:
    - Mentioning people and teams
    - Referencing issues and pull requests
    - Task lists

It contains 5 Markdown features:

1. First is a paragraph, which is a line of text that has no formatting symbols before it.
2. Second, there's a hyperlink. Hyperlinks are created by combining a link name in square brackets with a URL in parentheses.
    - `[Google](https://www.google.com)` becomes [Google](https://www.google.com)
3. The third markdown element is italicized text. Italics are created by enclosing text with asterisks
    - `*text*` becomes *text*
4. Then comes the unordered list. Unordered lists are created with a - or + symbol followed by a space and text to be bulleted.
    - `- list` becomes

- list

5. Finally, there is the GitHub specific feature of emojis. Each emoji is an emoji code ([GitHub Emoji Cheat Sheet](https://github.com/ikatyang/emoji-cheat-sheet/blob/master/README.md)) enclosed by colons.
    - `:+1:` becomes :+1:
