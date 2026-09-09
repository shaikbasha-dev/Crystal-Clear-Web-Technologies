# 2. Introduction to HTML

Before learning individual HTML tags, we need to understand **what HTML is, where it came from, what HTML5 means, and why we use it**.

---

## 2.1 What is HTML?

Suppose you open a webpage and see:

```text
Welcome to My Website

This is my first webpage.

[Visit Google]

       🖼️ Image
```

The browser needs some way to understand what each piece of content represents.

HTML provides that structure.

HTML tells the browser things such as:

```text
This is a heading.
This is a paragraph.
This is an image.
This is a link.
This is a table.
This is a form.
```

### Simple definition

> **HTML is a markup language used to structure the content of a webpage.**

For example:

```html
<h1>Welcome to My Website</h1>
<p>This is my first webpage.</p>
<a href="https://example.com">Visit Website</a>
```

The browser interprets these HTML elements and displays the corresponding content.

---

# 2.2 Full Form of HTML

HTML stands for:

> **HyperText Markup Language**

Let's understand each word.

### HyperText

**HyperText** means text that can contain links to other resources or pages.

For example:

```text
Click Here
```

When you click it, you may be taken to another webpage.

That connection between documents/pages is an important part of the web.

---

### Markup

**Markup** means using special tags to describe or structure content.

For example:

```html
<h1>Welcome</h1>
```

Here:

```text
<h1> → tells the browser that this is a heading
Welcome → the content
</h1> → marks the end of the heading
```

HTML doesn't simply contain plain text. It uses **markup to describe the role of the content**.

---

### Language

HTML is called a language because it follows a defined set of rules and syntax for creating structured web documents.

---

# 2.3 What Does HTML Do?

HTML primarily provides the **structure and content** of a webpage.

For example, HTML can tell the browser:

```text
Create a heading
Create a paragraph
Display an image
Create a link
Create a table
Create a form
Create a list
```

A simple example:

```html
<h1>Student Information</h1>

<p>This page contains student details.</p>

<img src="student.jpg">

<a href="students.html">View Students</a>
```

Here HTML creates different parts of the webpage.

---

## HTML does not primarily control everything

It is important to understand the division of responsibility.

```text
HTML
 ↓
Structure and content

CSS
 ↓
Appearance and styling

JavaScript
 ↓
Behavior and interactivity
```

For example:

```text
HTML       → Create a button
CSS        → Make the button beautiful
JavaScript → Make something happen when it is clicked
```

---

# 2.4 History of HTML

HTML was created for the **World Wide Web**.

The original idea was to make it possible to create documents that could be connected to other documents through hyperlinks.

The development of HTML is closely associated with **Tim Berners-Lee**, who developed the World Wide Web.

The early HTML versions were much simpler than the HTML we use today.

Over time, HTML developed through different versions and standards.

The general progression can be remembered as:

```text
Early HTML
    ↓
HTML 2.0
    ↓
HTML 3.2
    ↓
HTML 4.01
    ↓
XHTML
    ↓
HTML5
```

The language gradually gained more capabilities and better support for modern web applications.

---

# 2.5 HTML Versions

HTML has gone through several versions.

The important versions to know are:

### HTML

The early versions established the basic idea of structuring documents using markup.

---

### HTML 2.0

Provided a more formal specification for HTML and established additional basic capabilities.

---

### HTML 3.2

Added and standardized additional features used by webpages of that period.

---

### HTML 4.01

A major version that provided many commonly used HTML features and stronger separation between document structure and presentation.

---

### XHTML

XHTML applied stricter XML-style rules to HTML.

---

### HTML5

HTML5 brought many features needed for modern websites and web applications.

---

# 2.6 What is HTML5?

HTML5 is a major modern version of HTML.

The important idea is:

> **HTML5 provides modern capabilities for creating structured, multimedia-rich and interactive web content.**

HTML5 introduced or standardized many useful features for modern web development.

For example:

### Multimedia

HTML5 provides elements such as:

```html
<audio></audio>
<video></video>
```

This makes it possible to include audio and video directly in webpages.

---

### Semantic Elements

HTML5 provides meaningful structural elements such as:

```html
<header></header>
<nav></nav>
<section></section>
<article></article>
<footer></footer>
```

These elements make the structure of a webpage clearer.

---

### Forms

HTML5 provides useful form-related features and input types.

For example:

```html
<input type="email">
<input type="date">
<input type="number">
```

It also provides validation-related attributes such as:

```html
<input type="text" required>
```

---

# 2.7 Why Do We Use HTML5?

HTML5 is used because modern websites need more than simple text and links.

A modern webpage may contain:

```text
Text
Images
Audio
Video
Forms
Tables
Navigation
Interactive content
Semantic structure
```

HTML5 provides standard elements and features for representing this content.

---

## 2.8 HTML5 and Modern Web Development

Consider a modern website such as an online shopping application.

It may contain:

```text
                 SHOPPING WEBSITE
                       │
       ┌───────────────┼────────────────┐
       ↓               ↓                ↓
    Header          Products          Footer
       │               │
      Nav          Images/Prices
                       │
                     Forms
```

HTML5 can provide the structure for all these sections.

Then:

```text
HTML5
  ↓
Structure

CSS3
  ↓
Design

JavaScript
  ↓
Interaction
```

Together they form an important foundation of front-end web development.

---

# 2.9 HTML Example

Let's create a very small webpage.

```html
<!DOCTYPE html>
<html>
<head>
    <title>My First Page</title>
</head>

<body>

    <h1>Welcome</h1>

    <p>This is my first webpage.</p>

    <a href="https://example.com">Visit Website</a>

</body>
</html>
```

### What is happening?

```text
<!DOCTYPE html>
        ↓
Tells the browser this is an HTML document

<html>
        ↓
Contains the HTML document

<head>
        ↓
Contains information about the document

<title>
        ↓
Sets the browser/page title

<body>
        ↓
Contains the visible page content

<h1>
        ↓
Creates a heading

<p>
        ↓
Creates a paragraph

<a>
        ↓
Creates a link
```

We will study each of these elements separately in the upcoming topics.

---

# 2.10 HTML5 in One Picture

```text
                         HTML5
                           │
          ┌────────────────┼────────────────┐
          ↓                ↓                ↓
       Structure        Multimedia        Forms
          │                │                │
      Headings           Audio            Input
      Paragraphs         Video            Validation
      Links
      Tables
      Lists
          │
          ↓
   Semantic Elements
          │
    ┌─────┼─────┐
    ↓     ↓     ↓
 Header  Nav  Section
    │           │
 Article       Footer
```

---

# 2.11 Important Points to Remember

### HTML

> HTML is used to **structure webpage content**.

### Full form

> **HyperText Markup Language**

### HTML's main job

> Tell the browser **what different pieces of content are and how they are structured**.

### HTML5

> A modern version of HTML with features supporting modern web content and applications.

### HTML5 examples

```text
<audio>
<video>
<header>
<nav>
<section>
<article>
<footer>
```

and modern form features such as:

```text
email
date
number
required
```

---

# 2.12 HTML vs CSS vs JavaScript

| Technology     | Main Responsibility | Example                             |
| -------------- | ------------------- | ----------------------------------- |
| **HTML**       | Structure           | Create a button                     |
| **CSS**        | Appearance          | Change button color/size            |
| **JavaScript** | Behavior            | Do something when button is clicked |

Think of a webpage as a person:

```text
HTML
 ↓
Body / Structure

CSS
 ↓
Clothes / Appearance

JavaScript
 ↓
Actions / Behavior
```

---

# 2.13 Interview Questions

### What does HTML stand for?

**HyperText Markup Language.**

### What is HTML?

HTML is a markup language used to structure the content of web pages.

### Why is HTML called a markup language?

Because it uses markup tags/elements to describe and structure different types of content.

### What is HTML5?

HTML5 is a modern version of HTML that provides features for creating structured, multimedia-rich and modern web content.

### Why do we use HTML5?

We use HTML5 to create the structure of modern webpages and to support features such as semantic elements, multimedia and modern form controls.

### Does HTML provide styling?

HTML primarily provides structure and content. **CSS is used for styling.**

### Does HTML provide programming behavior?

HTML itself is not responsible for programming behavior. **JavaScript is used to add behavior and interactivity.**

---

# 2.14 Final Revision

Remember this chain:

```text
HTML
 ↓
HyperText Markup Language
 ↓
Markup language
 ↓
Structures webpage content
 ↓
HTML5
 ↓
Modern HTML
 ↓
Semantic elements
Multimedia
Forms
Modern web content
```

And the most important sentence:

> **HTML tells the browser what the content is and how the webpage is structured.**
