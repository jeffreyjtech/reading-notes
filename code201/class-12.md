# Read 12 - Docs for the HTML `<canvas>` Element & Chart.js

## [Chart.JS API Tutorial](https://www.webdesignerdepot.com/2013/11/easily-create-stunning-animated-charts-with-chart-js/)

- Chart JS is added into HTML with a `<script>` element in the `<head>`
- Combine with a `<canvas>` to render charts
- Drawing shapes
  - `Chart().Line()`
  - `Chart().Pie()`
  - `Chart().Bar()`

## [Canvas API: Basic usage](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Basic_usage)

- The `<canvas>` element: Has a similar appearance to `<img>` but creates a drawing surface instead of an embedding an image.
- When a `<canvas>` element is "loaded" into JS (assigned to a variable to make an element object), Canvas API methods can be applied to it to draw shapes
- Canvas methods
  - `.getContext()`: Obtains the rendering context and its drawing functions

## [Canvas API: Drawing shapes](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Drawing_shapes)

- The grid
- Drawing rectangles
  - `.fillStyle()`
  - `.fillRect()`
  - `.strokeRect()`
- Drawing paths
  - `.beginPath()`
  - `.closePath()`
  - `.stroke()`
  - `.fill()`
- Pen manipulation and path creation
  - `.moveTo()`
  - `.lineTo()`
  - `.arc()`
  - `.quadraticCurveTo()`
  - `.bezierCurveTo()`
  - `.rect()`
- `Path2D()`

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
