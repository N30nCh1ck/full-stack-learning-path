Learning about HTML tags is simple. All you have to do is just know the name of HTML tag and place it somewhere you can see the result of how it works and write in the right syntax. This lesson is going to guide you through most used HTML tags that you should know, which is enough for developing most websites these days.

First of all, adding this `styles.css` file for clear results from your HTML structures.
```css
body {
  font-family: "Roboto", sans-serif;
  width: 100%;
  min-height: 100vh;
  margin: 0;
  padding: 0;
}

.container {
  width: 100%;
  max-width: 800px;
  margin: 30px auto;
  color: #333;
}

a {
  text-decoration: none;
}

section,
article,
form,
.video,
.audio,
.youtube {
  margin: 50px auto;
}

article,
form {
  width: 300px;
}

label {
  display: block;
  margin-bottom: 5px;
}

input {
  width: 100%;
  padding: 8px;
  margin-bottom: 15px;
  box-sizing: border-box;
}

button {
  background-color: #4caf50;
  color: white;
  padding: 10px 15px;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

button:hover {
  background-color: #45a049;
}

button:active {
  transform: scale(0.98);
}

table {
  width: 100%;
  margin: 20px 0;
  border-collapse: collapse;
}

th,
td {
  border: 1px solid #ddd;
  padding: 8px;
  text-align: left;
}

th {
  background-color: #f2f2f2;
}

tr:hover {
  background-color: #f5f5f5;
}
```

###### 1. Heading and Paragraph
- create HTML template and add `styles.css` above.
- add `<div>` tag with `class="container"`.
- add `<h1>` and `<p>` inside `<div class="container">`.
![[division-heading-paragraph.png]]
Your results should be like the picture above or something like that.

>Tip: If you want the paragraph text like above, in the VS Code you can try to type "lorem10" and then enter or other numbers for short or long length.

>Hint: [[HTML#Division and Paragraph]], [[HTML#Heading]]

###### 2. Text Wrapper
- add `<article>` under heading and paragraph (from the previous step).
- inside the `<article>` add `<p>` with `<span>` to make the "blue" word is blue like the picture below.
- the next line add `<p>` again with `<strong>` tag to wrap the word "Important:".
- another line add `<p>` with `<em>` tag to wrap the word "Emphasized".
- the last one add `<pre>` which wraps the paragraph with line breaks.
```
	This is preformatted text.
	It preserves spaces and line breaks.
```

![[text-wrapper.png]]

>Hint: [[HTML#`<article>`]], [[HTML#Text Wrapper]]

###### 3. Image and Its Link
- wrap image with `<figure>` and use `<figcaption>` for the description under the `<article>`.
- use this image URL `https://i.ibb.co/Q9TjJNq/neon-chick.png` for `<img src="" >`.
- use anchor tag (`<a>`) inside `<figcaption>` to open the image URL in a new tab.
- wrap the whole text inside `<a>` with `<strong>` to make it important words and inside `<strong>` add text "N30nCh1ck".
- wrap the word "Ch1ck" with `<span>` and make it as `gold` color.
- try to click on "N30nCh1ck". It should navigate you to another tap and show you where the image is.
![[image-with-its-link.png]]
This is what the results should be if you do it correctly.

>Hint: [[HTML#`<figure>` and `<figcaption>`]], [[HTML#Anchor]], [[HTML#Text Wrapper]]

###### 4. List Items
- add `<section>` below `<figure>` in `<section>` add both order list (`<ol>`) and unorder list (`<ul>`) items with heading and paragraph following the picture.
![[order-and-unorder-list.png]]

>Hint: [[HTML#Heading]], [[HTML#Ordered and Unordered with Item]]

###### 5. Form Submit
- under the previous `<section>` add `<form>` that contain`<label>`, `<input>`, and `<button>` inside.
- prevent reload the page after click "Submit" button with inline JavaScript code.
- don't forget to add heading such "Login" inside the `<form>`
![[form-submit.png]]

>Hint: [[HTML#Heading]], [[HTML#Form Input]]

###### 6. Simple Table
- create simple table under `<form>` by using `<table>`, `<tr>`, `<th>`, and `<td>` following the reference. and make sure your results match with the picture.
![[simple-table.png]]

>Hint: [[HTML#Simple Table]]

###### 7. Display Media
- download 2 following files from and then add them into your project directory
	- https://drive.google.com/file/d/1GorXjInNDHSAP06KPEYWTM0NLyqY9pDm/view?usp=drive_link
	- https://drive.google.com/file/d/1mHANs36xubAikTiahHH9TK-_jXQHkGof/view?usp=drive_link
- add `<div>` tag with `class="video"` under the `<table>`. inside `<div class="video">` add heading and video with the `.mp4` file you just downloaded.
- add `<div>` tag with `class="audio"` under the `<div class="video">`. inside it, add heading and audio with the `.mp3` file you just downloaded.
- add `<div>` tag with `class="youtube"` under the `<div class="audio"`. inside it, add heading and `<iframe>` that call YouTube embedded video.
- check the results are matched with the picture below.
![[video-audio.png]]

For YouTube embedded video, you cannot open it in your local environment. Thus, just make sure the results of your screen are matched with the picture.
![[embed-youtube.png]]

>Hint: [[HTML#Media]]


#html #phase-1 #assignment #most-used-html 