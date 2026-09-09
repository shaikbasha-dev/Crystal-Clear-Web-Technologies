# 3. HTML Tags

HTML tags are the **basic building blocks of HTML**.

When we create a webpage, we need a way to tell the browser what each piece of content represents.

For example:

```html
<h1>Welcome</h1>
<p>This is my webpage.</p>
```

Here, `<h1>` tells the browser that **Welcome is a heading**, while `<p>` tells the browser that the text is a **paragraph**.

---

## 3.1 What is a Tag?

An HTML **tag** is a special keyword written inside **angle brackets `< >`** that tells the browser how to interpret or structure content.

Example:

```html
<p>
```

This is a paragraph tag.

```html
<h1>
```

This is a heading tag.

```html
<br>
```

This is a line-break tag.

### Simple definition

> **An HTML tag is a markup instruction written inside angle brackets that tells the browser how to interpret or structure content.**

---

# 3.2 Why Are Tags Required?

Imagine you give the browser only this:

```text
Welcome to My Website
This is my first webpage.
```

The browser sees text, but HTML needs to identify what each piece of content represents.

We can use tags:

```html
<h1>Welcome to My Website</h1>

<p>This is my first webpage.</p>
```

Now the browser understands:

```text
<h1> → This is a heading
<p>  → This is a paragraph
```

So tags are required because they provide **structure and meaning to webpage content**.

### Think of tags as labels

Imagine you have several boxes:

```text
┌───────────────┐
│  Books        │
└───────────────┘

┌───────────────┐
│  Clothes      │
└───────────────┘

┌───────────────┐
│  Shoes        │
└───────────────┘
```

The labels tell you what is inside each box.

Similarly, HTML tags help the browser understand the role of the content.

---

# 3.3 Angle Brackets `< >`

HTML tags are written using **angle brackets**.

There are two symbols:

```text
<    <
>    >
```

Together:

```text
< >
```

For example:

```html
<p>
```

Here:

```text
<  → beginning of the tag syntax
p  → tag name
>  → end of the tag syntax
```

Similarly:

```html
<h1>
```

contains:

```text
< → opening angle bracket
h1 → tag name
> → closing angle bracket
```

### Important

The `<` and `>` symbols are part of HTML tag syntax.

---

# 3.4 Opening Tag

An **opening tag** indicates the beginning of an HTML element.

Example:

```html
<p>
```

Here:

```text
< → opening angle bracket
p → tag name
> → closing angle bracket
```

Another example:

```html
<h1>
```

The opening tag tells the browser:

> "The content belonging to this element starts here."

---

# 3.5 Closing Tag

A **closing tag** indicates the end of an HTML element.

Example:

```html
</p>
```

Notice the `/`.

Compare:

```html
<p>
```

and

```html
</p>
```

### Opening tag

```html
<p>
```

### Closing tag

```html
</p>
```

The `/` indicates that the tag is being closed.

Another example:

```html
<h1>
Welcome
</h1>
```

Here:

```text
<h1>      → Opening tag
Welcome   → Content
</h1>     → Closing tag
```

---

# 3.6 Complete Structure of a Paired Tag

Consider:

```html
<p>Hello</p>
```

Break it down:

```text
<p>       → Opening tag

Hello     → Content

</p>      → Closing tag
```

Together:

```text
Opening tag + Content + Closing tag
```

forms an HTML element.

So:

```html
<p>Hello</p>
```

is an HTML element consisting of a paragraph tag and its content.

---

# 3.7 Paired Tags

Some HTML tags come in **pairs**.

They have:

1. Opening tag
2. Closing tag

Example:

```html
<p>Hello</p>
```

Another example:

```html
<h1>Welcome</h1>
```

### More examples

```html
<p>Paragraph</p>

<h1>Heading</h1>

<h2>Sub Heading</h2>
```

The general pattern is:

```html
<tagname>
    Content
</tagname>
```

### Why are they called paired tags?

Because the opening and closing tags work together as a pair.

---

# 3.8 Example: `<p></p>`

```html
<p>Hello World</p>
```

Here:

```text
<p>          → Opening tag
Hello World  → Content
</p>         → Closing tag
```

The browser understands that **Hello World is a paragraph**.

---

# 3.9 Example: `<h1></h1>`

```html
<h1>Welcome</h1>
```

