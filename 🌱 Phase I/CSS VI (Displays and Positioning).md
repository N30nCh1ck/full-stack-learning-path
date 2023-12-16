>**Ref:** [[CSS#Display]], [[CSS#Position]], [Learn CSS display property in 4 minutes! 🧱](https://www.youtube.com/watch?v=9T8uxp5hQ60) 

**Default Template**
- create a new directory with name `display-and-position` to separate your HTML and CSS files.
- create a new HTML template with the title `Display & Position` and link the CSS file for styling later.

For CSS root style use `* { /* CSS goes here */ }`:
- padding and margin `10px`
- line height `30px`
- `box-sizing: border-box`

**HTML Default Display**
The `block-level` start on a new line, take up the full width available e.g. `<h1>`, `<div>`, `<p>`, `<form>`, `<header>`, and `<footer>`.
- add `<div>` class `heading`, bg-color `antiquewhite`, `10px` padding and add the following inside:
	- `<h1>` with text "Header I", bg-color `#eba2a2`, `10px` padding and margin.
	- `<p>` with text `lorem7`, bg-color `#9393f7`, `10px` padding and margin.
	- a pure `lorem` or `lorem30` text without any wrapper.

The `inline` do not start on a new line, width is limited to what is needed e.g. `<span>`, `<a>`, and `<img>`.
- add `<article>` class `content`, bg-color `skyblue`, padding `50px`, margin `20px` and add the following inside:
	- `<span>` with text `lorem4`, bg-color `#ebc277`, padding `10px`.
	- `<img>` with source `https://i.ibb.co/Q9TjJNq/neon-chick.png` width `100px` and height `auto`.
	- `<a>` with target `_blank` to the `<img>` source link, no underline, bg-color `#5fdb5f`, padding `10px`, color `#2b2b2b`.
	- a pure `lorem` or `lorem30` text without any wrapper.

The following image shows how **HTML Default Display** works.

![[default-html-display.png]]

Try to custom `width` and `height` to the following tags:
- `<h1>`, `<p>`, `<span>`, `<a>` width and height to `300px` and `100px`.
- and see what happens

![[display-inline-and-block.png]]

**CSS Display Property**
The `display` property specifies if/how an element is displayed.

If you are done with the previous section. Then try to add `display` to the following tags:
- `<h1>`, `<p>` to `inline`.
- `<span>`, `<img>`, `<a>` to `block`.
 
Now, here we are!

![[custom-css-display.png]]

>**TIP:** If your results don't match the picture. Try to specify CSS for each HTML tag individually.

Let's try `inline-block`. Theoretically, the `inline-block` is the combination of `inline` and `block`, but you can't trust any theory that you didn't prove by yourself.
- change `<p>` and `<a>` to `inline-block`

Do you get something like this?

![[display-inline-block.png]]

**Display Flex**
Next one is `display: flex;`. Flex is a property that is used to create a flex container. Flexbox, or the Flexible Box Layout, is a layout model in CSS that allows you to design complex layouts more efficiently and with less code than traditional models.
- add `width: 480px` to class `heading` and `content` 
- inside `body` add `display: flex`

![[display-flex.png]]

- add `flex-wrap: wrap` in `body` then try to stretch and shrink your screen.

![[flex-wrap.gif]]

After that add the following inside `body`:
- set width and height `100vw`, `100vh` in order
- `align-items: center` and `justify-content: center` 
- then stretch and shrink your screen again.
- after that replace `flex-wrap: wrap` with `flex-direction: column`
- reduce box size by remove `padding` and `margin` from `heading` and `content`

![[flex-center-item.png]]

This is the easiest way to set items centered by using `display: flex`, `align-items: center`, and `justify-content: center`.

**Display Grid**
"Grid," is a layout system in CSS that allows you to create two-dimensional layouts with rows and columns. The `display: grid` property is used to define a container as a grid container, and its children become grid items.
- restructure your HTML by using this template
```html
<!-- Grid Container -->
<div class="grid-container">
  <!-- Grid Items -->
  <div class="grid-item">Item 1</div>
  <div class="grid-item">Item 2</div>
  <div class="grid-item">Item 3</div>
  <div class="grid-item">Item 4</div>
  <div class="grid-item">Item 5</div>
  <div class="grid-item">Item 6</div>
</div>
```
- replace `Item 1` with your `<h1>`
- do the same with `Item 2` with your `<p>`
- `Item 3` with the long `lorem` text
- `Item 4` with `<span>`
- `Item 5` with `<img>`
- and `Item 6` with `<a>`
- then add the following CSS:
	- for `grid-container` display `grid`, `grid-template-columns: repeat(3, 1fr)` (Three columns with equal width), and `grid-gap: 20px` (Gap between rows and columns)
	- for `grid-item` bg-color `lavender`, color `#2b2b2b`, width `360px`, height `240px`, and align text to center

![[display-grid.png]]

**CSS Position Property**
From the previous section if you already match your result with the picture. Let's try the CSS position in each grid item.
- add `position-n` class to each **Grid Item** in HTML such as `<div class="grid-item position-1">`

**Position Static**
- remove `width` and `height` from your `<h1>` 
- for `position-1` (which contain `<h1>`) add the following:
	- `position: static` (default value, you can omit this line)
	- make `<h1>` centered by display `flex`, `align-items: center`, and `justify-content: center`
	- rename text inside `<h1>` to "Static"

![[position-static.png]]

**Position Relative**
- for `position-2` (which contain `<p>`) add the following:
	- add `<h1>` with text "Relative"
	 - `position: relative`
	 - make everything inside centered by display `flex`, `align-items: center`, `justify-content: center`, and `flex-direction: colomn`
	 - `top` and `lift` to `40px`
	 - border `#9393f7`, `solid`, `2px`

![[position-relative.png]]

**Position Absolute**
- inside `position-2` custom `<p>` by the following:
	- replace HTML text with "Absolute `<br>` Inside Relative"
	- remove `display` (set to default) and `height`
	- change `width` to `150px`
	- add `position: absolute`
	- `top` and `left` to `-50px`
	- font weight `bold` and font size `18px`

![[position-absolute.png]]

**Position Fixed**
- inside `body` do the following:
	- remove `justify-content`, `flex-wrap`
	- edit `width` to `100%` and `height` to `150vh`
	- add padding `20px`
- replace `<span>` (inside `position-4`) text with "Fixed" and set the following:
	- display flex
	- align item `center`
	- justify content `center`
	- font weight `bold`
	- font size `18px`
	- position `fixed`
	- `top` and `left` to `20px`
	- `width` and `height` to `100px`
	- bg-color `#ebc277`
	- padding `10px`
 
![[position-fixed.png]]

**Position Sticky**
- inside `position-5` custom `<img>` tag by the following:
	- set position to `sticky`
	- add `z-index` to `99`
	- and `top` to `20px`

![[position-sticky.gif]]

>**Sticky Positioning:** can stick in a specified position, but can't go outside their parent


#css #phase-1 #assignment #displays-and-positioning 