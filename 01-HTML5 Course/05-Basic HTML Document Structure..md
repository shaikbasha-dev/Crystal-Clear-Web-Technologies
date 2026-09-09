# 5. Basic HTML Document Structure

Before writing individual HTML tags, we need to understand the **basic structure of an HTML document**.

Think of an HTML document like a **container with different sections**. Each section has a specific purpose.

A basic HTML document looks like this:

```html
<!DOCTYPE html>

<html>

<head>
    <title>My Page</title>
</head>

<body>
    Content
</body>

</html>
```

Let's understand every part one by one.

---

## 5.1 `<!DOCTYPE html>`

The first line is:

```html
<!DOCTYPE html>
```

This is called the **DOCTYPE declaration**.

It tells the browser:

> "This document is intended to be interpreted as an HTML document using the modern HTML standard."

### Important

`<!DOCTYPE html>` is **not an HTML element**.

It is a **document type declaration**.

Also notice:

```text
<!DOCTYPE html>
```

is written using:

```text
<! ... >
```

rather than a normal opening/closing tag pair.

---

## 5.2 `<html>`

Next we have:

```html
<html>
```

This is the **root element** of the HTML document.

The entire HTML document is placed inside it.

Example:

```html
<html>

    Everything in the HTML document

</html>
```

So the basic relationship is:

```text
<html>
   ↓
Entire HTML document
</html>
```

The `<html>` element contains two major parts:

```text
<html>
   │
   ├── <head>
   │
   └── <body>
</html>
```

---

# 5.3 `<head>`

The `<head>` element contains information about the HTML document that is generally **not displayed as the main visible page content**.

Example:

```html
<head>
    <title>My Page</title>
</head>
```

The `<head>` section can contain things such as:

* The page title
* Metadata
* Links to CSS files
* Other information needed by the browser

For now, the important thing to remember is:

> **`<head>` contains information and resources about the document.**

---

# 5.4 `<title>`

Inside `<head>`, we can write:

```html
<title>My Page</title>
```

The `<title>` element specifies the **title of the document**.

For example:

```html
<head>
    <title>My Page</title>
</head>
```

The text:

```text
My Page
```

is used as the document's title, such as in the browser tab.

### Important distinction

The `<title>` is **not the same thing as a heading displayed inside the webpage**.

Compare:

```html
<title>My Page</title>
```

with:

```html
<h1>Welcome to My Page</h1>
```

`<title>` belongs in the document's `<head>` and sets the document title.

`<h1>` is visible page content placed in the `<body>`.

---

# 5.5 `<body>`

The `<body>` element contains the **main content of the webpage**.

For example:

```html
<body>

    Welcome to my webpage.

</body>
```

Things that users normally see on the webpage are placed inside `<body>`.

For example:

```html
<body>

    <h1>Welcome</h1>

    <p>This is my webpage.</p>

    <button>Click Me</button>

</body>
```

The body can contain:

* Headings
* Paragraphs
* Images
* Links
* Tables
* Forms
* Buttons
* Lists
* And many other HTML elements

---

# 5.6 Proper Opening and Closing Structure

Now let's look carefully at the complete structure:

```html
<!DOCTYPE html>

<html>

<head>
    <title>My Page</title>
</head>

<body>
    Content
</body>

</html>
```

Notice how the elements are properly opened and closed.

```text
<html>
    <head>
        <title>My Page</title>
    </head>

    <body>
        Content
    </body>
</html>
```

The structure is **nested**.

That means one element is placed inside another element.

---

# 5.7 Understanding the Nesting

Look at:

```html
<html>

    <head>
        <title>My Page</title>
    </head>

    <body>
        Content
    </body>

</html>
```

We can visualize it like this:

```text
<html>
   │
   ├── <head>
   │      │
   │      └── <title>
   │
   └── <body>
          │
          └── Content
```

So:

```text
<html>
   │
   ├── head
   │      └── title
   │
   └── body
```

---

# 5.8 Why Proper Structure Matters

Imagine you have boxes inside boxes:

```text
Big Box
 ├── Small Box
 │     └── Tiny Box
 └── Another Box
```

You need to keep them properly organized.

HTML works similarly.

For example:

