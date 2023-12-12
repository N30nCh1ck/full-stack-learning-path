> Ref: [[CSS#Properties and Values]]

Create new HTML temple and link it with some CSS file to do the assignment below step by step.
###### 1. Color
- add `<h1>`, `<p>`, `<a>`, and `<span>` with some text. 
- and then set the `color` of each element in a difference ways such as `<h1>` use named colors, `<p>` use hexadecimal values, `<a>` use RGB values, `<span>` use HSL values, etc.
- your results should be like something below (if you use the following colors: `tomato`, `#4343e2`, `rgb(68, 216, 76)`, `hsl(39, 83%, 55%)`).

![[using-colors.png]]

>Hint: [[CSS#Color]]

###### 2. Font
- add some shorthand `font` inside `body` using CSS by set:
	- font family: cursive
	- font size: 16px
- try to add `font-style` and `font-weight` without shorthand.
- see the result when you change `font-variant` to `small-caps`.
- add `line-height: 10px` in shorthand at the first font assignment.
- move everything into shorthand then see the results.

![[shorthand-font.png]]

>Hint: [[CSS#Font]]

###### 3. Text
%%If you want to use the previous temple in this section **Remove** the **Shorthand Font** first then replace it with `width: 300px` to continues.%%

- try to transform your `<h1>` text to `uppercase` and set `letter-spacing` to `8px`.
- create 3 lines of `<p>` text then set `text-align` of each to `left`, `center`, and `right`.
- remove underline in `<a>` by using `text-decoration`.

![[text-styling.png]]

>Hint: [[CSS#Text]]

###### 4. Background
- wrap everything inside `<body>` with `<div class="container">`
- change the `background-color` of this `container` class to `lightgoldenrodyellow`.
- match the theme color with `font-family: cursive;` inside `body`.

![[background-color.png]]

>Hint: [[CSS#Background]]

###### 5. Width & Height
- set `width` and `height` of `container` class to `480px` and `320px` in order.
- it should look a little bit different from the previous one.

![[width-and-height.png]]

>Hint: [[CSS#Width & Height]]

###### 6. Margin & Padding
- set `margin` and `padding` in `body` to `0`.
- in `<h1>`,`<p>`,`<a>`, and `<span>` add `maring: 0;` and `padding: 10px;`

>Tip: You can specify the same values to multiple tags or set all tags at once.
```css
/* Set h1, p, a, and span font-size at once */
h1, p, a, span {
  font-size: 16px;
}

/* Set all tags color at once */
* {
  color: #A4A4A4;
}
```

>Beware: The difference between `h1, p, a, span` and `h1 p a span` is splitting with `,` which means multiple selecting, while white space means specific selector.

- add `padding` to `container` class `20px`.
- it should look a little bit bigger because of `padding: 10px`.
- and have space around with `maring: 10px`.
- add shorthand `margin` (2 params) by set top and bottom to `60px`, left and right to `auto` inside `container` class.

![[margin-and-padding.png]]

>Hint: [[CSS#Margin]], [[CSS#Padding]]

###### 7. Border
- from the previous `box` add `border` with shorthand syntax `2px`, `solid`, and `greenyellow`
- add `border-radius` to `20px`.
- change `height` to `fit-content`.

![[border-and-border-radius.png]]

>Hint: [[CSS#Border]]

###### 8. Display
- add the following HTML inside the `container` class under the rest.
```html
<div class="simple-display">
  <h2>simple display</h2>
  Lorem ipsum, dolor sit amet consectetur adipisicing elit. Dolor nulla ipsum id.
  <div class="box block">Block</div>
  Lorem ipsum dolor sit amet consectetur adipisicing elit. Nobis.
  <div class="box inline">Inline</div>
  Lorem ipsum dolor sit amet consectetur adipisicing elit.
  <div class="box inline-block">Inline Block</div>
  Lorem ipsum, dolor sit amet consectetur adipisicing elit. Optio, repellendus laboriosam.
</div>
```
- custom `simple-display` class by order:
	- set `text-align` to center to apply all text inside it align center.
	- transform all text inside it to `capitalize`.
	- make `font-bariant` to small caps.
	- finally, set line height to `30px`.
- select all `.box` class inside `simple-display` class to apply these properties:
	- width and height to `100px` and `50px` by sequence.
	- `10px` for margin and padding.
	- set text inside the box to `white`.
- set each box to the following:
	- display `block` with background color `#3498db`.
	- display `inline` with background color `#2ecc71`.
	- display `inline-block` with background color `#e74c3c`.

If you follow the assignment correctly, the final results should be something like the pic below.
![[simple-display.png]]

After you are satisfied with your result try to add `display: none;` inside `simple-display`.

>Hint: [[CSS#Display]]

###### 9. Position
- first of all, remove `display: none;` inside `simple-display` to make the content longer with cool styling.
- add `<div>` class `relative` with `<h2>`(Relative Position) and `<p>`(10 lorem words, `lorem10` then press enter) inside.
- add the following styles sequentially:
	- position `relative`.
	- background color `#3498db`.
	- margin top `100px`.
	- padding `10px`.
	- bottom `50px`.
	- make `h1` and `p` text to `white`.
- from the previous `wrapper` class, add `position: fixed;` and set `top: 0;` and `right: 0;`.
- add `<div>` class `absolute` with text "Absolute Positioning" inside `relative` class between `<h1>` and `<p>`, then styling it following:
	- position `absolute`.
	- background color `#dddd50`.
	- top `10px` and right `10px`.
	- padding `10px`.
- add `<div>` class `sticky` with text "Sticky Positioning" inside `container` between `<h1>` and `<p>`, then styling it following:
	- position `sticky`.
	- background color `#2ecc71`.
	- top and padding `10px`.
- add `<div>` class `fixed` with text "Fixed Positioning" inside `container` under the rest, then styling it following:
	- position `fixed`.
	- background color `#e74c3c`.
	- width to `160px` and text align to center.
	- top and padding to `10px`. 
	- right with calculate value `calc(50% - 240px)`.

scrolling into the bottom and you should match the results.
![[simple-positioning.png]]

>Hint: [[CSS#Position]]

These CSS properties and values are just a simple demonstration. Keep in mind, that you still require more practice to get to the next level.


#css #phase-1 #assignment #css-properties-and-values