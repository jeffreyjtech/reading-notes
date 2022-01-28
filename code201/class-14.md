# Combined Reading: 14a and 14b

## 14a | CSS Transforms, Transitions, and Animations

## [CSS Transforms](https://learn.shayhowe.com/advanced-html-css/css-transforms/)

The `transform` property allows transformation of elements in HTML in the geometric sense

### Transform syntax

Transform is not universally supported so a transform property made be repeated with multiple vendor prefixes to work on as many browsers as possible. The following codeblock copied from the [reading material](https://learn.shayhowe.com/advanced-html-css/css-transforms/#transform-syntax) demonstrates this

```css
div {
  -webkit-transform: scale(1.5);
     -moz-transform: scale(1.5);
       -o-transform: scale(1.5);
          transform: scale(1.5);
}
```

### Flavors of transform

- 2D: The following properties apply 2D transformations to an HTML element
  - `transform: scale()`
  - `transform: rotate()`
  - `transform: translate()`
  - `transform: skew()`
  - `transform-origin:`
- Pseudo-3D:
  - `transform: perspective()`
    - `perspective:`
    - `perspective-origin:`
- 3D: The following properties apply 3D transformations to an HTML element
  - `transform: rotateX()` and `transform: rotateY()`
  - `transform: scaleZ()`
  - `transform: translateZ()`
  - `transform-style:`
  - `backface-visibility:`

## [Transitions and Animations](https://learn.shayhowe.com/advanced-html-css/transitions-animations/)

### Transitions

Transitions are the state change that can occur when an element is hovered over, focused on, clicked on, etc.

Like the transform property, vendor prefixes may be need to have your transitions render on as many platforms as possible.

Not all CSS properties can be changed by transition. These are ones that cannot deterministically have a specific middle state.

- Transition CSS properties
  - `transition-property:`
  - `transition-duration:`
  - `transition-timing-function:`
  - `transition-delay:`
- Transition shorthand `transition:`

### Animations

Animations, as defined in CSS using the `@keyframes` selector, allow for more complex transitions. The `@keyframes` selector must be vendor-prefixed to work, and repeated with different prefixes to work on multiple browsers.

- `@keyframes`: The `@keyframes` selector has the special property of not directly affecting any element by itself. It must be followed by a name to be used in the `animation-name:` property of another element.
- Required properties for animations
  - `animation-name:` This property links the given value to an animation with that name.
  - `animation-duration:` How long the animation lasts
- More animation properties:
  - `animation-timing-function:`
  - `animation-delay:`
  - `animation-iteration-count:`
  - `animation-direction:`
  - `animation-play-state:`
  - `animation-fill-mode:`

## 14b | [What Google Learned About Teams](https://www.google.com/amp/mobile.nytimes.com/2016/02/28/magazine/what-google-learned-from-its-quest-to-build-the-perfect-team.amp.html)

This article was an interesting read. I like it to the point that I would rather reflect on it than just write notes:

The main thrust of it is that psychological safety is one of the few common threads which great teams have in common. An environment where people can share themselves naturally ends up being one where people do their best work. It's a source of stress and self-doubt to pretend to be someone else or deliberately hide what's going on in your personal life, even if it's for the sake of having a "game face" on while at work.

This demonstrates itself primarily with people socializing with their colleagues, like actually socializing, not just talking about work. My own experiences at work are reflected in this. The last few months at my job I started to share myself more and work became more fun and less stressful. Also, something that I really liked about my last manager was that, before our weekly standup, he would volunteer someone to come up with a joke and have them kick off the meeting with it. That ritual is actually a great idea based off the insights of this article.

The second demonstration of the psychological safety in a good team is the fact that members end up talking proportionally. There may be long diatribes, but eventually everyone says what's on their mind with tact and consideration. This too is something I've seen. Meetings where half the team isn't talking, for whatever reason, end up being a waste and alienating for those not contributing.

The story of Project Aristotle is something I'm tempted to totally gloss over since the article's conclusion points out how it produced very conventional wisdom. But I will say, it's great that they found out what *wasn't* the major factors that make a good team. Things like grouping by personalities, intelligence, or other seemingly-sensible heuristics were just not significant in comparison to psychological safety.

I think it's unfortunate that we live in a world where an astoundingly thorough and systematic research project had to be conducted in order to prove that human beings are, in fact, social creatures with emotional needs that are important at all times. It's good that they could come up with a vocabulary by which to emphasize it's importance, but ultimately I think it shows the flaws in the existing social constructs of the business and tech world. If we know numbers aren't more important than people, why should we need numbers to prove that?
