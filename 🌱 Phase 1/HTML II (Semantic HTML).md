In this lesson, we are gonna learn the semantic HTML that you should know step by step. But before you go to survey this lesson. You have to add this `semantic.css` file first. You don't need to understand the CSS code because we gonna focus on semantic HTML tags only. Thus, just copy and paste it into your work directory.

```css
body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

header {
  background-color: #333;
  color: #fff;
  padding: 10px;
  text-align: center;
}

nav ul {
  list-style: none;
  padding: 0;
  margin: 0;
}

nav li {
  display: inline;
  margin-right: 20px;
}

nav a {
  text-decoration: none;
  color: #fff;
}

main {
  max-width: 800px;
  height: 100%;
  min-height: 70vh;
  margin: 20px auto;
  padding: 20px;
  background-color: #f8f8f8;
}

section {
  margin-bottom: 20px;
}

article {
  border: 1px solid #ddd;
  padding: 10px;
  margin-bottom: 20px;
}

aside {
  position: fixed;
  top: 50%;
  left: 0;
  transform: translateY(-120px);
  width: 120px;
  background-color: #f8f8f8;
  padding: 10px;
  text-align: center;
}

details {
  border: 1px solid #ddd;
  padding: 10px;
}

summary {
  cursor: pointer;
}

figure {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  margin: 0;
  padding: 0;
}

figcaption {
  padding-top: 10px;
  font-size: 12px;
}

img {
  width: 100px;
  height: auto;
}

footer {
  background-color: #333;
  color: #fff;
  text-align: center;
  padding: 5px;
  position: fixed;
  bottom: 0;
  width: 100%;
}
```

###### 1. Create HTML Template
>Hint: [[HTML#!DOCTYPE]]

###### 2. Add Header Tag
In `index.html` file you just created. add the following code inside the `<body> ... </body>` and see the result.
```html
...
  <header>
    <h1>Semantic HTML 101</h1>
  </header>
...
```

>Hint: [[HTML#`<header>`]]
###### 3. Add Footer Tag
The `<footer>` is one of the most important tag in your website. Add it with a copy right text below `<header>` tag and see what happen.
```html
...
<footer>
  <p>&copy; 2023 Your Website Name. All rights reserved.</p>
</footer>
```

>Hint: [[HTML#`<footer>`]]

###### 4. Add Main & Section
Try to add `<main>` tag between `<header>` and `<footer>` inside the `<main>` tag add `<section>` with some heading and paragraph.

>For semantic reason you must use `<h2>` tag instead of `<h1>`, because the H tag in this situation have 2 levels deep (main -> section)

>Hint: [[HTML#`<main>`]], [[HTML#`<section>`]]

###### 5. Add 2 Articles
Adding 2  `<article>` inside `<section>`, which your `<article>` must contain both heading and paragraph. Consider which H tag you should use for semantic reasons too.

Below the `<article>` tag add `<details>` and `<summary>` with some paragraph.

>Hint: [[HTML#`<article>`]], [[HTML#`<details>` and `summary`]]

###### 6. Time and Mark
Go to the paragraph inside the `<section>` tag under the `<p>` tag add the following code:
```html
...
<p>
  <mark>End of Year:</mark>
  <time datetime="2023-12-31">December 31, 2023</time>
</p>
...
```

>Hint: [[HTML#`<time>`]], [[HTML#`<mark>`]]

###### 7. Aside with Advertisement
The simplest way to explain `<aside>` (including `<figure>` and `<figcaption>`) tag is the advertisement. Add the following code of `<aside>` below the `<section>` tag inside `<main>`.
```html
...
<aside>
  <h2>Aside Left</h2>
  <p>N30nCh1ck</p>

  <figure>
    <img src="https://i.ibb.co/Q9TjJNq/neon-chick.png" alt="neon-chick" />
    <figcaption>Advertisement</figcaption>
  </figure>
</aside>
```

The code above contain both `<figure>` and `<figcaption>` inside the `<aside>` which is the example of how to wrap the `<img>` tag in a semantic way.

>Hint: [[HTML#`<aside>`]], [[HTML#`<figure>` and `<figcaption>`]]

After you finish all assignment, the result should be something like the picture below.
![[semantic-html-webpage.png]]
the whole lesson above is the most used case for each semantic HTML tag. which covers enough of what you have to know.
