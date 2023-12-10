CSS or Cascading Style Sheets is a stylesheet language used in web development to describe the presentation and styling of HTML or XML documents. It enables the separation of content and design, allowing developers to control the appearance of web pages by defining styles for elements such as layout, fonts, colors, and more.

## Connecting CSS to HTML
Connecting CSS to HTML involves linking the CSS stylesheet file to the HTML document. There are three ways of connecting CSS to HTML: Inline CSS, Internal (or Embedded) CSS, and External CSS.

#### Inline CSS
Inline CSS is applied directly to individual HTML elements using the `style` attribute. This method is useful when you want to apply styles to a specific element without affecting others.

```css
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Inline CSS Example</title>
</head>
<body>
  <h1 style="color: blue;">Hello, World!</h1>
  <p style="font-size: 16px; line-height: 1.5;">This is an example of inline CSS.</p>
</body>
</html>
```

In this example, styles are applied directly to the `h1` and `p` elements using the `style` attribute.

#### Internal (or Embedded) CSS
Internal CSS is placed within the `<style>` element in the `<head>` section of the HTML document. This method is suitable for applying styles to multiple elements within the same HTML file.

```css
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Internal CSS Example</title>
    <style>
      body {
        background-color: #f0f0f0;
        font-family: Arial, sans-serif;
      }
      h1 {
        color: #333;
      }
      p {
        font-size: 16px;
        line-height: 1.5;
      }
    </style>
  </head>
  <body>
    <h1>Hello, World!</h1>
    <p>This is an example of internal CSS.</p>
  </body>
</html>
```

In this example, styles are defined within the `<style>` element in the `<head>` section.

#### External CSS
External CSS involves creating a separate CSS file and linking it to the HTML document using the `<link>` element. This method is preferred for maintaining a consistent style across multiple HTML files.
`styles.css`
```css
/* styles.css */
body {
  background-color: #f0f0f0;
  font-family: Arial, sans-serif;
}
h1 {
  color: #333;
}
p {
  font-size: 16px;
  line-height: 1.5;
}
```
`index.html`
```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>External CSS Example</title>
    <link rel="stylesheet" href="styles.css" />
  </head>
  <body>
    <h1>Hello, World!</h1>
    <p>This is an example of external CSS.</p>
  </body>
</html>
```

In this example, the styles are defined in an external `styles.css` file, and the HTML file links to it using the `<link>` element.

## CSS Reference
The CSS reference, often found in documentation or guides, is a comprehensive resource providing information about CSS selectors, properties, values, and syntax.

>There are other CSS reference that weren't mentioned in this documentation. To see the rest of them go to [CSS Reference](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference) and look at the left bar menu.

#### Selector
Selectors are patterns used to select and style HTML elements. They can be based on element names, classes, IDs, attributes, or a combination of these. For example, `h1` selects all `<h1>` elements, `.class` selects elements with a specific class, `#id` selects elements with a specific ID, and so on.

###### Element Selector
Targets HTML elements based on their name.
```html
<p>This is a paragraph with the Element Selector.</p>
<p>another paragraph that was selected</p>
<p>and another that was selected</p>
```
`styles.css`
```css
/* Selects all <p> elements */
p {
  color: blue;
}
```

###### Class Selector
Targets elements with a specific class attribute.
```html
<p class="highlight">This is a paragraph with the Class Selector.</p>
```
`styles.css`
```css
/* Selects elements with the class 'highlight' */
.highlight {
  background-color: yellow;
}
```

###### ID Selector
Targets a specific element with a unique ID attribute.
```html
<h2 id="header">Header with ID</h2>
```
`styles.css`
```css
/* Selects the element with the ID 'header' */
#header {
  font-size: 32px;
  color: purple;
}
```

###### Attribute Selector
Targets elements based on the presence or value of their attributes.
```html
<a href="#" target="_blank">link</a>

<input type="text">
```
`styles.css`
```css
/* Attribute Selector */
a[target] {
  text-decoration: none;
  color: red;
}

input[type="text"] {
  border: 1px solid #ccc;
  border-radius: 5px;
  padding: 10px;
}
```

###### Descendant Selector
Selects an element that is a descendant of another element.
```html
<div>
  <span>This span is selected using the Descendant Selector.</span>
</div>
```
`styles.css`
```css
/* Descendant Selector */
div span {
  font-weight: bold;
  color: #424242;
}
```

>Descendant selectors are less specific because they target all descendants, regardless of their level of nesting.
###### Child Selector
Selects an element that is a direct child of another element.
```html
<ul>
  <li>List item 1</li>
  <li>List item 2</li>
  <li>List item 3</li>
  <li>List item 4</li>
</ul>
```
`styles.css`
```css
/* Child Selector */
ul > li {
  list-style-type: square;
}
```

