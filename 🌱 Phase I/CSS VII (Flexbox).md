>**Ref:** [[CSS#Flexbox]]

###### Flex Container
- follow the **Hint** example and try to get result like the image below

>**Hint:** [[CSS#Flex Container]]

![[flex-container.png]]

**HTML Components**
- `<h1>` with text "Flex Container"
- `<p>` with text `lorem10`
- `<div>` with class `flex-container`
	- inside contain `<div>` with class `flex-item`
- `<span>` with text `lorem6`
- `<div>` with class `inline-flex-container`
	- inside container `<div>` with class `flex-item` 
- pure text `lorem8`

**CSS Components**
- `body`
	- font size `18px`
	- line height `30px`
	- font family `cursive`
	- padding `20px`
	- margin `0`
	- box sizing `border-box`
- `flex-container`
	- display `flex`
	- padding and margin `10px`
	- border `2px solid darkcyan`
	- border radius `20px`
- `inline-flex-container`
	- display `inline-flex`
	- padding and margin `10px`
	- border `2px solid darkcyan`
	- border radius `20px`
- `flex-item`
	- padding `10px`
	- margin `5px`
	- font weight `bold`
	- color `darkcyan`
	- background color `lightcyan`

###### Flex Flow
- add the follow "Flex Flow" section under "Flex Container"

>**Hint:** [[CSS#Flex Flow]]

![[flex-flow.png]]

**HTML Components**
- `<h1>` with text "Flex Flow"
- `<div>` with classes `flex-container` and `flex-flow`
	- inside contain `<div>` with classes `flex-item` and `flex-flow-item`

**CSS Components**
- the same class name use as the same as the previous assignment
- `flex-flow` row and wrap
- `flex-flow-item` 
	- width and height `100px`
	- margin `10px`

###### Flex Order
- custom the previous assignment (Flex Flow) to the following

>**Hint:** [[CSS#Flex Order]]

![[flex-order.png]]

**HTML Components**
- `<h1>` with text "Flex Flow & Flex Order"
- inside `<div>` with classes `flex-container` and `flex-flow`
	- add class `order-n` to each item

**CSS Components**
- set `order-n` such as `order-1` set to `order: 1`

###### Flex Alignment

>**Ref:** [[CSS#Flex Alignment]]

**Justify Content**
- mock the following image by the "Hint" and "Components"

>**Hint:** [[CSS#Justify Content]]

![[justify-content.png]]

**HTML Components**
- `<h1>` with text "Flex Alignment" (which not show on the image, but you must add)
- `<section>` use to wrap everything
	- `<h2>` with text "Justify Content"
	- `<span>` with text "space between"
	- `<div>` with classes `flex-container` and `space-between`
		- inside contain `<div>` with class `flex-item` (3 items)
	- `<span>` with text "space around"
	- `<div>` with classes `flex-container` and `space-around`
		- inside contain `<div>` with class `flex-item` (3 items)
	- `<span>` with text "space evenly"
	- `<div>` with classes `flex-container` and `space-evenly`
		- inside contain `<div>` with class `flex-item` (3 items)
	- `<span>` with text "flex center"
	- `<div>` with classes `flex-container` and `flex-center`
		- inside contain `<div>` with class `flex-item` (3 items)
	- `<span>` with text "flex start"
	- `<div>` with classes `flex-container` and `flex-start`
		- inside contain `<div>` with class `flex-item` (3 items)
	- `<span>` with text "flex end"
	- `<div>` with classes `flex-container` and `flex-end`
		- inside contain `<div>` with class `flex-item` (3 items)

**CSS Components**
- `h2` text align `center` font size `18px`
- `space-between` set justify content to `space-between`
- `space-around` set justify content to `space-around`
- `space-evenly` set justify content to `space-evenly`
- `flex-center` set justify content to `center`
- `flex-start` set justify content to `flex-start`
- `flex-end` set justify content to `flex-end`

**Align Items**
- mock the following image by the "Hint" and "Components"

>**Hint:** [[CSS#Align Items]]

![[align-items.png]]

**HTML Components**
- `<h2>` with text "Align Items"
- `<div>` with classes `flex-row` and `space-evenly` and contains
	- `<div>` with class `flex-col` and contains
		- inside contain `<span>` with text "items center"
		- `<div>` with classes `flex-box` and `items-center` and contain
			- `<div>` with class `flex-item`
	- `<div>` with class `flex-col` and contains
		- inside contain `<span>` with text "items start"
		- `<div>` with classes `flex-box` and `items-start` and contain
			- `<div>` with class `flex-item`
	- `<div>` with class `flex-col` and contains
		- inside contain `<span>` with text "items end"
		- `<div>` with classes `flex-box` and `items-end and contain
			- `<div>` with class `flex-item`

**CSS Components**
- `flex-row` display `flex` with flex direction `row`
- `flex-col` display `flex` with flex direction `column`
- `flex-box`
	- display `flex`
	- height `150px`
	- padding and margin `10px`
	- border `2px` `solid` `darkcyan`
	- border radius `20px`
- `items-center` set align items to `center`
- `items-start` set align items to `flex-start`
- `items-end` set align items to `flex-end`

**Align Content**
- mock the following image by the "Hint" and "Components"

>**Hint:** [[CSS#Align Content]]

![[align-content.png]]

**HTML Components**
- `<h2>` with text "Align Content"
- `<div>` with class `flex-row-wrap` 
	- `<article>` which contains
		- `<span>` with text "content between"
		- `<div>` with classes `flex-box-content` and `content-between`
			- `<div>` with classes `content-item`
	- `<article>` which contains
		- `<span>` with text "content around"
		- `<div>` with classes `flex-box-content` and `content-around`
			- `<div>` with class `content-item` (3 items)
	- `<article>` which contains
		- `<span>` with text "content evenly"
		- `<div>` with classes `flex-box-content` and `content-evenly`
			- `<div>` with class `content-item` (3 items)
	- `<article>` which contains
		- `<span>` with text "content center"
		- `<div>` with classes `flex-box-content` and `content-center`
			- `<div>` with class `content-item` (3 items)
	- `<article>` which contains
		- `<span>` with text "content start"
		- `<div>` with classes `flex-box-content` and `content-start`
			- `<div>` with class `content-item` (3 items)
	- `<article>` which contains
		- `<span>` with text "content end"
		- `<div>` with classes `flex-box-content` and `content-end`
			- `<div>` with class `content-item` (3 items)

**CSS Components**
- `flex-row-wrap` display `flex` and flex flow `row` and `wrap`
- `flex-box-content` 
	- display `flex` 
	- flex wrap `wrap`
	- width and height `300px`
	- padding and margin `10px`
	- border `2px` `solid` `darkcyan`
	- border radius `20px`
- `content-item`
	- width `100px` and height `50px`
	- padding `10px` and margin `5px`
	- font weight `bold`
	- color `darkcyan`
	- background color `lightcyan`
- `content-between` set align content to `space-between`
- `content-around` set align content to `space-around`
- `content-evenly` set align content to `space-evenly`
- `content-center` set align content to `center`
- `content-start` set align content to `flex-start`
- `content-end` set align content to `flex-end`

**Align Self**
- mock the following image by the "Hint" and "Components"

>**Hint:** [[CSS#Align Self]]

![[align-self.png]]

**HTML Components**
- `<h2>` with text "Align Self"
- `<div>` with classes `flex-row` and `flex-center`
	- `<div>` with classes `flex-row-wrap`, `align-self-box` and `flex-center`
		- `<div>` with classes `box-item` and `self-stretch` and text "self stretch"
		- `<div>` with classes `box-item` and `self-center` and text "self center"
		- `<div>` with classes `box-item` and `self-start` and text "self start"
		- `<div>` with classes `box-item` and `self-end` and text "self end"

**CSS Components**
- `align-self-box`
	- width and height `300px`
	- border `2px solid darkcyan`
	- border radius `20px`
- `box-item`
	- width `100px`
	- font weight `bold`
	- padding and margin `10px`
	- color `darkcyan`
	- background color `lightcyan`
- `self-stretch` set align self to `stretch`
- `self-center` set align self to `center`
- `self-start` set align self to `start`
- `self-end` set align self to `end`

>**Note:** You cannot use `align-self` when the parent element uses `align-items` or `align-content`. Otherwise, the `align-self` property on children's elements will break.

###### Miscellaneous
- mock the following image by the "Hint" and "Components"

>**Hint:** [[CSS#Flex Miscellaneous]]

![[flex-miscellaneous.png]]

**HTML Components**
- `<h1>` with text "Miscellaneous"
- `<section>` use to wrap everything about flex miscellaneous
	- `<p>` with `<strong>` inside then follow by text " (it grows by space and total ratio)" 
		- `<strong>` with text "flex grow:"
	- `<div>` with class `flex-container`
		- `<div>` with class `flex-item`, and text "Grow 0"
		- `<div>` with class `flex-item`, style `flex-grow: 5`, and text "Grow 5/7"
		- `<div>` with class `flex-item`, style `flex-grow: 2`, and text "Grow 2/7"
	- `<p>` with `<strong>` inside then follow by text " (it shrinks related by flex basis and total ratio)" 
		- `<strong>` with text "flex shrink:"
	- `<div>` with class `flex-container`
		- `<div>` with classes `flex-item`, `grow`, `basis`, and text "Grow 100%"
		- `<div>` with classes `flex-item`, `grow`, `basis`, style `flex-shrink: 7`, and text "Shrink 7/10"
		- `<div>` with classes `flex-item`, `grow`, `basis`, style `flex-shrink: 3`, and text "Shrink 3/10"
	- `<p>` with `<strong>` inside then follow by text " (flex basis is the default size before it grows)" 
		- `<strong>` with text "flex basis:"
	- `<div>` with class `flex-container`
		- `<div>` with classes `flex-item` and `basis`, and text "Basis 300px"
		- `<div>` with class `flex-item`, and text "No Basis"
		- `<div>` with class `flex-item`, and text "No Basis"

**CSS Components**
- `grow` class set to `flex-grow: 1`
- `basis` class set to `flex-basis: 300px`

>**Note:** You can use `flex-grow: 1`, `flex-shrink: 0`, and `flex-basis` by the following shorthand `flex: 1 0 300px`


#css #phase-1 #assignment #flexbox 