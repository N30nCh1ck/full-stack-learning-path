 HTML (Hypertext Markup Language) is a markup language used to structure content on the web using tags. It defines elements like headings, paragraphs, and links. These elements organize and format text, images, and multimedia for web page display.

## HTML Template
  
The `<!DOCTYPE>` declaration is an HTML document type declaration. It is not a tag or an element; rather, it is a directive that informs the web browser about the version of HTML or XML being used in a particular document. This declaration helps the browser to render the web page correctly.

###### !DOCTYPE
The `<!DOCTYPE>` declaration is placed at the very beginning of an HTML document, before the `<html>` tag. Its syntax is:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
  </head>
  <body>
    <!-- TODO -->
  </body>
</html>
```

Typically in **VS Code** when you type `!` then press *enter* you'll get the html default template above or something like that. Let's go through each tag of the provided HTML code:

>Before you go, keep in mind the "..." is *JUST* only use for abbreviation of the rest of code.

```html
<html lang="en">
  ...
</html>
```
`<html lang="en">` starts the HTML document and includes the opening `<html>` tag. The `lang="en"` attribute specifies the language of the document, which is set to English (en). while `</html>` marks the end of the HTML document. It includes the closing `</html>` tag.

```html
<head>
  ...
</head>
```
`<head>` marks the beginning of the document's head section, where meta-information about the document is placed. while `</head>` marks the end of the head section.

```html
...
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
...
```
`<meta charset="UTF-8" />` This line sets the character encoding for the document to UTF-8, which is a widely used character encoding that supports a vast range of characters from various languages. 
And this line `<meta name="viewport" content="width=device-width, initial-scale=1.0" />` sets the viewport properties for responsive web design. It ensures that the width of the page is set to the width of the device, and the initial zoom level is set to 1.0.

```html
...
  <title>Document</title>
...
```
`<title>...</title>` use to sets the title of the HTML document, which typically appears in the browser's title bar or tab.

```html
<body>
  <!-- TODO -->
</body>
```
`<body>` marks the beginning of the body section, where the content of the HTML document is placed. while `</body>` marks the end of the body section.
`<!-- TODO -->` is an HTML comment. It doesn't affect the rendering of the page and is often used to leave notes or placeholders in the code. In this case, it suggests that there's something to be done in the body of the document.

**Additionally**
There are some HTML tags that are used in `<head>...</head>` which are `<script>...</script>`, `<style>...</style>`, and `<link>`. Let's break into these html tags.

###### 1. `<script>` Tag
The `<script>` tag is used to embed or reference JavaScript code in an HTML document. It can be placed in the head or body section of the HTML document.

**Example: Inline JavaScript**
`index.html`
```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <title>JavaScript Example</title>
    <script>
      // Inline JavaScript code
      function greet() {
        alert('Hello, World!');
      }
    </script>
  </head>
  <body>
    <button onclick="greet()">Click me</button>
  </body>
</html>
```

**Example: External JavaScript File**
`index.html`
```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <title>External JavaScript Example</title>
    <script src="script.js"></script>
  </head>
  <body>
    <button onclick="greet()">Click me</button>
  </body>
</html>
```
`script.js`
```js
// External JavaScript code
function greet() {
  alert("Hello, World!");
}
```

###### 2. `<style>` Tag
The `<style>` tag is used to embed or reference CSS (Cascading Style Sheets) code in an HTML document. It is typically placed in the head section.

**Example:**
`index.html`
```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <title>CSS Example</title>
    <style>
      /* Inline CSS code */
      body {
        background-color: #f0f0f0;
        font-family: Arial, sans-serif;
      }
    </style>
  </head>
  <body>
    <h1>Welcome to my website</h1>
    <p>This is a sample paragraph.</p>
  </body>
</html>
```

###### 3. `<link>` Tag
The `<link>` tag is used to link external resources such as stylesheets or icons. It is commonly used to link external CSS files.

**Example:**
`index.html`
```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <title>External CSS Example</title>
    <link rel="stylesheet" type="text/css" href="styles.css" />
  </head>
  <body>
    <h1>Welcome to my website</h1>
    <p>This is a sample paragraph.</p>
  </body>
