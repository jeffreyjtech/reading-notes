# CSS Reading Notes

## What is CSS?

> Cascading Style Sheets

The language that describes how HTML elements look. It is a rule-based language, and can be used to change color, size, font, layout, and even create animations.

The CSS language is broken into modules which can be referenced in MDN or another web resources.

### Adding CSS

CSS can be added to an HTML page externally, internally, and inline.

External: CSS is added externally by linking a `.css` stylesheet with the link tag, typically written on the line after the opening `<head>` tag.

```html
<link rel="stylesheet" href="style.css">
```

Internal: CSS is added externally by enclosing CSS rules between a set of `<style>` `</style>` tags, typically written on the line after the opening `<head>` tag.

```html
<style>
  p {
    color: black;
  }
</style>
```

Inline: CSS is added inline by writing the `style` attribute into an element's tag.

```html
<p style="color:black;">I've written a paragraph here</p>
```

## CSS Syntax

The following codeblock is a complete CSS rule.

```css
#boxybox p, .potato {
    font-size: 10px;
    border: thick black;
    display: relative;
}
```

- **Selector**: The selector comes right before the rule in curly braces, and the selector is used to choose which HTML elements recieve the rule.
  - `#boxybox` -  id selector
  - `.potato` - class selector
  - `p` - element selector

  > Rules when using multiple selectors:
  >
  > - Selectors in sequence `#boxybox p {}`, with just a space between, have a parent-child relationship. The CSS rule above will only apply to `<p>` elements within another element id'ed as `boxybox`, or \<p> elements with the id `boxybox`, for example `<p id="boxybox">`. 
  > - Selectors seperated by commas `#boxybox, p {}` allows the following rule to apply to all `<p>` elements and all `#boxybox`- ID'd elements.

- **Rule**: A rule is "completed property" which can be applied to an HTML element.
- **Property**: A property is the specific attribute of an element that you want to change
  - `font-size`
  - `border`
  - `display`
- **Value**: The value is what you assign to a property. Valid valueas can be strings as defined in the CSS specifications or numerical values with different units.
  - `10px`
  - `black`
  - `thick`
- **Curly Brackets (braces)**: Encloses the properties and values, thus creating a complete rule which can then be applied to HTML elements as chosen by the selector.

## Color

Colors in CSS can be defined with (1) semantic names, (2) RGBa values, and (3) hex values. These are not the only valid syntaxes, others can be found at the [Color MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/color).

1. `black`, or `white`, or `blue`
2. `rgba(255,255,255,1)` (the RGBa value for solid white)
3. `#ffffff` (the hex value for white, which is an encoding of RGB)

Different aspects of elements can be assigned different colors by modifying the correct property. Some examples are:

- `color` changes the color of text within an element
- `background-color` changes the background color of an element
- `border-color` changes the border color of an element