```html
<html>
    <head>
        <title>My Page</title>
    </head>

    <body>
        Content
    </body>
</html>
```

The opening and closing tags correctly define where each element begins and ends.

---

# 5.9 Opening and Closing Tags

Let's identify them.

### HTML

```html
<html>
```

Opening tag:

```html
<html>
```

Closing tag:

```html
</html>
```

---

### Head

```html
<head>
```

Opening tag:

```html
<head>
```

Closing tag:

```html
</head>
```

---

### Title

```html
<title>My Page</title>
```

Opening tag:

```html
<title>
```

Content:

```text
My Page
```

Closing tag:

```html
</title>
```

---

### Body

```html
<body>
    Content
</body>
```

Opening tag:

```html
<body>
```

Closing tag:

```html
</body>
```

---

# 5.10 Complete Structure Breakdown

Here is the complete document again:

```html
<!DOCTYPE html>

<html>

<head>
    <title>My Page</title>
</head>

<body>

    Content

</body>

</html>
```

Now identify each part:

| Part              | Purpose                                 |
| ----------------- | --------------------------------------- |
| `<!DOCTYPE html>` | Declares the document type              |
| `<html>`          | Root element                            |
| `<head>`          | Contains document information/resources |
| `<title>`         | Specifies the document title            |
| `<body>`          | Contains the main webpage content       |

---

# 5.11 What Does the Browser Do?

When the browser receives this document:

```html
<!DOCTYPE html>

<html>

<head>
    <title>My Page</title>
</head>

<body>
    Content
</body>

</html>
```

it understands the document structure.

Conceptually:

```text
HTML Document
      ↓
<!DOCTYPE html>
      ↓
<html>
   ↓
   ├── head
   │    ↓
   │   title
   │
   └── body
        ↓
      Content
```

The browser then uses this structure to display the webpage.

---

# 5.12 A More Practical Example

Let's create a small webpage:

```html
<!DOCTYPE html>

<html>

<head>
    <title>Student Page</title>
</head>

<body>

    <h1>Student Information</h1>

    <p>Welcome to the student page.</p>

</body>

</html>
```

Here:

```text
<!DOCTYPE html>
        ↓
Document type

<html>
        ↓
Entire HTML document

<head>
        ↓
Document information

<title>
        ↓
Browser/document title

<body>
        ↓
Visible webpage content

<h1>
        ↓
Heading

<p>
        ↓
Paragraph
```

---

# 5.13 The Most Important Structure to Memorize

```text
                    HTML DOCUMENT
                          │
                          ↓
                   <!DOCTYPE html>
                          │
                          ↓
                       <html>
                          │
              ┌───────────┴───────────┐
              ↓                       ↓
            <head>                  <body>
              │                       │
              ↓                       ↓
           <title>               Page Content
              │
              ↓
          My Page
```

Or simply:

```text
<!DOCTYPE html>
        ↓
<html>
   ├── <head>
   │      └── <title>
   │
   └── <body>
          └── Content
</html>
```

---

# 5.14 Common Confusions

### Is `<!DOCTYPE html>` a tag?

No.

It is a **DOCTYPE declaration**, not a normal HTML element.

---

### Is `<html>` the first visible thing on the webpage?

No.

`<html>` is the root element that contains the document.

---

### Is `<head>` visible on the webpage?

The contents of `<head>` are generally not the main visible page content.

The `<head>` contains document information and resources.

---

### Is `<title>` displayed inside the webpage?

No. The `<title>` specifies the document title, commonly seen in the browser tab.

---

### Where do we put visible webpage content?

Inside:

```html
<body>
    ...
</body>
```

---

# 5.15 Final Revision

Remember this structure:

```html
<!DOCTYPE html>

<html>

<head>
    <title>My Page</title>
</head>

<body>
    Content
</body>

</html>
```

And remember the job of each part:

```text
<!DOCTYPE html>
        ↓
Document type

<html>
        ↓
Root/container of the document

<head>
        ↓
Document information

<title>
        ↓
Document title

<body>
        ↓
Main webpage content
```

### One-line memory trick

> **DOCTYPE tells the browser what type of document it is, `<html>` contains the whole document, `<head>` contains document information, `<title>` gives the document its title, and `<body>` contains the main webpage content.**
