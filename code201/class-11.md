# Read 11 - Audio, Video, Images

>Reading notes for Code 201, covering various chapters from *HTML & CSS: Design and Build Websites* and *JavaScript & JQuery: Interactive Front-End Web Development* by Jon Duckett. The book titles have been abbreviated as HTML and JS in the subheadings of these notes.

## HTML | Chapter 16: “Images” (pp.406-427)

- Controlling image size with CSS: `width` & `height`: Images sizes can be controlled in CSS with the width and height properties.
- Image size classes: Organizing your images in to size classes allows you to create consistent and DRY-er property sets to apply to all the images on your site.
- Image location classes: This "image class" idea can be taken further by creating class selectors which apply centering or float properties to appropriately classed images.
- Background images `background-image`: Background images can be added to elements with this property. The url value need to be written as `url("images/kittycat.jpg")`.
  - `background-repeat`: This property sets if/how a bg image will be repeated. Potential values are `repeat`, `repeat-x`, `repeat-y`, `space`, `round`
  - `background-attachment`: This property determines if the background images will scroll with the rest of the page or stay fixed regardless of scroll position.
  - `background-position`: This property will set where on the screen non-repeated images will be placed.
- Image rollovers and sprites: It's possible to use a background image to give a consistent background image for button-like elements of differing sizes and mouse-over behaviors.
- Gradients: Gradient backgrounds are possible in CSS3 using special values assigned to the `background-image` key such a `-moz-linear-gradient(#555555,#000000)`.

## HTML | Chapter 19: “Practical Information” (476-492)

### Search Engine Optimization (SEO)

It's important for the modern web developer to make it so their website doesn't just exist and look great, but also can be found. Search Engine Optimization is the practice of providing search engines the information they want so your content appears in user searches.

Important "on-page" elements are:

- Linked keywords
- Repeated keywords throughout content
- Keywords in URL
- Page title
- Headings
- Image alt text
- Page descriptions using `<meta>` tag(s)

It is important to understand and research what keywords and other data should be in the above SEO elements.

### Google Analytics and You

Google Analytics is a service provided by Google which you can embed into your website. You must insert Google Analytics tracking code onto every page of your website. You can then using the Google Analytics website to view and analyze the behavior of visitors. The provided data can give you insight to where your visitors "land" on your site, where they leave, how many views each page gets, and where your visitors are coming from.

### Domain Names

Owning a domain name gives a special address for your website to live at. You'll also need a web server to host your site. Web hosting companies provide the ability to host a website without actually building a web server's hardware. These can include back-end services like databases. A domain name and web hosting service together can also give you an email server with which to receive email at your personal domain.

### FTP & Other tools

File-transfer protocol is the shorthand term for services that allow you to upload and download data from a web server. Popular providers for this are FileZilla, FireFTP, CuteFTP, SmartFTP, and Transmit.

There are providers for "template sites" which you can use to easily create blogs, e-commerce storefronts, newsletters, and social network buttons.

## [MDN Article on A/V elements](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Client-side_web_APIs/Video_and_audio_APIs)

HTML5 supports embedded `<audio>` and `<video>` elements. The `controls` attribute allows you to enable the default controls to appear on embedded AV content. The HTMLMediaElement API gives you the ability to customize the content controls, and it gives JavaScript the ability to manipulate embedded content as well.

A custom HTML5 video player will be wrapped in a div which the `<video controls>` element and various button elements (play, rewind, forward) will be grouped together. CSS can adjust the look and behavior of these elements. The `<video>` element will be the primary provider/target of methods (`.play`, `.pause`) for JS manipulation. Combined with event handlers, play, pause, fast-forward, rewind, seeking and duration bar can be provided for user interaction. Refer to the heading link for code examples.
