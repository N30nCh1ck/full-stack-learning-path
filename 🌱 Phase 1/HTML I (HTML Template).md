Create a default HTML template in VS Code. run your code and try to change the title tab to `HTML 101` as the picture below.

![[html-101.png]]

>Hint: [[HTML#!DOCTYPE]]

When you've done. Let's add some JavaScript code by using inline script to alert "Hello, World!"

![[hello-world-html-js.png]]

And then try to split your inline JavaScript code to external file `script.js` and import it into your `index.html` file. Click the button and check your code still work fine.

>Hint: [[HTML#1. `<script>` Tag]]

Decorate your html code by using inline CSS to change the `background-color: skyblue;` like this:

![[bg-skyblue.png]]

>Hint: [[HTML#2. `<style>` Tag]]

Move your inline CSS code to external `styles.css` file and link it to `index.html` file. After that update your `styles.css` to the following code:
`styles.css`
```css
body {
  background-color: skyblue;
  font-family: Arial, sans-serif;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  width: 100vw;
  height: 100vh;
}

button {
  outline: none;
  border: 1px solid #000;
  border-radius: 10px;
  padding: 10px;
}

button:hover {
  cursor: pointer;
  border: 2px solid lightblue;
}
```

>Hint: [[HTML#3. `<link>` Tag]]

![[greetings-html-101.png]]
Finally, what you have to do is just write HTML code and make it display as same as possible the picture above. You can simply finish this by following the last 3 hints previously.
