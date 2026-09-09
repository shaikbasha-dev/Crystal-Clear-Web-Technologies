# 8. Paragraph and Text Formatting

This topic explains how HTML is used to **write paragraphs, control line breaks, create horizontal divisions, preserve spaces/line breaks, and format text**.

---

## 8.1 Paragraph — `<p>`

The `<p>` element is used to represent a **paragraph of text**.

### Syntax

```html
<p>Paragraph content</p>
```

### Example

```html
<p>HTML is used to create the structure of webpages.</p>
```

The complete structure is:

```text
<p>                         → Opening tag
HTML is used to create...   → Content
</p>                        → Closing tag
```

### Multiple paragraphs

```html
<p>HTML is used to structure webpages.</p>

<p>CSS is used to style webpages.</p>

<p>JavaScript is used to add behavior.</p>
```

Each `<p>` represents a separate paragraph.

---

# 8.2 Line Break — `<br>`

The `<br>` element is used when you want to move content to the **next line**.

### Example

```html
<p>
    Hello<br>
    Welcome to HTML
</p>
```

The text is displayed approximately as:

```text
Hello
Welcome to HTML
```

### Important

`<br>` is a **void element**, so it does not require a closing tag.

Correct:

```html
<br>
```

You do not normally write:

```html
<br></br>
```

---

## `<p>` vs `<br>`

These are often confused.

### `<p>`

Creates a paragraph:

```html
<p>This is paragraph one.</p>
<p>This is paragraph two.</p>
```

### `<br>`

Creates a line break within the surrounding content:

```html
This is line one.<br>
This is line two.
```

Remember:

```text
<p>  → Paragraph
<br> → Line break
```

---

# 8.3 Horizontal Line — `<hr>`

The `<hr>` element represents a **thematic break** between sections of content.

Browsers commonly display it as a horizontal line.

### Example

```html
<h2>HTML</h2>

<p>HTML provides webpage structure.</p>

<hr>

<h2>CSS</h2>

<p>CSS provides webpage styling.</p>
```

The `<hr>` separates the two sections.

It is also a **void element**.

```html
<hr>
```

There is no normal closing tag.

---

# 8.4 `<br>` vs `<hr>`

| `<br>`                                   | `<hr>`                      |
| ---------------------------------------- | --------------------------- |
| Creates a line break                     | Represents a thematic break |
| Moves following content to the next line | Separates content/sections  |
| Example: `Hello<br>World`                | Example: `<hr>`             |
| Void element                             | Void element                |

Simple distinction:

```text
<br>
 ↓
Break the line

<hr>
 ↓
Separate content/sections
```

---

# 8.5 Preformatted Text — `<pre>`

The `<pre>` element is used for **preformatted text**.

The browser preserves the whitespace and line breaks inside the element.

### Example

```html
<pre>
Name     : Mahaboob
Course   : Java
Location : Bangalore
</pre>
```

The spacing and line breaks are preserved as written.

---

## Why do we need `<pre>`?

Normally, HTML does not treat every space and line break in source code as a visible space or line break.

For example:

```html
<p>
    Hello
             World
</p>
```

The browser generally collapses the whitespace when displaying normal HTML text.

With `<pre>`:

```html
<pre>
Hello
             World
</pre>
```

the formatting is preserved.

---

# 8.6 `<pre>` Example

Consider this:

```html
<pre>
HTML
    CSS
        JavaScript
</pre>
```

The indentation is preserved.

Conceptually:

```text
HTML
    CSS
        JavaScript
```

This makes `<pre>` useful when the exact arrangement of text matters.

---

# 8.7 Basic Text Formatting

HTML provides elements for giving text different meanings or presentations.

Common examples include:

```text
Bold
Italic
Underline
Quotation
Citation
Abbreviation
```

Some commonly used formatting elements are:

```html
<strong>
<em>
<b>
<i>
<u>
<q>
<blockquote>
<cite>
<abbr>
```

---

# 8.8 Bold Text — `<b>`

The `<b>` element is used to draw attention to text without adding a specific level of importance.

Example:

```html
<p>This is <b>bold text</b>.</p>
```

The browser normally displays:

```text
This is bold text.
```

with the selected text visually bold.

### Syntax

```html
<b>Text</b>
```

---

# 8.9 Important Text — `<strong>`

Although your topic mentions **bold**, it is important to understand the distinction between `<b>` and `<strong>`.

```html
<p>This is <strong>important information.</strong></p>
```

`<strong>` indicates that the content has **strong importance**.

Browsers commonly display it in bold.

So:

```text
<b>
 ↓
Visual attention/bold presentation

<strong>
 ↓
Strong importance/semantic meaning
```

### Important interview point

Do not simply say:

> "`<b>` and `<strong>` are exactly the same."

They may look similar by default, but they have different semantic purposes.

---

# 8.10 Italic Text — `<i>`

The `<i>` element represents text in an **alternate voice or mood**, or text that is conventionally presented in italics.

Example:

```html
<p>This is <i>italic text</i>.</p>
```

Syntax:

```html
<i>Text</i>
```

The browser normally displays the text in an italic style.

---

# 8.11 Emphasized Text — `<em>`

`<em>` represents **emphasized text**.

Example:

```html
<p>You <em>must</em> complete the assignment.</p>
```

Browsers commonly display `<em>` as italic text.

The important difference is semantic:

```text
<i>
 ↓
Alternate voice/mood or conventional italic styling

<em>
 ↓
Emphasis
```

---

# 8.12 Underline — `<u>`

The `<u>` element represents text with an **unarticulated annotation**, and browsers commonly render it with an underline.

Example:

```html
<p>This is <u>underlined text</u>.</p>
```

Syntax:

```html
<u>Text</u>
```

---