>Child selectors are more specific as they only target immediate children.
###### Adjacent Sibling Selector
Selects an element that is immediately preceded by a specified element.
```html
<h2>Header with ID</h2>
<p>
  This paragraph is immediately preceded by an H2 and affected by the
  Adjacent Sibling Selector.
</p>

<p>This paragraph WAS NOT affected by Adjacent Sibling Selector</p>
```
`styles.css`
```css
/* Adjacent Sibling Selector */
h2 + p {
  color: hotpink;
}
```

###### General Sibling Selector
Selects all elements that are siblings of a specified element.
```html
<h1>Header with ID</h1>
<p>Also NOT affected paragraph</p>

<h2>Header with ID</h2>
<p>
  This paragraph is immediately preceded by an H2 and affected by the
  General Sibling Selector.
</p>

<p>This also affected by Adjacent Sibling Selector</p>

<div>
  <p>This paragraph WAS NOT affected by Adjacent Sibling Selector</p>
</div>
```
`styles.css`
```css
/* General Sibling Selector */
h1 ~ p {
  font-style: italic;
}
```

###### Pseudo-class Selector
Selects elements based on their state or position.
```html
<a href="#" target="_blank">"Gold" color when hover</a>.

<ul>
  <li>List item 1</li>
  <li>List item 2 lightgray bg color</li>
  <li>List item 3</li>
  <li>List item 4 lightgray bg color</li>
</ul>
```
`styles.css`
```css
/* Pseudo-class Selector */
a:hover {
  color: gold;
}

ul li:nth-child(even) span {
  background-color: lightgray;
}
```

###### Pseudo-element Selector
Selects a specific part of an element.
```html
<p>A first line is bigger and bold. Lorem ipsum dolor sit amet.</p>
<p>All paragraph have a "Note: " prefix with lightgray color</p>
```
`styles.css`
```css
/* line length 300px */
p {
  width: 300px;
}

/* Pseudo-element Selector */
p::first-line {
  font-weight: bold;
  font-size: 18px;
}

p::before {
  content: "Note: ";
  color: #888;
}
```

#### Properties and Values
CSS properties and values work together to style HTML elements. Properties define the aspect being styled (e.g., color, font-size), while values assign specific settings to those properties, determining how the elements should look or behave on a webpage.

Below is a short demonstration of the use of 10 different CSS properties with their values.

###### Color
The `color` property in CSS is used to define the text color of an HTML element. It allows you to set the color of the text content within an element. The value of the `color` property can be specified using various formats such as named colors, hexadecimal values, RGB values, HSL values, and more.
```css
body {
  /* Color Name */
  color: red;
}
h1 {
  /* Hexadecimal Notation */
  color: #ff0000; /* Red */
}
p {
  /* RGB Notation */
  color: rgb(255, 0, 255); /* Magenta */
}
a {
  /* HSL Notation (Hue, Saturation, Lightness) */
  color: hsl(120, 100%, 50%); /* Green */
}
span {
  /* HSLA Notation (with Alpha Channel for Transparency) */
  color: hsla(240, 100%, 50%, 0.7); /* Semi-transparent blue */
}
```

###### Font
The `font` property in CSS is a shorthand property that allows you to set multiple font-related properties in a single declaration. It simplifies the process of specifying the font style, variant, weight, size, line height, and family for text within an element.

```css
selector { 
  font: style variant weight size/line-height family;
}
```

In the shorthand, the properties are specified in the order of `font-style`, `font-variant`, `font-weight`, `font-size`, `line-height`, and finally, `font-family`. However, you can omit any of these properties if you don't need them, and the remaining ones will still be applied.

`font-family`, `font-size`
```css
body {
  font: 16px Arial, sans-serif;
}
/* Or you can use */
body {
  font-family: Arial, sans-serif;
  font-size: 16px;
}
```

`font-style`, `font-size`, `font-family`
```css
h1 {
  font: italic 24px 'Times New Roman', serif;
}
/* Or you can use */
h1 {
  font-style: italic;
  font-size: 24px;
  font-family: 'Times New Roman', serif;
}
```

`font-weight`, `font-size`, `font-family`
```css
p {
  font: bold 14px Verdana, sans-serif;
}
/* Or you can use */
p {
  font-weight: bold;
  font-size: 14px;
  font-family: Verdana, sans-serif;
}
```

