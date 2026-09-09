# 7. Headings in HTML

HTML provides **six levels of headings**, from `<h1>` to `<h6>`.

```html
<h1>Heading 1</h1>
<h2>Heading 2</h2>
<h3>Heading 3</h3>
<h4>Heading 4</h4>
<h5>Heading 5</h5>
<h6>Heading 6</h6>
```

They are used to organize the content of a webpage into a clear hierarchy.

---

## 7.1 `<h1>` — Main Heading

`<h1>` represents the **highest-level heading**.

Example:

```html
<h1>Web Technologies</h1>
```

If your webpage is about Web Technologies, the main topic can be represented by `<h1>`.

```text
Web Technologies
      ↓
     <h1>
```

---

## 7.2 `<h2>` — Second-Level Heading

`<h2>` represents a heading under the main `<h1>` topic.

Example:

```html
<h1>Web Technologies</h1>

<h2>HTML</h2>

<h2>CSS</h2>

<h2>JavaScript</h2>
```

The hierarchy is:

```text
<h1> Web Technologies
   │
   ├── <h2> HTML
   ├── <h2> CSS
   └── <h2> JavaScript
```

---

## 7.3 `<h3>` — Third-Level Heading

`<h3>` can be used for a subsection under an `<h2>`.

Example:

```html
<h1>Web Technologies</h1>

<h2>HTML</h2>

<h3>HTML Tags</h3>
<h3>HTML Elements</h3>
<h3>HTML Attributes</h3>
```

Structure:

```text
<h1> Web Technologies
   │
   └── <h2> HTML
          │
          ├── <h3> HTML Tags
          ├── <h3> HTML Elements
          └── <h3> HTML Attributes
```

---

## 7.4 `<h4>` — Fourth-Level Heading

`<h4>` represents a lower-level heading.

Example:

```html
<h2>HTML</h2>

<h3>HTML Tags</h3>

<h4>Paired Tags</h4>
<h4>Unpaired Tags</h4>
```

Here `<h4>` is used for subsections under `<h3>`.

---

## 7.5 `<h5>` — Fifth-Level Heading

`<h5>` represents another lower level in the heading hierarchy.

Example:

```html
<h4>Paired Tags</h4>

<h5>Opening Tag</h5>
<h5>Closing Tag</h5>
```

---

## 7.6 `<h6>` — Sixth-Level Heading

`<h6>` is the **lowest heading level** provided by HTML.

Example:

```html
<h5>Opening Tag</h5>

<h6>Example of Opening Tag</h6>
```

---

# 7.7 All Six Headings

```html
<h1>Heading 1</h1>
<h2>Heading 2</h2>
<h3>Heading 3</h3>
<h4>Heading 4</h4>
<h5>Heading 5</h5>
<h6>Heading 6</h6>
```

The hierarchy is:

```text
<h1>
  ↓
<h2>
  ↓
<h3>
  ↓
<h4>
  ↓
<h5>
  ↓
<h6>
```

Think of them as different levels of titles in a book:

```text
Book
│
├── Chapter
│     ├── Section
│     │     ├── Subsection
│     │     │     └── ...
```

---

# 7.8 Important: Heading Level ≠ Just Font Size

A common beginner mistake is to think:

> `<h1>` to `<h6>` are simply different font sizes.

They **do have default visual size differences in browsers**, but their more important purpose is to represent the **hierarchy and structure of the content**.

CSS can change their visual appearance.

For example:

```html
<h1>Main Topic</h1>
<h2>Sub Topic</h2>
```

CSS can make either heading larger, smaller, bold, or otherwise styled.

So:

```text
HTML heading level
        ↓
Content hierarchy/meaning

CSS
        ↓
Visual appearance
```

---

# 7.9 Complete Example

Suppose we are creating notes for Web Technologies:

```html
<h1>Web Technologies</h1>

<h2>HTML</h2>

<h3>HTML Basics</h3>

<h4>HTML Tags</h4>

<h5>Paired Tags</h5>

<h6>Opening and Closing Tags</h6>

<h5>Unpaired Tags</h5>
```

The hierarchy becomes:

```text
<h1> Web Technologies
  │
  └── <h2> HTML
        │
        └── <h3> HTML Basics
              │
              └── <h4> HTML Tags
                    │
                    ├── <h5> Paired Tags
                    │      └── <h6> Opening and Closing Tags
                    │
                    └── <h5> Unpaired Tags
```

This makes the relationship between topics clear.

---

# 7.10 Heading Syntax

All six heading elements follow the same basic syntax:

```html
<h1>Content</h1>
```

```html
<h2>Content</h2>
```

```html
<h3>Content</h3>
```

and so on until:

```html
<h6>Content</h6>
```

General syntax:

```html
<hN>Heading Content</hN>
```

where `N` is from **1 to 6**.

---

# 7.11 Important Rules

### Rule 1: There are six heading levels

```text
<h1> → highest level
<h2>
<h3>
<h4>
<h5>
<h6> → lowest level
```

### Rule 2: Headings are paired elements

For example:

```html
<h1>Welcome</h1>
```

They have:

```text
Opening tag → <h1>
Content      → Welcome
Closing tag  → </h1>
```

### Rule 3: Use headings according to content hierarchy

Don't choose a heading merely because its default text size looks good.

If you need to change appearance, CSS should be used.

---

# 7.12 Common Confusion

### Is `<h1>` the biggest possible HTML heading?

It is the **highest heading level**, but visual size can be changed using CSS.

### Is `<h6>` a paragraph?

No.

`<h6>` is the lowest-level heading.

A paragraph uses:

```html
<p>Some text</p>
```

### Can `<h2>` be used without `<h1>`?

HTML does not technically require every page to contain an `<h1>` before an `<h2>`, but headings should be organized logically according to the document's structure.

### Are `<h1>` and `<h6>` different tags?

Yes. They are six different heading elements representing different heading levels.

---

# 7.13 Quick Revision Table

| Tag    | Heading Level | Typical Role           |
| ------ | ------------: | ---------------------- |
| `<h1>` |             1 | Main topic             |
| `<h2>` |             2 | Major subsection       |
| `<h3>` |             3 | Subsection             |
| `<h4>` |             4 | Lower-level subsection |
| `<h5>` |             5 | Further subsection     |
| `<h6>` |             6 | Lowest heading level   |

---

# 7.14 Final Revision

```text
              HTML HEADINGS
                    │
        ┌───────────┼───────────┐
        ↓           ↓           ↓
       <h1>        <h2>        <h3>
        ↓           ↓           ↓
     Main        Section     Subsection
                                  │
                                  ↓
                         <h4> <h5> <h6>
```

The most important thing to remember:

> **`<h1>` through `<h6>` provide six levels of headings used to organize the content hierarchy of an HTML document.**
