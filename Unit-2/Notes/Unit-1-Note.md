--- 
Unit 2: HTML & XHTML - Comprehensive Notes
### 2.1 Introduction to HTML

HTML, which stands for HyperText Markup Language, is the standard language used to create and structure the content of web pages. It is the fundamental building block of the web.

HyperText: Refers to text that contains links ("hyperlinks") to other texts or resources, allowing users to navigate between pages.

Markup Language: A language that uses a system of tags to define and structure elements within a document. It tells the web browser how to display content like headings, paragraphs, images, and links.

HTML describes the structure and meaning (semantics) of web content, not its visual presentation. Styling is handled by CSS, and interactivity is managed by JavaScript.

[Image: A diagram showing three layers. The base layer is "HTML (Structure)", the middle layer is "CSS (Presentation)", and the top layer is "JavaScript (Behavior)".]

### 2.2 Document Structure
Every HTML document follows a standard, hierarchical structure. This structure is essential for the browser to correctly interpret and render the page. The main components are the DOCTYPE, <html>, <head>, and <body>.

<!DOCTYPE html>: The Document Type Declaration. It must be the very first thing in your document. It tells the browser that the page is written in HTML5.

<html> Element: The root element that wraps all the content on the entire page.

<head> Element: A container for metadata (data about the HTML document). This information is not displayed on the page itself but is used by the browser and search engines. It includes things like the page title, character set, links to stylesheets (CSS), and scripts.

<body> Element: Contains all the visible content of the webpage, such as headings, paragraphs, images, tables, lists, and links. Everything inside the <body> tag is rendered in the main browser window.

[Image: A tree diagram showing the HTML document structure.<html>is the root, with two main branches:<head>and<body>. The<head>branch has children like<meta>and<title>. The<body>branch has children like<h1>and<p>.]

Code Example: Basic Document Structure

```
<!DOCTYPE html>
<html lang="en">
<head>
    <!-- Metadata: Not visible on the page -->
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My First Web Page</title>
</head>
<body>
    <!-- Visible content goes here -->
    <h1>Welcome to My Website</h1>
    <p>This is my first paragraph.</p>
</body>
</html>
```

### Differences: HTML vs. XHTML
XHTML (Extensible HyperText Markup Language) is a stricter, more XML-based version of HTML. While HTML5 is the current standard and is more flexible, understanding XHTML rules promotes writing clean, well-formed code.

Feature	HTML (specifically HTML5)	                                        XHTML
| **Feature**                | **HTML (HTML5)**                                                                           | **XHTML**                                                                                      |
| -------------------------- | ------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------- |
| **Well-Formedness**        | Forgiving; browsers render even poorly structured code.                                    | Strict; must follow XML rules with properly nested tags.                                       |
| **Closing Tags**           | Optional for some tags (e.g., `<p>`). Empty tags like `<img>`, `<br>` do not need closing. | Mandatory; every element must be closed. Empty tags must be self-closed (`<img />`, `<br />`). |
| **Case Sensitivity**       | Not case-sensitive; tags and attributes can be uppercase, lowercase, or mixed.             | Case-sensitive; tags and attributes must be lowercase.                                         |
| **Attribute Values**       | Quotes are often optional for attribute values.                                            | Mandatory; all attribute values must be in quotes.                                             |
| **Attribute Minimization** | Allowed (e.g., `<input checked>`).                                                         | Not allowed; attributes must have explicit values (`checked="checked"`).                       |
| **DOCTYPE**                | Simple: `<!DOCTYPE html>`                                                                  | Complex and strictly required.                                                                 |



📌 Important: Best Practice
Even though HTML5 is forgiving, always write your code as if it were XHTML: close all your tags, use lowercase, and quote all attributes. This makes your code more readable, maintainable, and less prone to unexpected browser behavior.

2.3 Text Formatting

Explanation
HTML provides a wide range of tags to format text. These can be categorized into presentational (defining visual appearance) and semantic (defining meaning). Best practice is to prioritize semantic tags.

Code Example: Common Text Formatting Tags

