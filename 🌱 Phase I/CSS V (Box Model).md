>**Ref:** [[CSS#Width & Height]], [[CSS#Padding]], [[CSS#Border]], [[CSS#Margin]], [Learn CSS Box Model In 8 Minutes](https://www.youtube.com/watch?v=rIO5326FgPE) 

**Default Template**
- create a new directory with name `box-model` to separate your HTML and CSS files.
- create a new HTML template with the title `Box Model` and link the CSS file for styling later.

Try this shorthand key in your VS Code then press enter.
![[html-class-shorthand-1.png]]
Or you can create multiple classes with:
![[html-class-shorthand-2.png]]

>**NOTE:** Everything in CSS is a box, either a rectangular shape or a square shape

- add `<div>` with `box`, `box-red` classes and text "red"
- and `<div>` with `box`, `box-blue` classes and text "blue"
- set  `padding` and `margin` to `0` inside `body`
- for `box` set font size `40px`, `bold`, `capitalize`, and `small-caps`
- set background color for `box--red` to `#f15959` and `box--blue` to `#5353f8`

![[red-blue-boxes.png]]

- to make the `box--red` is bigger, add `padding: 20px`
	- add space with `margin: 50px`
	- add border `#eeda68`, `solid`, and `30px`
	- press `Ctrl` + `Shift` + `C` then press on the **RED** box

![[Pasted image 20231212215624.png]]

Click on the `Computed` tab, the box details appear here. The deepest area is a **Content Area** which specifies width and height.
- try to custom width and height to `200px` and `100px` in order. the **Content Area** will be `200x100` instead.

>This custom is a default `box-sizing: content-box` which means the `width` and `height` are affected only **Content Area** when you specify values.

- for the `box--blue`, let's make it:
	- bigger by `padding: 20px`
	- add border `#23c93f`, `solid`, and `30px`
	- finally, add `margin: 50px` then see the result

![[Pasted image 20231212221455.png]]

When you hover on the `box--blue` margin look not correctly. That's because in the **Box Model** `margin` collapses between two element that are next to each other.

>Keep in mind, in the **Box Model** `margin` collapses each other.

- inside `box--blue` add the following:
	- set width and height to `200px` and `100px` in order
	- set `box-sizing` to `boder-box`

![[Pasted image 20231212222908.png]]

As you see, the `box--blue` looks smaller. That's because when you set `width` and `height` in the box that specify `box-sizing: border-box`, it includes `padding` and `border` with the **Content Area**. 

> Currently, your **Content Area** can no longer be smaller (because it's `0` already).

**Challenge**
- try to add `padding` that makes the text **BE** inside the **BLUE** background then **OBSERVE** the **Content Area**, `padding`, and `border` carefully.

>**Hint:** Your `box--blue` are set to `box-sizing: boder-box` and `height: 100px`

![[Pasted image 20231212225712.png]]

The theory tell you `box-sizing: border-box` will be count **Content Area**, `padding`, and `border` as your `height` (and `width`). That's why your `height` automatically scales up to `160px` immediately.

**Screen Overflow**
- add `width` and `height` to `100vw` and `100vh` sequentially in your `body` 

![[Pasted image 20231212230559.png]]

What's going on? How do `width` and `height` scrollbars happen?

That's because your `box-sizing` automatically is `content-box` and all childe's `margin` are not included in your specified sizes (width and height).

>**NOTE: Try to fix this issue by yourself**

###### Answer
%% 
Fixing this issue is pretty challenging for beginners. So, just follow the way if you don't want to challenge yourself:

- add `box-sizing: border-box;` and add padding 1px or more in `body`

By following the way above, the issue should be gone.
%%

#css #phase-1 #assignment #box-model 
