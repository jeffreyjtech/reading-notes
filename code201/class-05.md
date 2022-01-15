# Read 05 - Images, Color, Text

>Reading notes for Code 201, covering various chapters from *HTML & CSS: Design and Build Websites* and *JavaScript & JQuery: Interactive Front-End Web Development* by Jon Duckett. The book titles have been abbreviated as HTML and JS in the subheadings of these notes.

## HTML | Chapter 5: “Images” (pp.94-125)

- Image formats: The following are *the* most common image file types used on the Web.
  - JPEG: JPEG is a format developed to compress digital photographs to manageable sizes. It uses lossy compression.
  - GIF: GIF is a file type developed for the Web. It's best suited to store simple images and graphics. Outside of certain cases, GIF encoding can be considered lossy.([GIF on Wikipedia](https://en.wikipedia.org/wiki/GIF#File_format)).
    - Animated GIFs: GIFs can also store multiple images, and cycle through them to create animation.
  - PNG: PNG is a true lossless file type developed for the Web. It is best suited for simple images and graphics. Digital photographs stored as PNGs will be excessively large files.
- Image dimensions: Images used on your website should be resized in an image editor software to match their final size on you page.
- Image shape: Images may need to be cropped to fit well into your layouts. Consider the appropriate dimension ratio carefully.
- `<figure>` and `<figcaption>`: Images fit well in the `<figure>` element. The `<figcaption>` element can be used to insert a caption and provide screen reader information.

## HTML | Chapter 11: “Color” (pp.246-263)

- `color`: The color property determines text color within the element.
- `background-color`: The background color property determines the color of the entire element except for text and some other properties.
- Color values and displays: Almost all computer displays produce light by combining red, blue, and green light to color and brighten a single pixel. Therefore they create colors additively. Maximum red, blue, and green makes white.
  - RGB: Color values in CSS can be defined by an RGB value.
  - Hex: Color values can also be defined by a hex value, which is a hexadecimal representation of an RGB value.
  - Color names: Color values can also be defined using one of CSS's pre-determined named colors.
- Contrast: Effective color design should use a high amount of contrast to keep text and other elements readable.
- Opacity: Opacity is the computer-specific measure of translucency. Adding an "alpha channel" (value from 0 to 1) to an RGB value to make an RGBa value will modify the opacity of the target.

## HTML | Chapter 12: “Text” (pp.264-299)

### Typeface Terminology

- Serif: the pointy dangly bits on serif fonts are serifs. They're generally considered to improve readability in dense blocks of text.
- San-serif: Fonts without serifs. They are considered more modern looking, and they're are more common in digital applications than in traditional printing.

- Weight: the thickness or thinness of a font. Modified in CSS with `font-weight`
- Style: *Italics* or oblique (basically italics++) are the common styles. Modified in CSS with `font-style`
- Stretch: Condensed and extended text have different stretch. 

### Choosing Typeface

- Typefaces affect the feel of your site significantly.
- That said, be considerate of the fact that fonts must exist in the user's web browser/device to work.
- Different types of fonts have different purposes.
- The `font-family` property chooses the text's typeface.

### Other CSS properties

- `text-transform`: Depending on the assigned value, this will uppercase, lowercase or automatically capitalize the first letter of words in text.
- `text-decoration`: Can add underline, overline, line-through and a blinking effect.
- The psuedo classes `:hover`, `:active`, and `:focus` allow the text to be style differently depending on user interaction.
- `text-align`: Changes the horizontal alignment of text depending on assigned value.
- `vertical-align`: Changes whether which vertical part of the box that text will be adjacent to.
