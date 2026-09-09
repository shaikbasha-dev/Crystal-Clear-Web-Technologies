# 6. Important HTML Tags

HTML provides many different tags, and each tag has a **specific purpose**.

Instead of trying to memorize the tags randomly, it is much easier to group them according to what they are used for.

The following are the important tags listed in your notes.

---

## 6.1 Document Structure Tags

These tags define the basic structure of an HTML document.

```html
<html>
<head>
<title>
<body>
```

### `<html>`

The `<html>` element is the **root element** of the HTML document.

```html
<html>
    ...
</html>
```

Everything in the HTML document is placed inside it.

---

### `<head>`

The `<head>` element contains information and resources related to the document.

```html
<head>
    ...
</head>
```

For example, the document title is placed inside it.

---

### `<title>`

The `<title>` element specifies the title of the HTML document.

```html
<title>My Page</title>
```

The title is commonly displayed in the browser tab.

---

### `<body>`

The `<body>` element contains the main content of the webpage.

```html
<body>
    Welcome to my website.
</body>
```

Headings, paragraphs, images, links, tables, forms and many other visible webpage elements are normally placed inside `<body>`.

---

# 6.2 Heading Tags — `<h1>` to `<h6>`

HTML provides six levels of headings:

```html
<h1>Heading 1</h1>
<h2>Heading 2</h2>
<h3>Heading 3</h3>
<h4>Heading 4</h4>
<h5>Heading 5</h5>
<h6>Heading 6</h6>
```

They represent different heading levels.

```text
<h1> → Heading level 1
<h2> → Heading level 2
<h3> → Heading level 3
<h4> → Heading level 4
<h5> → Heading level 5
<h6> → Heading level 6
```

For example:

```html
<h1>Web Technologies</h1>

<h2>HTML</h2>

<h3>HTML Tags</h3>
```

Think of them like the headings in a book:

```text
Web Technologies
    ↓
    HTML
       ↓
       HTML Tags
```

---

# 6.3 Paragraph Tag — `<p>`

The `<p>` element represents a paragraph.

```html
<p>This is a paragraph.</p>
```

You can have multiple paragraphs:

```html
<p>HTML is used to structure webpages.</p>

<p>CSS is used to style webpages.</p>

<p>JavaScript adds behavior.</p>
```

---

# 6.4 Line Break Tag — `<br>`

`<br>` is used to create a line break.

Example:

```html
Hello<br>
World
```

The result appears approximately as:

```text
Hello
World
```

It is an empty/void element, so it does not require a normal closing tag.

---

# 6.5 Horizontal Rule — `<hr>`

`<hr>` represents a thematic break and is commonly displayed as a horizontal line.

Example:

```html
<h1>Chapter 1</h1>

<hr>

<p>This is the content of Chapter 1.</p>
```

It is also a void element.

---

# 6.6 Preformatted Text — `<pre>`

The `<pre>` element is used for **preformatted text**.

Whitespace and line breaks inside `<pre>` are preserved as written.

Example:

```html
<pre>
Name:  Mahaboob
Age:   26
Course: Java
</pre>
```

The browser preserves the spacing and line breaks within the `<pre>` element.

This can be useful when the exact formatting of text matters.

---

# 6.7 Anchor Tag — `<a>`

The `<a>` element is used to create a **hyperlink**.

Example:

```html
<a href="https://example.com">Visit Website</a>
```

Here:

```text
<a>        → Anchor element
href       → Specifies the destination
Visit Website → Clickable text
```

When the user clicks the link, the browser can navigate to the specified destination.

---

# 6.8 Image Tag — `<img>`

The `<img>` element is used to display an image.

Example:

```html
<img src="photo.jpg">
```

Here:

```text
<img>       → Image element
src         → Specifies the image source
photo.jpg   → Image file
```

A more useful example is:

```html
<img src="photo.jpg" alt="Student Photo">
```

The `alt` attribute provides alternative text for the image.

`<img>` is a void element.

---

# 6.9 Audio Tag — `<audio>`

The `<audio>` element is used to embed audio content.

Example:

```html
<audio controls>
    <source src="music.mp3" type="audio/mpeg">
</audio>
```

The `controls` attribute allows the browser to provide audio controls.

---