```
<!-- Headings -->
<h1>Heading 1 (Most Important)</h1>
<h2>Heading 2</h2>
<h6>Heading 6 (Least Important)</h6>

<!-- Paragraph -->
<p>This is a standard paragraph of text. It's a block-level element.</p>

<!-- Semantic Formatting -->
<p>This text is <strong>very important</strong>, while this text is just <em>emphasized</em>.</p>
<p>The chemical formula for water is H<sub>2</sub>O, and the equation is E=mc<sup>2</sup>.</p>

<!-- Quote -->
<blockquote cite="http://example.com">
  This is a long quotation that is indented by the browser.
</blockquote>

<!-- Code -->
<p>Use the <code>&lt;p&gt;</code> tag to create a paragraph.</p>
```

Differences: Presentational vs. Semantic Tags
This is a critical concept in modern web development.

| **Tag Type**       | **Presentational Tags**                                           | **Semantic (Phrase) Tags**                                                |
| ------------------ | ----------------------------------------------------------------- | ------------------------------------------------------------------------- |
| **Purpose**        | Describe **how the text looks** (visual style).                   | Describe the **meaning or importance** of text.                           |
| **Examples**       | `<b>` (bold), `<i>` (italic), `<u>` (underline)                   | `<strong>` (strong importance), `<em>` (emphasis), `<cite>` (citation)    |
| **Screen Readers** | Often **ignored** by screen readers; no special meaning conveyed. | Screen readers apply **intonation or emphasis**, improving accessibility. |
| **SEO Impact**     | Minimal or no impact on SEO.                                      | Helps search engines interpret structure and importance of content.       |
| **Best Practice**  | **Avoid** for styling; use **CSS** instead.                       | **Preferred**; use semantic tags for meaningful markup.                   |



### Separation of Concerns
The golden rule is: HTML is for structure and meaning. CSS is for presentation. While <b> and <strong> might look the same in a browser, their purpose is fundamentally different. Always choose the tag that best describes the meaning of your content.

### 2.4 & 2.5 Links and Navigation / Hyperlinks

Hyperlinks are the essence of the "HyperText" in HTML. They connect web pages and resources, forming the World Wide Web. The <a> (anchor) tag is used to create links.

href attribute: The most important attribute. It specifies the destination URL of the link.
Link Text: The visible, clickable part of the link that is placed between the opening <a> and closing </a> tags.

Code Example: Different Types of Links

```
<!-- Link to an external website -->
<a href="https://www.google.com">Go to Google</a>

<!-- Link to another page on the same website (relative URL) -->
<a href="/about.html">About Us</a>

<!-- Link that opens in a new browser tab -->
<a href="https://www.wikipedia.org" target="_blank">Open Wikipedia in a new tab</a>

<!-- Link to a specific section on the same page (internal link/anchor) -->
<a href="#section-2">Jump to Section 2</a>
<!-- ... later on the page ... -->
<h2 id="section-2">This is Section 2</h2>

<!-- Link to send an email -->
<a href="mailto:contact@example.com">Email Us</a>
```

### Differences: Absolute vs. Relative URLs

| **URL Type**   | **Absolute URL**                                                                             | **Relative URL**                                                                |
| -------------- | -------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| **Definition** | A full web address including protocol (`http://` or `https://`), domain name, and full path. | A partial address relative to the current page’s location.                      |
| **Example**    | `https://www.example.com/images/photo.jpg`                                                   | `images/photo.jpg` or `../pages/about.html`                                     |
| **Use Case**   | Used for linking to **external websites** or resources.                                      | Used for linking to **internal pages/resources** within the same website.       |
| **Advantage**  | Clear and unambiguous; always points to the same resource.                                   | More portable; links remain valid even if the website is moved to a new domain. |



### Important: Accessibility
Use descriptive link text. Instead of "Click Here," use text that makes sense out of context, like "View our 2024 Annual Report." This helps users with screen readers and improves SEO.

2.6 Images and Multimedia

HTML allows you to embed images and other multimedia directly into your web pages, making them more engaging.
Images (<img>): An empty tag (no closing tag) used to embed an image.
src: Specifies the source (path or URL) of the image file. Required.
alt: Provides alternative text for the image. Required for accessibility. It's read by screen readers and displayed if the image fails to load.
Audio & Video (<audio>, <video>): HTML5 introduced these tags for native multimedia playback without needing plugins like Flash.
controls: A boolean attribute that adds default playback controls (play/pause, volume, etc.).
<source> element: Used inside <audio> or <video> to specify multiple file formats for better browser compatibility.

