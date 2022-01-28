# Read 12 - Docs for the HTML `<canvas>` Element & Chart.js

## [Chart.JS API Tutorial](https://www.webdesignerdepot.com/2013/11/easily-create-stunning-animated-charts-with-chart-js/)

- Chart JS is added into HTML with a `<script>` element in the `<head>`
- Combine with a `<canvas>` to render charts
- The following constructor functions create charts of various types:
  - `Chart().Line()`
  - `Chart().Pie()`
  - `Chart().Bar()`

## [Canvas API: Basic usage](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Basic_usage)

- The `<canvas>` element: Has a similar appearance to `<img>` but creates a drawing surface instead of an embedding an image.
- When a `<canvas>` element is "loaded" into JS (assigned to a variable to make an element object), Canvas API methods can be applied to it to draw shapes
- Canvas methods
  - `.getContext()`: Obtains the rendering context and its drawing functions

## [Canvas API: Drawing shapes](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Drawing_shapes)

- The grid: The canvas element has a grid defined in pixels, which is equivalent to it's real size in pixels on the webpage.
- Drawing rectangles
  - `.fillRect()`: This draws a solid rectangle
  - `.strokeRect()`: this draws a rectangle outline
  - `.clearRect()`: This clear a rectangular area of any fill
  - `.rect()`: This creates a rectangle of the specified length and width whose top left corner is at the specified x,y coordinate position.
- Drawing paths
  - `.beginPath()`: This defines where a drawing path starts
  - `.closePath()`: This tells CSS to draw a line between the start of the path and wherever the "path cursor" is currently.
  - `.stroke()`: This draws an outline of the laid out path
  - `.fill()`: This fills the laid out path.
- Pen manipulation and path creation
  - `.moveTo()`: This moves the "path cursor" to a pixel coordinate position.
  - `.lineTo()`: This draws a line from the current "path cursor" position to the specified x and y point. 
  - `.arc()`: This takes in several arguments to draw a specified arc.
    - `.quadraticCurveTo()` & `.bezierCurveTo()`: : Like `.arc()`, these draw a quadratic curve or a bezier curve based off a formula fed by the several arguments you are required to pass in.
- `Path2D()`: Path 2D is a new (or recently updated) API which provides simpler function calls for drawing shapes.

## [Canvas API: Applying styles and colors](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Applying_styles_and_colors)

- Coloring
  - `.fillStyle() = color`: Colors the shape's area
  - `.strokeStyle() = color`: Colors the shape's outline
- Transparency
  - `.globalAlpha` property
- Line Styling
  - `.lineWidth`
  - `.lineCap`
  - `.lineJoin`
  - `.miterLimit`
  - `.getLineDash()`
  - `.setLineDash()`
  - `.lineDashOffset`
- Miter Limit Behavior
- Gradients
  - `.createLinearGradient()`
  - `.createRadialGradient()`
  - `.createConicGradient()`
  - `.gradient.addColorStop()`
- Patterns `.createPattern()`
- Shadows
  - `.shadowOffsetX`
  - `.shadowOffsetY`
  - `.shadowBlur`
  - `.shadowColor`
- Canvas fill rules
  - `'nonzero'`
  - `'evenodd'`

## [Canvas API: Drawing text](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Drawing_text)

- Drawing text methods
  - `.fillText()`
  - `.strokeText()`
- Text properties
  - `.font`
  - `.textAlign`
  - `.textBaseline`
  - `.direction`