# 6.10 Video Tag — `<video>`

The `<video>` element is used to embed video content.

Example:

```html
<video controls>
    <source src="movie.mp4" type="video/mp4">
</video>
```

The `controls` attribute provides controls such as play and pause.

---

# 6.11 Ordered List — `<ol>`

`<ol>` creates an **ordered list**.

The items are normally displayed in a numbered sequence.

Example:

```html
<ol>
    <li>HTML</li>
    <li>CSS</li>
    <li>JavaScript</li>
</ol>
```

Result:

```text
1. HTML
2. CSS
3. JavaScript
```

---

# 6.12 Unordered List — `<ul>`

`<ul>` creates an **unordered list**.

The items are normally displayed using bullets.

Example:

```html
<ul>
    <li>HTML</li>
    <li>CSS</li>
    <li>JavaScript</li>
</ul>
```

Result:

```text
• HTML
• CSS
• JavaScript
```

---

# 6.13 List Item — `<li>`

`<li>` represents an individual **list item**.

It is normally used inside:

```text
<ol>
```

or:

```text
<ul>
```

Example:

```html
<ul>
    <li>HTML</li>
    <li>CSS</li>
    <li>JavaScript</li>
</ul>
```

Here there are three `<li>` elements.

```text
<ul>
 ├── <li>HTML</li>
 ├── <li>CSS</li>
 └── <li>JavaScript</li>
```

---

# 6.14 Description List — `<dl>`

`<dl>` is used to create a **description list**.

It works together with:

```html
<dt>
<dd>
```

Example:

```html
<dl>
    <dt>HTML</dt>
    <dd>Used to structure webpages.</dd>

    <dt>CSS</dt>
    <dd>Used to style webpages.</dd>
</dl>
```

Think of it as:

```text
Term
  ↓
Description
```

---

# 6.15 Description Term — `<dt>`

`<dt>` represents the **term/name** in a description list.

Example:

```html
<dt>HTML</dt>
```

Here:

```text
HTML → Term
```

---

# 6.16 Description Definition — `<dd>`

`<dd>` provides the **description of the term**.

Example:

```html
<dt>HTML</dt>
<dd>Used to structure webpages.</dd>
```

So:

```text
<dt> → Term
<dd> → Description
```

---

# 6.17 Blockquote — `<blockquote>`

`<blockquote>` is used for a longer quotation or quoted section.

Example:

```html
<blockquote>
    Learning never stops.
</blockquote>
```

It indicates that the content is a quotation.

---

# 6.18 Abbreviation — `<abbr>`

`<abbr>` represents an abbreviation or acronym.

Example:

```html
<abbr title="HyperText Markup Language">HTML</abbr>
```

Here:

```text
HTML
 ↓
Abbreviation
 ↓
HyperText Markup Language
```

The `title` attribute provides the expanded meaning.

---

# 6.19 Citation — `<cite>`

`<cite>` is used to identify the title of a cited creative work or reference.

Example:

```html
<p>
    <cite>Harry Potter</cite> is a popular book series.
</p>
```

The `<cite>` element identifies the cited work.

---

# 6.20 Short Quotation — `<q>`

`<q>` is used for a **short inline quotation**.

Example:

```html
<p>
    He said, <q>HTML is easy to learn.</q>
</p>
```

The browser generally renders the quoted text with quotation marks.

---

# 6.21 `<blockquote>` vs `<q>`

Both are related to quotations, but they are used differently.

| `<blockquote>`                        | `<q>`                   |
| ------------------------------------- | ----------------------- |
| Longer quotation                      | Short quotation         |
| Usually displayed as a separate block | Used within normal text |
| Example: large quoted passage         | Example: `"Hello"`      |

Simple memory:

```text
<blockquote> → Big/long quotation

<q> → Quick/short quotation
```

---

# 6.22 `<div>`

`<div>` is a **generic block-level container**.

It is commonly used to group related content.

Example:

```html
<div>
    <h1>Student Details</h1>
    <p>Name: Ali</p>
    <p>Course: Java</p>
</div>
```

Here, the `<div>` groups the student-related content together.

Think of `<div>` as a **large container**.

---

# 6.23 `<span>`

`<span>` is a **generic inline container**.