`font-style`, `font-variant`, `font-size`, `font-family`
```css
.quote {
  font: italic small-caps 18px 'Georgia', serif;
}
/* Or you can use */
.quote {
  font-style: italic;
  font-variant: small-caps;
  font-size: 18px;
  font-family: 'Georgia', serif;
}
```

`font-size`, `line-height`, `font-family`
```css
article {
  font: 16px/1.5 'Helvetica', sans-serif;
}
/* Or you can use */
article {
  font-size: 16px;
  line-height: 1.5;
  font-family: 'Helvetica', sans-serif;
}
```

In CSS, the order of properties within a declaration block generally does not matter. However, it's a good practice to follow a logical order for better readability and maintenance of your code. When dealing with font-related properties, including `font-family` and `font-size`, you might want to consider the following sequence:

1. **`font-style`:** Set the style of the font (e.g., normal, italic, oblique).
2. **`font-variant`:** Set the variant of the font (e.g., normal, small-caps).
3. **`font-weight`:** Set the weight of the font (e.g., normal, bold).
4. **`font-size`:** Set the size of the font.
5. **`line-height`:** Set the height of a line of text.
6. **`font-family`:** Specify the font family or list of font families.

###### Text
The `text` property in CSS is not a standalone property. Instead, it is used as part of other properties to style various aspects of text within HTML elements.

The `text-align` specifies the horizontal alignment of text content within an element.
```css
p {
  text-align: center; /* Can be "left" or "right" either */
}
```

The `text-decoration` sets the decoration properties for text, such as underline, overline, and line-through.
```css
a {
  text-decoration: none; /* Removes underline from links */
}
```

The `text-transform` controls the capitalization of text.
```css
h1 {
  text-transform: uppercase; /* capitalize, lowercase, others */
}
```

The `letter-spacing` adjusts the space between characters in text.
```css
p {
  letter-spacing: 2px;
}
```

The `white-space` determines how white space inside an element is handled.
```css
pre {
  white-space: pre-wrap; /* Preserves white space and allows wrapping */
}
```

###### Background
The `background` property in CSS is a shorthand property that allows you to set various background-related properties for an HTML element. It combines several background properties into a single declaration for convenience.

```css
.shorthand {
  background: background-color background-image background-repeat background-attachment background-position;
}
```

The `background` property is quite versatile, allowing you to set color, image, position, repeat, and other background-related properties in a single line. You can choose to include only the properties you need for a specific element's background styling.

`background-color` sets the background color of an element.
```css
body {
  background-color: #f0f0f0; /* Light gray background */
}
```

`background-image` sets one or more background images for an element.
```css
header {
  background-image: url('header-background.jpg');
}
```

`background-repeat` specifies how a background image should be repeated.
```css
section {
  background-image: url('pattern-background.png');
  background-repeat: repeat-x; /* Repeat horizontally */
}
```

`background-attachment` sets whether a background image is fixed or scrolls with the page.
```css
body {
  background-image: url('fixed-background.jpg');
  background-attachment: fixed; /* Fixed background */
}
```

`background-position` sets the initial position of a background image.
```css
article {
  background-image: url('article-background.jpg');
  background-position: top right; /* Position at the top right corner */
}
```

###### Width & Height
In CSS, the `width` and `height` properties are used to control the dimensions of elements. They determine the width and height of an element, respectively. These properties can be set using various units such as pixels, percentages, viewpoint units, and more.

`px`
```css
div {
  width: 200px;
  height: 100px;
}
```

`%` 
```css
.container {
  width: 80%;
  height: 300px;
}
```

`vw`, `vh`
```css
section {
  width: 50vw; /* 50% of the viewport width */
  height: 80vh; /* 80% of the viewport height */
}
```

`auto`
```css
.box {
  width: auto;
  height: auto;
}
```

`max-width`, `max-height`, `min-width`, `min-height`
```css
img {
  max-width: 100%;
  max-height: 200px;
  min-width: 50px;
  min-height: 50px;
}
```

###### Margin
In CSS, the `margin` property is used to control the space around an element's content. It defines the empty space outside the border of an element and separates it from other elements on the page.

`margin` this example sets a margin of 10 pixels on all sides of the `div` element.
```css
div {
  margin: 10px;
}
```

`margin-top`, `margin-right`, `margin-bottom`, `margin-left`
```css
p {
  margin-top: 20px;
  margin-right: 10px;
  margin-bottom: 30px;
  margin-left: 15px;
}
/* Or */
p {
  margin: 20px 10px 30px 15px;
}
```
The shorthand `margin` property allows you to specify values for the top, right, bottom, and left margins in a single declaration.

