# 4. HTML Elements

An **HTML element** is the complete structure that represents something on a webpage.

The easiest way to understand it is:

> **A tag is the instruction, while an element is the complete thing created using that instruction.**

---

## 4.1 What is an Element?

Consider this HTML:

```html
<p>Hello World</p>
```

This complete structure is called an **HTML element**.

It contains:

```text
<p>          → Opening tag
Hello World  → Content
</p>         → Closing tag
```

So:

```text
Opening Tag + Content + Closing Tag
                    ↓
              HTML Element
```

### Simple definition

> **An HTML element is a complete HTML structure consisting of an opening tag, content, and usually a closing tag.**

For example:

```html
<h1>Welcome</h1>
```

The complete `<h1>Welcome</h1>` is an element.

---

# 4.2 Tag vs Element

This is one of the most common beginner confusions.

Consider:

```html
<p>Hello</p>
```

There are two tags:

```html
<p>
```

and

```html
</p>
```

But the complete structure:

```html
<p>Hello</p>
```

is an **element**.

### Think of it like this

A tag is like an **instruction**.

An element is the **complete result/structure created using that instruction**.

### Comparison

| Tag                  | Element                                          |
| -------------------- | ------------------------------------------------ |
| A markup instruction | Complete HTML structure                          |
| Written using `< >`  | Can contain opening tag, content and closing tag |
| Example: `<p>`       | Example: `<p>Hello</p>`                          |
| Example: `</p>`      | Example: `<h1>Welcome</h1>`                      |

---

# 4.3 Understanding With an Analogy

Imagine a teacher gives you an instruction:

> "Create a box."

That instruction is like a **tag**.

After following the instruction, you have:

```text
┌─────────────────┐
│    HELLO        │
└─────────────────┘
```

That complete box is like an **element**.

Similarly:

```html
<p>Hello</p>
```

The tags provide the instructions, while the complete structure forms the element.

---

# 4.4 Element Structure

Let's take:

```html
<p>Hello World</p>
```

Break it into three parts:

```text
         HTML ELEMENT
              │
      ┌───────┼────────┐
      ↓       ↓        ↓
 Opening    Content   Closing
   Tag                 Tag
      ↓       ↓        ↓
    <p>   Hello World  </p>
```

So the general structure is:

```html
<opening-tag>
    content
</closing-tag>
```

Or when written on one line:

```html
<opening-tag>content</closing-tag>
```

---

# 4.5 Example With a Heading

```html
<h1>Welcome to HTML</h1>
```

Let's identify each part:

```text
<h1>               → Opening tag

Welcome to HTML    → Content

</h1>              → Closing tag
```

Complete element:

```html
<h1>Welcome to HTML</h1>
```

---

# 4.6 Content Inside an Element

The information placed between the opening and closing tags is called the **content** of that element.

Example:

```html
<p>HTML is easy to learn.</p>
```

Here:

```text
<p>                         → Opening tag
HTML is easy to learn.     → Content
</p>                        → Closing tag
```

Therefore:

> **"HTML is easy to learn." is the content of the paragraph element.**

Another example:

```html
<h1>My Website</h1>
```

Here:

```text
<h1>          → Opening tag
My Website    → Content
</h1>         → Closing tag
```

---

# 4.7 Content Can Be More Than Just Text

An element doesn't always have to contain simple text.

For example:

```html
<p>
    Welcome to my website.
</p>
```

The content is text.

But HTML elements can also contain **other elements**.

Example:

```html
<p>
    Welcome to <strong>my website</strong>.
</p>
```

Here the `<strong>` element exists inside the `<p>` element.

This creates a relationship:

```text
<p>
   │
   ├── Welcome to
   │
   ├── <strong>my website</strong>
   │
   └── .
</p>
```

This concept of putting one element inside another is called **nesting**, which we will study later.

---

# 4.8 Element With No Content

Some HTML elements don't have content between an opening and closing tag.

For example:

```html
<br>
```

This represents a line break.

Similarly:

```html
<hr>
```

represents a thematic break.

These are **void/empty elements** and don't have normal closing tags.

So not every HTML element follows:

```html
<opening>content</closing>
```

Some are simply:

```html
<br>
```

or:

```html
<hr>
```

---

# 4.9 Tag vs Element — Very Easy Example

Consider:

```html
<h1>Hello</h1>
```

### Tags

```html
<h1>
</h1>
```

### Content

```text
Hello
```

### Element

```html
<h1>Hello</h1>
```

Remember:

```text
TAG
 ↓
Instruction

ELEMENT
 ↓
Complete structure
```

---

# 4.10 Multiple Elements

A webpage normally contains many elements.

Example:

```html
<h1>Student Details</h1>

<p>This page contains student information.</p>

<p>Students can view their details here.</p>
```

There are three elements:

```text
Element 1 → <h1>Student Details</h1>

Element 2 → <p>This page contains student information.</p>

Element 3 → <p>Students can view their details here.</p>
```

Each element represents a particular part of the webpage.

---

# 4.11 Complete Example

```html
<h1>My College</h1>

<p>Welcome to my college website.</p>

<p>We offer several courses.</p>

<hr>

<p>Contact us for more information.</p>
```

We can identify the elements:

```text
<h1>My College</h1>
        ↓
      Element

<p>Welcome to my college website.</p>
        ↓
      Element

<p>We offer several courses.</p>
        ↓
      Element

<hr>
        ↓
      Element

<p>Contact us for more information.</p>
        ↓
      Element
```

---

# 4.12 Important Difference: Tag and Element

Let's make it extremely clear.

Suppose we have:

```html
<p>Hello</p>
```

### `<p>`

This is an **opening tag**.

### `</p>`

This is a **closing tag**.

### `Hello`

This is the **content**.

### `<p>Hello</p>`

This is the **complete element**.

So:

```text
Opening Tag
     +
 Content
     +
Closing Tag
     ↓
HTML Element
```

---

# 4.13 Common Mistakes

### Mistake 1

Calling `<p>Hello</p>` only a tag.

❌ Incorrect.

The complete structure is an **element**.

---

### Mistake 2

Calling `<p>` an element.

In basic terminology:

```html
<p>
```

is the **opening tag**.

The complete element is:

```html
<p>Hello</p>
```

---

### Mistake 3

Thinking content and element are the same.

They are different.

```html
<p>Hello</p>
```

```text
Hello           → Content

<p>Hello</p>    → Element
```

---

# 4.14 Quick Revision Table

| Part             | Example        | Meaning                        |
| ---------------- | -------------- | ------------------------------ |
| Opening tag      | `<p>`          | Starts the element             |
| Content          | `Hello`        | Information inside the element |
| Closing tag      | `</p>`         | Ends the element               |
| Complete element | `<p>Hello</p>` | Complete HTML structure        |

---

# 4.15 Final Mental Picture

```text
                 HTML ELEMENT
                      │
          ┌───────────┼───────────┐
          ↓           ↓           ↓
       Opening      Content     Closing
         Tag                      Tag
          ↓           ↓           ↓
        <p>         Hello        </p>
          └───────────┬───────────┘
                      ↓
              <p>Hello</p>
                      ↓
               COMPLETE ELEMENT
```

### Remember this sentence

> **Tag = instruction.**

> **Element = complete structure made using the tag.**

And for:

```html
<p>Hello World</p>
```

remember:

```text
<p>          → Opening tag
Hello World  → Content
</p>         → Closing tag
Entire thing → Element
```