</html>
```
`styles.css`
```css
/* External CSS code */
body {
  background-color: #f0f0f0;
  font-family: Arial, sans-serif;
}
```

These examples showcase the basic use-cases for `<script>`, `<style>`, and `<link>` tags in HTML, illustrating how they are employed to include or reference JavaScript code, CSS styles, and external resources in a web page.

## Semantic HTML
There are the semantic elements introduced in HTML5. They provide a way to add more meaning to the structure of a web page, making it easier for both browsers and developers to understand the content.

#### `<header>`
The `<header>` tag represents introductory content or a group of introductory content. It can contain headings, logos, navigation menus, and other elements typically placed at the top of a webpage.
```html
<header>
   <h1>Page Title</h1>
   <p>Header content goes here.</p>
</header>
```

#### `<footer>`
The `<footer>` tag defines a footer for a section or a page. It often contains metadata, copyright information, links to related documents, or contact details, appearing at the bottom of the webpage.
```html
<footer>
   <p>Footer content goes here.</p>
</footer>
```

#### `<nav>`
The `<nav>` tag is used to define a section with navigation links. It typically contains a set of links to other pages, helping users navigate through the website.
```html
<nav>
   <ul>
      <li><a href="#">Home</a></li>
      <li><a href="#">About</a></li>
      <li><a href="#">Contact</a></li>
   </ul>
</nav>
```

#### `<aside>`
The `<aside>` tag represents content that is tangentially related to the content around it, such as a sidebar or a pull quote.
```html
<aside>
   <p>Related information or sidebar content goes here.</p>
</aside>
```

#### `<main>`
The `<main>` tag represents the main content of the `<body>` element in an HTML document. It excludes headers, footers, and sidebars, providing a way to identify the primary content of a page.
```html
<main>
   <h1>Main Content</h1>
   <p>Main content goes here.</p>
</main>
```

#### `<section>`
The `<section>` tag defines a section in a document, grouping together thematically related content. It helps in organizing and structuring the content on a webpage.
```html
<section>
   <h2>Section Title</h2>
   <p>Section content goes here.</p>
</section>
```

#### `<article>`
The `<article>` tag represents a self-contained piece of content that could be distributed and reused independently. It is often used for blog posts, news articles, forum posts, etc.
```html
<article>
   <h2>Article Title</h2>
   <p>Article content goes here.</p>
</article>
```

#### `<figure>` and `<figcaption>`
The `<figure>` tag represents any content that is referenced from the main content, usually with an associated caption `<figcaption>` element.
```html
<figure>
   <img src="image.jpg" alt="A description of the image">
   <figcaption>Caption for the image</figcaption>
</figure>
```

#### `<details>` and `summary`
The `<details>` tag represents a disclosure widget from which the user can obtain additional information or controls. and `<summary>` tag is a summary or a legend for a `<details>` element. 
```html
<details>
   <summary>Click to reveal more details</summary>
   <p>Additional content goes here.</p>
</details>
```

#### `<time>`
the `<time>` tag represents a specific period in time, often including a machine-readable date.
```html
<p>Event date: <time datetime="2023-12-02">December 2, 2023</time></p>
```

#### `<mark>`
The `<mark>` tag represents the main content of the document. It should be unique and not nested within other `<main>` elements.
```html
<p>This is <mark>important</mark> information.</p>
```


## Most Used HTML

#### Text and Layout
Here's an explanation of each of the HTML tags you must know along with examples:

###### Division and Paragraph
The `<div>` tag is a generic container that is often used to group together and apply styles to a block of content. and the `<p>` tag is used to define paragraphs of text.
```html
<div>
   <p>This is some content inside a div.</p>
   <p>Another paragraph inside the div.</p>