>If you omit values, they will be set to the same value as the previous one in the sequence. 
>e.g. for 3 and 2 parameters
>	`margin: 20px 10px 30px` it means top `20px`, right and left `10px`, and bottom `30px`.
>	`margin: 20px 10px` it sets the top and bottom `20px`, right and left `10px`.

Percentage Margin
```css
img {
  margin: 2%;
}
```

Using the `auto` Value
```css
.content {
  width: 600px;
  margin: 20px auto;
}
```
Setting the left and right margins to `auto` horizontally centers the block-level element within its containing element.

###### Padding
In CSS, the `padding` property is used to control the space between an element's content and its border. It defines the internal space within an element and contributes to the overall size of the element.

**TLDR;**
>The most common uses for **Padding** and **Margin** are set in the same way.

`padding` this example sets a padding of 10 pixels on all sides of the `div` element.
```css
div {
  padding: 10px;
}
```

`padding-top`, `padding-right`, `padding-bottom`, `padding-left`
```css
p {
  padding-top: 20px;
  padding-right: 10px;
  padding-bottom: 30px;
  padding-left: 15px;
}
/* Or */
p {
  padding: 20px 10px 30px 15px;
}
```
The shorthand `padding` property allows you to specify values for the top, right, bottom, and left margins in a single declaration.

>If you omit values, they will be set to the same value as the previous one in the sequence. 
>e.g. for 3 and 2 parameters
>	`padding: 20px 10px 30px` it means top `20px`, right and left `10px`, and bottom `30px`.
>	`padding: 20px 10px` it sets the top and bottom `20px`, right and left `10px`.

Using `em` Units
```css
h1 {
  padding: 1em;
}
```

Using the `auto` Value
```css
.container {
  width: 50%;
  padding: 20px auto;
}
```
Setting the left and right margins to `auto` horizontally centers the block-level element within its containing element.

###### Border
In CSS, the `border` property is used to define the border of an element. The border surrounds the padding area and the content of the element. It can be used to set the style, color, and width of the border.

```css
.shorthand {
  /* Shorthand syntax */
  border: [border-width] [border-style] [border-color];
}

.card {
  /* Example usage */
  border: 2px solid #3498db; /* 2-pixel wide solid border with the color #3498db */
}
/* Or */
.card {
  /* Individual properties */
  border-width: 2px;
  border-style: solid;
  border-color: #3498db;
}
```

`border-radius`
```css
.card {
  /* 1-pixel wide solid border with rounded corners */
  border: 1px solid #333;
  border-radius: 5px; /* Adds rounded corners */
}
```

`none`
```css
button {
  /* No border */
  border: none;
}
```

###### Display
In CSS, the `display` property is used to specify how an element should be rendered on the page. It controls the layout behavior of an element and determines whether it behaves like a block, inline, inline-block, or other display types.

`block`
```css
div {
  display: block;
}
```
The element generates a block-level box, causing a line break before and after the element.

`inline`
```css
span {
  display: inline;
}
```
The element generates an inline-level box, allowing it to flow within the text and not causing line breaks before or after.

`inline-block`
```css
img {
  display: inline-block;
}
```
The element generates an inline-level block container. It behaves as an inline-level element but can have block-like properties.

`flex`
```css
.container {
  display: flex;
}
```
The element generates a flex container, and its children become flexible items. It allows for advanced alignment and distribution of space.

`grid`
```css
.container {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
}
```
The element generates a grid container, and its children become grid items. It allows for a two-dimensional layout system.

`none`
```css
.hidden {
  display: none;
}
```
The element is not rendered on the page. It effectively hides the element.

###### Position
In CSS, the `position` property is used to specify the positioning method for an element within its containing element.

`static` 
```css
div {
  position: static;
}
```
This is the default value. Elements with `position: static;` are positioned according to the normal flow of the document.

`relative`
```css
div {
  position: relative;
  top: 10px;
  left: 20px;
}
```
Elements with `position: relative;` are positioned relative to their normal position in the document flow. Using the `top`, `right`, `bottom`, and `left` properties, you can offset the element from its normal position.

`absolute`
```css
.parent {
  position: relative;
}

.child {
  position: absolute;
  top: 50px;
  left: 50px;
}
```
Elements with `position: absolute;` are removed from the normal document flow and positioned relative to their nearest positioned (not static) ancestor.

`fixed`
```css
div {
  position: fixed;
  top: 0;
  right: 0;
}
```
Elements with `position: fixed;` are removed from the normal document flow and positioned relative to the browser window. They remain in the same position even when the page is scrolled.

`sticky`
```css
div {
  position: sticky;
  top: 20px;
}
```
Elements with `position: sticky;` are a hybrid of `relative` and `fixed` positioning. They are treated as `relative` positioned until they cross a specified threshold, after which they are treated as `fixed` positioned.

