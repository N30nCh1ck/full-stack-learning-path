>Ref: [[CSS#Example CSS Function]]

###### RGB & RGBA
- create `container` class and styling it following:
	- width `600px` and height auto.
	- margin `50px`top and bottom and leave the rest to `auto`.
	- set background color to `#f8f8f8`.
- create 3 boxes inside `container` in different colors both text and background by using `rgb` and `rgba` functions:
	- for each `box` 
		- display `inline-block`
		- padding and margin `20px`
		- width and height `100px` and `50px` sequentially.
		- transform text to `uppercase` and make it `bold`.
		- border radius `10px`.

![[3-color-boxes.png]]

>Hint: [[CSS#RGB & RGBA]]

###### HSL & HSLA
- from the previous section, change `rgb` and `rgba` to `hsl` and `hsla` by order.

![[tip-change-color-format.png]]

>Tip: You can change `rgb` to `hsl` easily by hovering at `arrow 1` and clicking on `arrow 2`.

>Hint: [[CSS#HSL & HSLA]]

###### CALC
- set `container` height to `200px`.
- make the `container` stay in the middle of the page by using only shorthand `maring` for details:
	- equal distance from top and bottom.
	- equal distance from left and right.

You can use `calc()` to calculate device height and `container` height to make it stay in the middle vertically.
![[calc-height-with-margin.png]]

>Hint: [[CSS#CALC]]

###### VAR
- add `--container-height: 200px` variable inside the `:root` and use it in `container` class.
- change some other plain values to CSS variables with new value:
	- `--container-width: 610px`
	- `--box-width: 120px`
	- `--box-margin: 55px 20px`

If you follow the assignment properly you results should look like this.
![[using-css-var.png]]

>Hint: [[CSS#VAR]]

###### Linear Gradient
- change background color to background `linear-gradient` like picture below.
	- red box colors: `#e08e58` and `#b11414`.
	- green box colors: `#ade01f` and `#0c6d0c`.
	- blue box colors: `#19afdd` and `#05117c`.
- don't forget to change the text color to `white`.

![[linear-gradient-box.png]]

> Hint: [[CSS#Linear Gradient]]

###### Radial Gradient
- add elliptical gradient in `container` with the following colors `#e08e58`, `#ade01f`, and `#19afdd`.
- and add border radius `20px` to top right and bottom left.

![[bg-radial-gradient.png]]

>Tip: When using `border-radius`, you can use shorthand for each angle by the following in order `border-radius: [top-left] [top-right] [bottom-right] [bottom-left].

>Hint: [[CSS#Radial Gradient]]

###### URL
- add variable `--bg-url: url("https://i.ibb.co/hVw9D4C/pexels-photo-620337.jpg")`.
- inside `body`, use shorthand background to custom following styles:
	- image call `--bg-url`
	- repeat to `no-repeat`
	- attachment to `fixed`
	- position to `center`
- add `background-size` to `cover` inside the `body`.
- finally, add `opacity: 0.4` to `container`.

Do you get something like this?
![[url-bg-image.png]]

>Hint: [[CSS#URL]]

###### Transform
- add `cursor: pointer` to `box` class.
- for the `red` box:
	- create pseudo-class `:hover` and set `transform: rotate(45deg)`
	- create pseudo-class `:active` and set `transform: rotate(45deg) scale(0.98)`
- for the `green` box:
	- create pseudo-class `:hover` and set `transform: skew(5deg, 5deg)
	- create pseudo-class `:active` and set `transform: skew(-5deg, -5deg)`
- for the `blue` box:
	- create pseudo-class `:hover` and set `transform: translate(10px, 20px)
	- create pseudo-class `:active` and set `transform: translate(10px, 20px) rotate(180deg)
- remove `opacity` in `container` and the following instead:
```css
/* Using alpha in color instead of opacity */
.container {
  ...
  /* opacity: 0.4; should be removed */
  background: radial-gradient(
    ellipse at center,
    hsla(24, 69%, 61%, 0.4), /* alpha 0.4 */
    hsla(76, 76%, 50%, 0.4), /* alpha 0.4 */
    hsla(194, 80%, 48%, 0.4) /* alpha 0.4 */
  );
  
  /* Prevent User Select Text */
  user-select: none; 
  -webkit-user-select: none; /* For older versions of Safari and Chrome */
  -moz-user-select: none; /* For Firefox */
  -ms-user-select: none; /* For Edge */
}
```

>Hint: [[CSS#Transform]]

###### ATTR
- change `<div class="container">` to `<div class="container" data-text="👻👻👻">`.
- create `container` selector with pseudo-element `::before` then style it following:
	- add position `absolute` (also add position `relative` in `container`)
	- set `content` to `attr(data-text)` ("👻👻👻")
	- add padding `20px`
	- create `@keyframe` fadeInOut and add `animation: fadeInOut 4s ease-in-out infinite;`
```css
@keyframes fadeInOut {
  0% {
    opacity: 0;
    right: 0;
    top: 0;
  }
  50% {
    opacity: 1;
    left: 40%;
    top: 50%;
  }
  100% {
    opacity: 0;
    bottom: 0;
    left: 0;
  }
}
```

>Hint: [[CSS#ATTR]]

###### Clamp
- add `<h1>` on top of `container` class with text "CSS Functions"
- styling `<h1>` by following:
	- position `fixed`
	- top `50px` and left `50%`
	- width `300px` and padding `10px`
	- translate itself 50% of x axis to left, `translateX(-50%)`
	- text align center and font family `cursive`
	- finally, set `font-size` by using `clamp()` by:
		- use a minimum font size of `18px`
		- use a preferred font size of 8% of the viewport width `vw`
		- use a maximum font size of `32px`

Your results are likely the picture below. Try to change device screen and *inspect* font size of `<h1>`. This is the easiest way to create a responsive font size.
![[clamp-responsive-font.png]]

>Hint: [[CSS#Clamp]]


#css #phase-1 #assignment #css-functions 