</div>
```

###### Heading
The **`<h1> to <h6>`**: Heading tags, used to define headings. `<h1>` is the largest and `<h6>` is the smallest.
```html
<h1>Main Heading</h1>
<h2>Subheading 1</h2>
<h3>Subheading 2</h3>
<h4>Subheading 3</h4>
<h5>Subheading 4</h5>
<h6>Subheading 5</h6>
```

###### Image
The `<img>` tag is used to embed images in HTML documents. It requires the `src` attribute to specify the image file's source (URL or local path).
```html
<img src="image.jpg" alt="Description of the image">
```

###### Anchor
The `<a>` tag is used to create hyperlinks. The `href` attribute specifies the URL of the linked resource.
```html
<a href="https://www.example.com">Visit Example.com</a>
```

if you want to open the link in a new tab use the `target="_blank"` attribute such as:
```html
<a href="https://www.example.com" target="_blank">Visit Example.com</a>
```

###### Text Wrapper
The `<span>` tag is an inline container that is often used to apply styles or scripting to a specific portion of text.
```html
<p>This is <span style="color: blue;">blue</span> text.</p>
```

The `<strong>` tag is used to define strong importance. Browsers usually render the text as bold.
```html
<p><strong>Important:</strong> This is a strong statement.</p>
```

The `<em>` tag is used to emphasize text. Browsers typically render the text in italics.
```html
<p><em>Emphasized</em> text is often displayed in italics.</p>
```

The `<pre>` tag defines preformatted text. It preserves both spaces and line breaks.
```html
<pre>
   This is preformatted text.
   It preserves spaces and line breaks.
</pre>
```
 
>These tags wrapper provide structural meaning to the content and help browsers and developers understand the document's hierarchy and semantics.

###### Ordered and Unordered with Item
The `<ol>` defines an ordered (numbered) list while the `<ul>` tag defines an unordered list, and the `<li>` tag represents a list item within `<ol>` or `<ul>` lists.
```html
<!-- Ordered List -->
<ol>
  <li>First item</li>
  <li>Second item</li>
  <li>Third item</li>
</ol>

<!-- Unordered List -->
<ul>
  <li>Apple</li>
  <li>Orange</li>
  <li>Banana</li>
</ul>
```

>Choosing the appropriate order for lists (using `<ol>` for ordered lists and `<ul>` for unordered lists) and using the correct list item tag `<li>` can be semantics.

#### Form Input
The HTML provides several form-related tags to create interactive forms on web pages. Here's an explanation of the main form-related tags:

###### Form
**`<form>`**: This tag is used to create an HTML form. It encloses all the form elements and defines the way data is sent to the server. The `action` attribute specifies the URL where the form data is sent, and the `method` attribute specifies the HTTP method (usually "GET" or "POST").
```html
<form action="/submit_form" method="post">
   <!-- Form elements go here -->
</form>
```

>You can omit attribute `action` and `method` in `<form>` without any error happening.

###### Label
**`<label>`**: This tag represents a label for an `<input>`, `<select>`, `<textarea>`, or `<button>` element. It helps improve accessibility and user experience by associating a text label with a form control.
```html
<label for="username">Username:</label>
<input type="text" id="username" name="username">
```

###### Input
**`<input>`**: This tag is used to create various types of form controls, such as text fields, checkboxes, radio buttons, and more. The `type` attribute determines the specific type of input control.
```html
<input type="text" name="username" id="username" placeholder="Enter your username">
```

###### Button
**`<button>`**: This tag represents a clickable button. It can be used to submit a form or trigger a JavaScript function.
```html
<button type="submit">Submit</button>
```

Putting it all together in a simple form example:
```html
<form>
   <label for="username">Username:</label>
   <input type="text" id="username" name="username" placeholder="Enter your username">

   <label for="password">Password:</label>
   <input type="password" id="password" name="password" placeholder="Enter your password">

   <button type="submit">Submit</button>
</form>
```

>Default navigation when you submit the form is reload the current page. but you can prevent it by using JavaScript code.

```html
<form id="myForm">
  <!-- form fields go here -->
  <input type="submit" value="Submit">
</form>

<script>
  document.getElementById('myForm').addEventListener('submit', function(event) {
    // Prevent the default form submission
    event.preventDefault();

    // Optionally, you can perform additional actions here
  });