Code Example: Embedding Media

```
<!-- A standard image with required attributes -->
<img src="images/logo.png" alt="Our Company Logo" width="200" height="100">

<!-- An HTML5 video player with multiple sources for compatibility -->
<video controls width="640" height="360" poster="images/video-poster.jpg">
  <source src="videos/promo.mp4" type="video/mp4">
  <source src="videos/promo.webm" type="video/webm">
  Your browser does not support the video tag.
</video>

<!-- An HTML5 audio player -->
<audio controls>
  <source src="audio/theme.mp3" type="audio/mpeg">
  <source src="audio/theme.ogg" type="audio/ogg">
  Your browser does not support the audio element.
</audio>

```

### The alt Attribute is NOT Optional
Always provide a descriptive alt attribute for every <img> tag. It is the single most important thing you can do for image accessibility. For purely decorative images, an empty alt attribute (alt="") is acceptable.

2.7 Lists, Tables, Forms, and Input
These elements are used to structure complex data and gather user input.

### Lists
Used to group related items.
<ul> (Unordered List): For items where the order doesn't matter. Displays with bullet points by default.
<ol> (Ordered List): For items where the sequence is important. Displays with numbers by default.
<dl> (Definition List): Used to list terms (<dt>) and their definitions (<dd>).

Code Example: Lists

```
<ul>
  <li>Coffee</li>
  <li>Tea</li>
</ul>

<ol>
  <li>First, open the file.</li>
  <li>Second, edit the content.</li>
</ol>

<dl>
    <dt> MOMO </dt>
    <dd>Veg</dd>
    <dd>Buff</dd>
    <dd>chicken</dd>
</dl>
```

### Tables

Used to display tabular data in a grid of rows and columns.

<table>: The main container.
<tr> (Table Row): Defines a row.
<th> (Table Header): A header cell. Text is bold and centered by default.
<td> (Table Data): A standard data cell.

colspan & rowspan: Attributes to make a cell span multiple columns or rows.
[Image: A simple table grid showing<tr>as rows,<th>as the header row cells, and<td>as the data cells.]

Code Example: Table with colspan

```
<table border="1">
  <thead>
    <tr>
      <th>Name</th>
      <th colspan="2">Contact</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>John Doe</td>
      <td>Email</td>
      <td>Phone</td>
    </tr>
  </tbody>
</table>
```

### Tables for Data, Not Layout
Do not use <table> elements to create the layout of your webpage. This is an outdated practice that is bad for accessibility and maintainability. Use CSS (e.g., Flexbox, Grid) for page layout.

### Forms and Input

Used to collect user input.
<form>: The container for all form controls.
action: The URL where the form data will be sent for processing.
method: The HTTP method to use (GET or POST).

Form Elements: <label> <input> <textarea> <select> <option> <details> <fieldset> <lagend>

<input>: The most versatile form element. Its behavior changes based on the type attribute (text, password, radio, checkbox, submit, file, etc.).
<label>: Crucial for accessibility. It connects a text label to a specific form control.
Other Controls: <textarea> (multi-line text), <select> (dropdown list).

### Common HTML <input> Element Types
Type	    Description
text	    A single-line text input field. The most common input type.
password	Similar to text, but the characters entered are masked (shown as dots or asterisks).
submit	    A button that, when clicked, submits the form data to the server.
reset	    A button that resets all form controls to their initial values.
button	    A generic clickable button with no default behavior. Used with JavaScript.
radio	    A circular radio button. Allows a user to select only ONE option from a group of choices that share the same name attribute.
checkbox	A square checkbox. Allows a user to select ZERO or MORE options from a group of choices.
file	    An input field for file selection, which includes a "Browse..." button.
hidden	    An input field that is not visible to the user but its value is submitted with the form. Used for sending tracking data or security tokens.
email	(HTML5) A field for an email address. Browsers may provide basic format validation.
url	    (HTML5) A field for a URL. Browsers may provide basic format validation.
number	(HTML5) A field for numeric input. Often displayed with spinner controls.
date	(HTML5) Provides a date picker interface for selecting a year, month, and day.
color	(HTML5) Provides a color picker interface.
range	(HTML5) A slider control for selecting a number within a specified range.
search	(HTML5) A text field specifically for search queries. May have different styling.
tel	    (HTML5) A field for a telephone number. May trigger a numeric keypad on mobile devices.