Here:

```text
<h1>       → Opening tag
Welcome    → Content
</h1>      → Closing tag
```

The browser understands that **Welcome is a level-1 heading**.

---

# 3.10 Unpaired / Empty Tags

Not every HTML tag needs a closing tag.

Some tags do not contain content between an opening and closing tag.

These are commonly called:

* **Unpaired tags**
* **Empty elements**
* **Void elements**

Examples from your topic are:

```html
<br>
<hr>
```

---

# 3.11 `<br>` Tag

`<br>` represents a **line break**.

Suppose we write:

```html
<p>
Hello
World
</p>
```

HTML whitespace and line breaks do not necessarily produce the visual line break you might expect.

Using `<br>`:

```html
<p>
Hello<br>
World
</p>
```

The browser displays the text on separate lines:

```text
Hello
World
```

### Important point

`<br>` does not need a separate closing tag.

We don't normally write:

```html
<br></br>
```

The tag itself represents the line break.

---

# 3.12 `<hr>` Tag

`<hr>` represents a thematic break, commonly displayed by browsers as a horizontal line.

Example:

```html
<h1>Chapter 1</h1>

<hr>

<p>This is the content of Chapter 1.</p>
```

The browser can display a horizontal dividing line between the sections.

Like `<br>`, `<hr>` is an empty/void element and does not have a normal closing tag.

---

# 3.13 Paired vs Unpaired Tags

| Paired Tags                   | Unpaired / Empty Tags               |
| ----------------------------- | ----------------------------------- |
| Have opening and closing tags | Do not have a separate closing tag  |
| Usually contain content       | Do not contain content between tags |
| Work as a pair                | Stand alone                         |
| `<p></p>`                     | `<br>`                              |
| `<h1></h1>`                   | `<hr>`                              |

### Easy memory

```text
PAIRED
↓
Start + Content + End

<p>
Hello
</p>
```

```text
UNPAIRED
↓
One tag

<br>
```

---

# 3.14 Examples of HTML Tags

The examples in this topic include:

### Paragraph

```html
<p>Welcome</p>
```

### Heading

```html
<h1>Welcome</h1>
```

### Line Break

```html
<br>
```

### Horizontal Rule

```html
<hr>
```

---

# 3.15 Quick Comparison

```text
<p>Welcome</p>
```

```text
Opening       Content       Closing
  ↓             ↓              ↓
 <p>         Welcome          </p>
```

Whereas:

```text
<br>
```

has only the tag itself.

---

# 3.16 Common Confusion

### Is `<p>` an opening tag or a complete paragraph?

`<p>` by itself is the **opening tag**.

```html
<p>Hello</p>
```

The complete structure represents the **paragraph element**.

---

### Is `</p>` an opening tag?

No.

```html
</p>
```

is the **closing tag**.

The `/` is the important difference.

---

### Is `<br>` a paired tag?

No.

```html
<br>
```

is an **empty/void element**.

It doesn't require a normal closing tag.

---

### Is `<h1>` the content?

No.

```html
<h1>Welcome</h1>
```

Here:

```text
<h1>       → Opening tag
Welcome    → Content
</h1>      → Closing tag
```

---

# 3.17 One Important Distinction

Don't confuse **tag** and **element**.

Consider:

```html
<p>Hello</p>
```

The tags are:

```html
<p>
</p>
```

The complete element is:

```html
<p>Hello</p>
```

So remember:

> **Tag = markup instruction**

> **Element = complete HTML structure**

We will study this distinction in detail in the next topic.

---

# 3.18 Final Revision

```text
HTML TAG
   ↓
Written inside < >
   ↓
Tells browser about structure/content
   ↓
        ┌───────────────┐
        ↓               ↓
    Paired          Unpaired
        ↓               ↓
 Opening +          Stand-alone
 Closing tag           tag
        ↓               ↓
 <p></p>             <br>
 <h1></h1>           <hr>
```

### Remember these four examples

```html
<p>Paragraph</p>
```

**Paired tag**

```html
<h1>Heading</h1>
```

**Paired tag**

```html
<br>
```

**Unpaired/empty tag**

```html
<hr>
```

**Unpaired/empty tag**

### The core idea

> **HTML tags are instructions written inside angle brackets that help the browser understand and structure webpage content.**