#### Example CSS At-Rules
CSS at-rules are instructions for CSS processors to control aspects of the styling process. They begin with the "@" symbol and are followed by keywords and various parameters.

###### @import
- **Purpose:** Imports an external style sheet into the current style sheet.
- **Usage:** Typically placed at the beginning of a style sheet to import styles from another file.
```css
@import url('styles.css');
```

###### @media
- **Purpose:** Specifies styles for a specific media type or device characteristics.
- **Usage:** Allows for responsive design by applying styles based on conditions such as screen width, device orientation, etc.
```css
@media screen and (min-width: 600px) {
  /* Styles for screens wider than 600px */
  body {
    font-size: 18px;
  }
}
```

###### @font-face
- **Purpose:** Describes the font to be used for text in the document.
- **Usage:** Enables the use of custom fonts that are not installed on the user's device.
```css
@font-face {
  font-family: 'CustomFont';
  src: url('custom-font.woff2') format('woff2');
}
```

###### @keyframes
- **Purpose:** Defines animations using a set of keyframes.
- **Usage:** Specifies intermediate stages in the CSS animation sequence.
```css
/* Apply the animation to an element */
.box {
  animation: slide-in 1s ease-in; /* Animation name, duration, and easing function */
}

@keyframes slide-in {
  from {
    transform: translateX(-100%);
  }
  to {
    transform: translateX(0);
  }
}
```

#### Example CSS Function
CSS functions are an essential part of modern web development, providing dynamic and reusable solutions to various styling challenges. Here are some commonly used CSS functions.

###### RGB & RGBA
`rgba()` used for defining colors with red, green, blue values along with an alpha (transparency) value.
```css
body {
  background-color: rgba(255, 0, 0, 0.5);
}

h1 {
  color: rgb(255,0,0);
}
```

###### HSL & HSLA
`hsla()` defines colors using hue, saturation, lightness, and alpha (transparency) values.
```css
body {
  background-color: hsla(290, 100%, 50%, 0.3);
}

p {
  color: hsl(120, 100%, 50%); /* Pure green color */
}
```

###### CALC
`calc()` performs calculations to determine a value. Useful for responsive design.
```css
.box {
  width: calc(50% - 20px); /* 50% width minus 20 pixels */
}
```

###### VAR
`var()` allows the use of variables in CSS to promote maintainability and ease of theming.
```css
:root {
  --main-color: #3498db;
}

.box {
  background-color: var(--main-color);
}
```

###### Linear Gradient
`linear-gradient()` creates a gradient effect between two or more specified colors.
```css
body {
  background: linear-gradient(to right, #3498db, #2c3e50);
}
```

###### Radial Gradient
Creates a radial gradient effect.
```css
body {
  background: radial-gradient(circle, #3498db, #2c3e50);
}
```

###### URL
`url()` specifies the location of a resource, such as an image, to be used in the styling.
```css
section {
  background: url('image.jpg') center/cover;
}
```

###### Transform
`transform()` applies transformations to elements, such as rotation, scaling, and translation.
```css
.content {
  transform: translate(20px, 30px) rotate(45deg);
}
```

###### ATTR
Retrieves the value of an attribute from an HTML element and uses it in CSS.
```css
.item {
  content: attr(data-text);
}
```

###### Min and Max
Selects the smaller or larger of two values, respectively.
```css
body {
  width: min(50%, 200px);
  height: max(100%, 300px);
}
```


>`box-shadow` is not a CSS function, but it gives a result like a CSS function e.g. `box-shadow: 2px 2px 5px #888888;` to adds a shadow effect to an element.






3. Guides
	- Box Model
		- Introduction to the box model (content, padding, border, margin)
		- Understanding box sizing
		- Practical exercises to manipulate the box model
	- Display and Position
		- Display property (block, inline, inline-block)
		- Position property (static, relative, absolute, fixed)
		- Float and clear properties
	- Flexbox
		- Introduction to Flexbox layout
		- Properties: flex container and flex items
		- Creating flexible and responsive layouts with Flexbox
	- Grid Layout
		- Introduction to CSS Grid
		- Creating a grid layout with rows and columns
		- Responsive design with Grid
	- Typography
		- Styling text with CSS
		- Font properties (family, size, weight)
		- Text alignment and decoration
	- Transitions and Animations
		- Adding smooth transitions to elements
		- Keyframe animations for more complex animations
		- Creating engaging user experiences with CSS animations
	- Responsive Design
		- Media queries and their role in responsive design
		- Building a responsive navigation bar
		- Flexibility and fluidity in responsive layouts