### Common <form> Element Attributes
Attribute	Description
action	    (Essential) Specifies the URL of the server-side script that will process the form data when it is submitted.
method	    (Essential) Specifies the HTTP method to use for submitting the form. The two main values are:
	        • GET: Appends form data to the URL. Use for non-sensitive data like search queries.
	        • POST: Sends form data in the HTTP request body. Use for sensitive data, logins, or file uploads.
enctype	    Specifies how the form data should be encoded when submitted. Only used with method="POST". The default is fine for most forms, but you must use multipart/form-data when the form includes a file upload (<input type="file">).
name	        Gives the form a name. Useful for referencing the form with JavaScript.
id	            Provides a unique identifier for the form, which can be used by JavaScript or CSS.
target	        Specifies where to display the response after submitting the form (e.g., _self for the same window, _blank for a new window/tab).
autocomplete	Specifies whether a browser should automatically complete values based on user's previous entries. Can be set to on or off.
novalidate	    A boolean attribute that disables the browser's default HTML5 form validation for all controls within the form.
onsubmit	    An event attribute that specifies a JavaScript function to run when the form is submitted (before the data is sent to the server). Often used for client-side validation.

### Differences: GET vs. POST Method

| **Feature**         | **GET**                                                  | **POST**                                                          |
| ------------------- | -------------------------------------------------------- | ----------------------------------------------------------------- |
| **Data Submission** | Appends data to the URL as a query string.               | Sends data within the body of the HTTP request.                   |
| **Visibility**      | Data is visible in the URL and browser history.          | Data is not visible in the URL.                                   |
| **Data Limit**      | Limited length (approximately 2048 characters).          | No size limit.                                                    |
| **Security**        | Not secure; should **never** be used for sensitive data. | More secure; suitable for passwords, personal info, file uploads. |
| **Use Case**        | Search queries, page parameters, bookmarkable links.     | Logins, registrations, submitting sensitive or large data.        |


Code Example: A Simple Form
```
    <form action="/submit-form.php" method="POST">
    <div>
        <label for="username">Username:</label>
        <input type="text" id="username" name="user_name" required>
    </div>
    <div>
        <label for="password">Password:</label>
        <input type="password" id="password" name="user_pass" required>
    </div>
    <div>
        <input type="submit" value="Log In">
    </div>
    </form>
```
### 2.8 Semantic HTML

Semantic HTML means using HTML tags that accurately describe the meaning and purpose of the content they contain, rather than just how they look. Using semantic tags makes your website more accessible for users with screen readers and helps search engines (like Google) better understand your content, which can improve your site's ranking (SEO).

Before HTML5, developers often used generic <div> tags for everything.
Non-Semantic Example:
<div id="header">...</div>
<div id="nav">...</div>
<div class="article">...</div>
<div id="footer">...</div>

HTML5 introduced new semantic elements to give structure and meaning to these common page sections.

[Image: A diagram of a webpage layout. A non-semantic version shows boxes all labeled "div". A semantic version shows the same layout but with boxes labeled "<header>", "<nav>", "<main>", "<article>", "<aside>", and "<footer>".]

Code Example: A Semantic Layout

```
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Semantic Page</title>
</head>
<body>
    <header>
        <h1>My Awesome Blog</h1>
        <nav>
            <ul>
                <li><a href="#">Home</a></li>
                <li><a href="#">About</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <article>
            <h2>Article Title</h2>
            <p>Content of the article...</p>
        </article>
        
        <aside>
            <h3>Related Links</h3>
            <ul>
                <li><a href="#">Link 1</a></li>
            </ul>
        </aside>
    </main>

    <footer>
        <p>&copy; 2024 My Website. All rights reserved.</p>
    </footer>
</body>
</html>
``` 
### Important: Benefits of Semantic HTML

Accessibility: Screen readers can use semantic tags to help visually impaired users navigate the page more easily (e.g., "jump to main content").

SEO: Search engines give more weight to content inside semantic tags like <main> and <article>, helping them understand your page structure.

Maintainability: Your code becomes much easier to read and understand for other developers (and your future self!).