# 8.13 Bold vs Italic vs Underline

```html
<b>Bold</b>

<i>Italic</i>

<u>Underline</u>
```

Conceptually:

```text
Bold       → visually bold
Italic     → visually italic
Underline  → visually underlined
```

---

# 8.14 Combining Formatting Elements

HTML elements can be nested.

For example:

```html
<p>
    This is <b><i>bold and italic</i></b> text.
</p>
```

Here:

```text
<p>
   └── <b>
         └── <i>
               └── bold and italic
```

Multiple elements can therefore be applied to the same content.

---

# 8.15 Quotation — `<q>`

The `<q>` element is used for a **short inline quotation**.

Example:

```html
<p>
    He said, <q>HTML is easy to learn.</q>
</p>
```

The browser generally displays the quoted text with quotation marks.

Think:

```text
<q>
 ↓
Short quotation inside normal text
```

---

# 8.16 Block Quotation — `<blockquote>`

`<blockquote>` is used for a **longer quotation or quoted section**.

Example:

```html
<blockquote>
    Learning web technologies requires regular practice.
</blockquote>
```

It represents a quotation that forms its own block of content.

---

# 8.17 `<q>` vs `<blockquote>`

| `<q>`                   | `<blockquote>`                          |
| ----------------------- | --------------------------------------- |
| Short quotation         | Longer quotation                        |
| Inline                  | Block-level                             |
| Used within normal text | Used for a separate quoted section      |
| Example: `<q>Hello</q>` | Example: `<blockquote>...</blockquote>` |

Easy memory:

```text
<q>
 ↓
Quick/short quotation

<blockquote>
 ↓
Long/block quotation
```

---

# 8.18 Citation — `<cite>`

The `<cite>` element is used to identify the **title of a cited creative work**, such as a book, movie, song, or other work.

Example:

```html
<p>
    <cite>The Alchemist</cite> is a famous novel.
</p>
```

Here:

```text
The Alchemist
      ↓
Cited work
```

is represented using `<cite>`.

---

# 8.19 Abbreviation — `<abbr>`

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

title
 ↓
Expanded meaning
```

Another example:

```html
<p>
    <abbr title="Cascading Style Sheets">CSS</abbr>
</p>
```

---

# 8.20 Quotation and Citation Elements Together

The important elements from this area are:

```text
<q>
 ↓
Short quotation

<blockquote>
 ↓
Long quotation

<cite>
 ↓
Title of a cited work

<abbr>
 ↓
Abbreviation
```

Example:

```html
<p>
    <cite>HTML Guide</cite> explains that
    <q>HTML structures webpages.</q>
</p>
```

---

# 8.21 Complete Example

Let's combine the concepts:

```html
<!DOCTYPE html>

<html>

<head>
    <title>Text Formatting</title>
</head>

<body>

    <h1>HTML Text Formatting</h1>

    <p>
        HTML is used to <b>structure</b> webpage content.
    </p>

    <p>
        HTML can also contain <i>italic</i> and
        <u>underlined</u> text.
    </p>

    <p>
        This is the first line.<br>
        This is the second line.
    </p>

    <hr>

    <pre>
Name   : Student
Course : Web Technologies
    </pre>

    <p>
        He said, <q>HTML is easy to learn.</q>
    </p>

    <blockquote>
        Web development requires understanding structure,
        presentation, and behavior.
    </blockquote>

    <p>
        <cite>Web Development Guide</cite>
    </p>

    <p>
        <abbr title="HyperText Markup Language">HTML</abbr>
        is a markup language.
    </p>

</body>

</html>
```

---

# 8.22 Important Tag Summary

| Element        | Purpose                                                  |
| -------------- | -------------------------------------------------------- |
| `<p>`          | Paragraph                                                |
| `<br>`         | Line break                                               |
| `<hr>`         | Thematic break                                           |
| `<pre>`        | Preformatted text                                        |
| `<b>`          | Draws attention with bold presentation                   |
| `<strong>`     | Strong importance                                        |
| `<i>`          | Alternate voice/mood or conventional italic presentation |
| `<em>`         | Emphasis                                                 |
| `<u>`          | Underlined/unarticulated annotation                      |
| `<q>`          | Short inline quotation                                   |
| `<blockquote>` | Longer quotation                                         |
| `<cite>`       | Title of a cited creative work                           |
| `<abbr>`       | Abbreviation/acronym                                     |

---

# 8.23 Most Important Differences

### `<p>` vs `<br>`

```text
<p>  → Paragraph
<br> → Line break
```

### `<br>` vs `<hr>`

```text
<br> → Breaks a line

<hr> → Represents a thematic break
```

### `<b>` vs `<strong>`

```text
<b>        → Bold presentation/attention
<strong>   → Strong importance
```

### `<i>` vs `<em>`

```text
<i>   → Alternate voice/mood or conventional italic presentation
<em>  → Emphasis
```

### `<q>` vs `<blockquote>`

```text
<q>           → Short inline quotation
<blockquote>  → Longer quotation
```

---

# 8.24 Final Revision

```text
                 TEXT & PARAGRAPH
                         │
        ┌────────────────┼─────────────────┐
        ↓                ↓                 ↓
    Paragraph          Breaks           Formatting
        │                │                 │
       <p>              <br>          <b> <strong>
                                      <i> <em>
                                      <u>
        │
        ├───────────────┐
        ↓               ↓
   Preformatted     Quotations
        │               │
      <pre>       <q> <blockquote>
                        │
                        ├── <cite>
                        └── <abbr>
```

### Core idea

> **`<p>` organizes text into paragraphs, `<br>` creates a line break, `<hr>` represents a thematic break, `<pre>` preserves formatting, and text/quotation elements provide different meanings or presentations for text.**