It is commonly used to group or target a small part of text/content.

Example:

```html
<p>
    My favorite language is
    <span>Java</span>.
</p>
```

Think:

```text
<div>  → Larger/general container

<span> → Smaller/inline container
```

---

# 6.24 `<div>` vs `<span>`

| `<div>`                                  | `<span>`                                      |
| ---------------------------------------- | --------------------------------------------- |
| Generic block-level container            | Generic inline container                      |
| Commonly used for larger sections/groups | Commonly used for smaller portions of content |
| Starts on a new line in normal flow      | Does not normally start a new line            |
| Can contain many elements                | Commonly used within text                     |

Example:

```html
<div>
    Student Information
</div>
```

versus:

```html
<p>
    Student <span>Information</span>
</p>
```

---

# 6.25 Form — `<form>`

The `<form>` element is used to create a **form for collecting user input**.

Example:

```html
<form>
    <input type="text">
    <input type="submit">
</form>
```

Forms are commonly used for:

* Login
* Registration
* Search
* Contact forms
* Data submission

---

# 6.26 Input — `<input>`

`<input>` creates an input control.

Example:

```html
<input type="text">
```

Other examples:

```html
<input type="email">

<input type="number">

<input type="password">

<input type="date">
```

The `type` attribute determines the kind of input control.

---

# 6.27 Label — `<label>`

`<label>` provides a label for a form control.

Example:

```html
<label>Name:</label>
<input type="text">
```

A better connected example is:

```html
<label for="name">Name:</label>
<input type="text" id="name">
```

Here the label is associated with the input using:

```text
for="name"
      ↕
id="name"
```

---

# 6.28 Fieldset — `<fieldset>`

`<fieldset>` is used to **group related form controls**.

Example:

```html
<fieldset>

    <input type="text">
    <input type="email">

</fieldset>
```

Think of it as a **box/group around related form controls**.

---

# 6.29 Legend — `<legend>`

`<legend>` provides a caption for a `<fieldset>`.

Example:

```html
<fieldset>

    <legend>Personal Information</legend>

    <label>Name:</label>
    <input type="text">

    <label>Email:</label>
    <input type="email">

</fieldset>
```

Here:

```text
<fieldset>
     ↓
Group of related controls

<legend>
     ↓
Name/caption of that group
```

---

# 6.30 Table — `<table>`

`<table>` is used to create a table.

Example:

```html
<table>
    ...
</table>
```

A table can contain rows and cells.

```text
        Table
          │
       ┌──┴──┐
       ↓     ↓
     Rows   Cells
```

---

# 6.31 Table Row — `<tr>`

`<tr>` represents a **table row**.

Example:

```html
<tr>
    ...
</tr>
```

A table contains multiple rows.

```html
<table>

    <tr>
        ...
    </tr>

    <tr>
        ...
    </tr>

</table>
```

---

# 6.32 Table Data — `<td>`

`<td>` represents a normal **table data cell**.

Example:

```html
<tr>
    <td>Ali</td>
    <td>Java</td>
</tr>
```

Here:

```text
Ali   → Data cell
Java  → Data cell
```

---

# 6.33 Table Header — `<th>`

`<th>` represents a **header cell** in a table.

Example:

```html
<tr>
    <th>Name</th>
    <th>Course</th>
</tr>
```

Here:

```text
Name    → Header
Course  → Header
```

---

# 6.34 Complete Table Example

```html
<table>

    <tr>
        <th>Name</th>
        <th>Course</th>
    </tr>

    <tr>
        <td>Ali</td>
        <td>Java</td>
    </tr>

    <tr>
        <td>Ravi</td>
        <td>Python</td>
    </tr>

</table>
```

The structure is:

```text
<table>
    │
    ├── <tr>
    │     ├── <th>
    │     └── <th>
    │
    ├── <tr>
    │     ├── <td>
    │     └── <td>
    │
    └── <tr>
          ├── <td>
          └── <td>
</table>
```

Remember:

```text
<table> → Complete table
<tr>    → Table row
<th>    → Header cell
<td>    → Data cell
```

---

# 6.35 Datalist — `<datalist>`

`<datalist>` provides a set of suggested options for an input control.

Example:

```html
<input list="courses">

<datalist id="courses">
    <option value="Java">
    <option value="Python">
    <option value="JavaScript">
</datalist>
```

The user can type into the input and choose from the available suggestions.

Think of it as:

```text
Input box
    ↓
Suggestions
    ├── Java
    ├── Python
    └── JavaScript
```

---

# 6.36 Option — `<option>`

`<option>` represents an individual option.

It is commonly used inside elements such as `<datalist>` and `<select>`.

Example with `<datalist>`:

```html
<datalist id="courses">

    <option value="Java">
    <option value="Python">
    <option value="JavaScript">

</datalist>
```

Each `<option>` represents one available choice.

---

# 6.37 Important Tag Groups

Now let's organize the complete list from your notes.

### Document structure

```text
<html>
<head>
<title>
<body>
```

### Text and headings

```text
<h1> to <h6>
<p>
<br>
<hr>
<pre>
```

### Links and media

```text
<a>
<img>
<audio>
<video>
```

### Lists

```text
<ol>
<ul>
<li>
<dl>
<dt>
<dd>
```

### Quotations and references

```text
<blockquote>
<abbr>
<cite>
<q>
```

### Containers

```text
<div>
<span>
```

### Forms

```text
<form>
<input>
<label>
<fieldset>
<legend>
<datalist>
<option>
```

### Tables

```text
<table>
<tr>
<td>
<th>
```

---

# 6.38 Complete Tag Map

```text
                         HTML TAGS
                            │
       ┌────────────────────┼────────────────────┐
       ↓                    ↓                    ↓
   Structure              Text                Media
       │                    │                    │
 html/head/body       h1-h6/p/pre          a/img/audio/video
 title                br/hr
       │
       ├───────────────┐
       ↓               ↓
     Lists         Quotations
       │               │
 ol/ul/li          blockquote
 dl/dt/dd          abbr/cite/q
       │
       ├───────────────┐
       ↓               ↓
   Containers        Forms
       │               │
    div/span      form/input/label
                  fieldset/legend
                  datalist/option
       │
       ↓
     Tables
       │
   table/tr/td/th
```

---

# 6.39 Quick Revision Table

| Tag            | Main Purpose                   |
| -------------- | ------------------------------ |
| `<html>`       | Root of HTML document          |
| `<head>`       | Document information/resources |
| `<title>`      | Document title                 |
| `<body>`       | Main webpage content           |
| `<h1>`–`<h6>`  | Headings                       |
| `<p>`          | Paragraph                      |
| `<br>`         | Line break                     |
| `<hr>`         | Thematic break                 |
| `<pre>`        | Preformatted text              |
| `<a>`          | Hyperlink                      |
| `<img>`        | Image                          |
| `<audio>`      | Audio                          |
| `<video>`      | Video                          |
| `<ol>`         | Ordered list                   |
| `<ul>`         | Unordered list                 |
| `<li>`         | List item                      |
| `<dl>`         | Description list               |
| `<dt>`         | Description term               |
| `<dd>`         | Description/details            |
| `<blockquote>` | Longer quotation               |
| `<abbr>`       | Abbreviation                   |
| `<cite>`       | Citation/title of cited work   |
| `<q>`          | Short quotation                |
| `<div>`        | Generic block container        |
| `<span>`       | Generic inline container       |
| `<form>`       | Form                           |
| `<input>`      | Input control                  |
| `<label>`      | Label for form control         |
| `<fieldset>`   | Groups form controls           |
| `<legend>`     | Caption for fieldset           |
| `<table>`      | Table                          |
| `<tr>`         | Table row                      |
| `<td>`         | Table data cell                |
| `<th>`         | Table header cell              |
| `<datalist>`   | Suggested input options        |
| `<option>`     | Individual option              |

---

# 6.40 Most Important Things to Remember

Don't try to memorize all these tags as one huge list.

Remember them by **purpose**:

```text
STRUCTURE
html head title body

TEXT
h1-h6 p br hr pre

LINK / MEDIA
a img audio video

LISTS
ol ul li dl dt dd

QUOTATIONS
blockquote abbr cite q

CONTAINERS
div span

FORMS
form input label fieldset legend
datalist option

TABLES
table tr td th
```

Once you understand these groups, the large list of HTML tags becomes much easier to remember.
