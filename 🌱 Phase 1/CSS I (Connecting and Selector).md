There are 3 ways to connect CSS to HTML you should know (or not necessary?) before going to the Selector lesson by following the reference.

>Ref: [[CSS#Connecting CSS to HTML]]

First of all, you have to add `index.html` below to see how the CSS selector works.
```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>CSS Selector Examples</title>
    <link rel="stylesheet" href="styles.css" />
  </head>
  <body>
    <p>This is a paragraph with the Element Selector.</p>
    <p class="highlight">This is a paragraph with the Class Selector.</p>
    <p>A first line is bigger and bold. Lorem ipsum dolor sit amet.</p>
    <p>All paragraphs have a "Note: " prefix with lightgray color</p>
    <div>
      <span
        >&lt;span&gt;This span is selected using the "Descendant
        Selector".&lt;span&gt;</span
      >
	    <div><span>test</span></div>
    </div>
    <h2 id="header">Header with ID</h2>
    <p>
      This underlined paragraph is affected by the Adjacent Sibling Selector.
    </p>
    <ul>
      <li>List item 1</li>
      <li class="highlight">List item 2 (even) with Class Selector</li>
      <li>List item 3</li>
      <li class="highlight">List item 4 (even) with Class Selector</li>
    </ul>
    <p>
      Another paragraph with the General Sibling Selector are
      <a href="#" target="_self">Italic</a>.
    </p>
    <p>
      Styling the first line of All paragraph using the Pseudo-element Selector.
    </p>
    <div>
      <p>Should be not Italic by General Sibling Selector</p>
      <ul>
        <li>List item 1<span>test</span></li>
        <li class="highlight">List item 2 (even) with Class Selector<span>test</span></li>
        <li>List item 3</li>
        <li class="highlight">List item 4 (even) with Class Selector</li>
      </ul>
    </div>
    <input type="text" />
  </body>
</html>
```
Then start your `styles.css` file with the following code:
```css
body {
  margin: 20px auto;
  max-width: 300px;
}
```

###### 1. Element Selector
Make all `<p>` is blue and set `width` to `300px`.

>Hint: [[CSS#Element Selector]]

###### 2. Class Selector
Highlight the `<p>` with `class="highlight"` by set `background-color` to `yellow`.

>Hint: [[CSS#Class Selector]]

###### 3. ID Selector
Change `<h2>` color to `purple` and set `font-size` to `32px`.

>Hint: [[CSS#ID Selector]]

###### 4. Attribute Selector
Select `<a>` with attribute `target` then set `text-decoration` to `none` and select `<input>` with attribute `type="text"` then set `border`, `border-radius`, and `padding`.

>Hint: [[CSS#Attribute Selector]]

###### 5. Descendant Selector
Change text color of `<span>` inside `<div>` to `#424242` and set `font-weight` to `bold`.

>Hint: [[CSS#Descendant Selector]]

###### 6. Child Selector
Make the bullet of the `<li>` list inside `<ul>` from circle to square.

>Hint: [[CSS#Child Selector]]

###### 7. Adjacent Sibling Selector
Apply the `underline` to only `<p>` adjacent with `<h2>` by using `text-decoration`.

>Hint: [[CSS#Adjacent Sibling Selector]]

###### 8. General Sibling Selector
Change `font-style` to `italic` all of `<p>` under `<h2>`.

>Hint: [[CSS#General Sibling Selector]]

###### 9. Pseudo-class Selector
When hover the link (`<a>`) make the text `underline`, `bold`, and `blue`. And make background color of `<li>` inside `<ul>` that be even sequence line to `#f0f0f0`.

>Hint: [[CSS#Pseudo-class Selector]]

###### 10. Pseudo-element Selector
Make every `first-line` of `<p>` is bold and bigger by set `font-size` to `18px`. After that, add prefix "Note: " to every `<p>` with `lightgray` color.

>Hint: [[CSS#Pseudo-element Selector]]

After finish all of selector assignment. The results of your assignment should be something like this.
![[css-selector-results.png]]

Try to understand how the CSS selector works and how it write in the right syntax.


#css #phase-1 #assignment #connecting-css #css-selector