</script>
```

In this example, we have a form with two text input fields (for username and password) and a submit button. The `<label>` elements provide labels for the input fields, and the `for` attribute in the `<label>` tags is associated with the `id` attribute of the corresponding `<input>` elements for better accessibility.

#### Simple Table
The HTML table structure is composed of several elements to organize and display tabular data. Here's an explanation of the main table-related tags:

###### Table
`<table>`: This tag defines the start of the HTML table. All the content of the table, including rows and cells, is enclosed between the opening `<table>` tag and the closing `</table>` tag.
```html
<table>
   <!-- Table content (rows and cells) goes here -->
</table>
```

###### Table Row
`<tr>`: This tag represents a row in the table. It contains one or more `<td>` (table data) or `<th>` (table header) elements.
```html
<table>
   <tr>
      <!-- Table header or data cells go here -->
   </tr>
</table>
```

###### Table Header Cell
`<th>`: This tag represents a header cell in a table. It is typically used to label the columns or rows. Text within `<th>` elements is usually bold and centered.
```html
<table>
   <tr>
      <th>Header 1</th>
      <th>Header 2</th>
   </tr>
   <!-- More rows go here -->
</table>
```

###### Table Data Cell
`<td>`: This tag represents a standard data cell in a table. It contains the actual data that is displayed in the table.
```html
<table>
   <tr>
      <td>Data 1</td>
      <td>Data 2</td>
   </tr>
   <!-- More rows go here -->
</table>
```

Putting it all together in a simple example:
```html
<table>
   <tr>
      <th>Name</th>
      <th>Age</th>
      <th>Country</th>
   </tr>
   <tr>
      <td>John Doe</td>
      <td>25</td>
      <td>USA</td>
   </tr>
   <tr>
      <td>Jane Smith</td>
      <td>30</td>
      <td>Canada</td>
   </tr>
</table>
```

In this example, we have a table with three columns (Name, Age, Country) and two rows of data. The first row contains headers (`<th>`), and the subsequent rows contain data (`<td>`). The `<tr>` tag defines each row in the table.

#### Media
Multimedia comes in many different formats. It can be almost anything you can hear or see, like images, music, sound, videos, records, films, animations, and more.

Web pages often contain multimedia elements of different types and formats.

###### Video
The HTML `<video>` tag is used to embed video content in a web page. It supports various video formats and provides options for customization. Here's a breakdown of its attributes:

- **`src`**: Specifies the source URL or file path of the video.
- **`controls`**: Adds video playback controls (play, pause, volume, etc.).
- **`width` and `height`**: Set the width and height of the video player.
- **`autoplay`**: Automatically starts playing the video when the page loads.
- **`loop`**: Loops the video playback.
- **`muted`**: Mutes the audio of the video.

Here's an example of how to use the `<video>` tag:
```html
<div class="video">
  <h2>MP4 Video Example</h2>

  <video width="640" height="360" controls>
    <source src="path/to/your/local-video.mp4" type="video/mp4" />
    Your browser does not support the video tag.
  </video>
</div>
```

###### Audio
The HTML `<audio>` tag is used to embed audio content in a web page. It allows you to include various audio formats and provides controls for playback. Here's a breakdown of its attributes:

- **`src`**: Specifies the source URL or file path of the audio.
- **`controls`**: Adds audio playback controls (play, pause, volume, etc.).
- **`autoplay`**: Automatically starts playing the audio when the page loads.
- **`loop`**: Loops the audio playback.
- **`muted`**: Mutes the audio.

Here's an example of how to use the `<audio>` tag:
```html
<div class="audio">
  <h2>MP3 Audio Example</h2>

  <audio controls>
    <source src="path/to/your/audio.mp3" type="audio/mp3" />
    Your browser does not support the audio element.
  </audio>
</div>
```

###### YouTube
To embed a YouTube video in an HTML document, you can use an `<iframe>` tag with the `src` attribute set to the YouTube video's embed URL. Here's an example:
```html
<div class="youtube">
  <h2>YouTube Media Example</h2>

  <iframe
    width="560"
    height="315"
    src="https://www.youtube.com/embed/your-video-id"
    frameborder="0"
    allowfullscreen
  ></iframe>
</div>
```

>You cannot directly embed a YouTube video for local playback because YouTube videos are hosted on YouTube's servers.


#html #phase-1 #documentation #html-template #semantic-html #most-used-html