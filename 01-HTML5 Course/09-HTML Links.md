# 9. HTML Links

A webpage is rarely alone. Usually, we need to move from one webpage to another.

For example:

```text
Home → About → Courses → Contact
```

HTML provides the **anchor (`<a>`) element** to create these links.

A link is like a **door**: when you click it, the browser can take you to another place.

---

## 9.1 Anchor Tag — `<a>`

The `<a>` element is used to create a **hyperlink**.

### Basic syntax

```html
<a href="destination">Link Text</a>
```

For example:

```html
<a href="about.html">About Us</a>
```

Here:

```text
<a>             → Anchor element
href            → Destination
About Us        → Text the user clicks
```

The user sees:

```text
About Us
```

and can click it.

---

# 9.2 Understanding the `<a>` Element

Consider:

```html
<a href="about.html">About Us</a>
```

Break it into parts:

```text
<a href="about.html">    → Opening tag
About Us                 → Link text
</a>                     → Closing tag
```

The complete structure is an **anchor element**.

Notice that `href` is written inside the opening tag.

```text
<a
 └── href="about.html"
>
```

`href` is an **attribute** of the `<a>` element.

---

# 9.3 What is `href`?

`href` stands for **Hypertext Reference**.

It specifies the **destination of the link**.

Example:

```html
<a href="about.html">About Us</a>
```

Here:

```text
href="about.html"
       ↓
Destination
```

So when the user clicks **About Us**, the browser knows where the link should go.

### Easy way to remember

```text
<a>     → Creates the door
href    → Tells the door where to go
```

---

# 9.4 Linking to Another Page

Suppose your website has these files:

```text
website/
│
├── index.html
├── about.html
└── contact.html
```

You are currently on `index.html`.

You can create a link to `about.html`:

```html
<a href="about.html">About Us</a>
```

When the user clicks:

```text
About Us
   ↓
about.html
```

The browser opens the other page.

---

## Example

### `index.html`

```html
<h1>My Website</h1>

<a href="about.html">About Us</a>
<a href="contact.html">Contact Us</a>
```

The user can navigate between the pages.

---

# 9.5 Linking to Another Website

A link doesn't have to point to another page in your own website.

It can point to a completely different website.

Example:

```html
<a href="https://www.google.com">Google</a>
```

When the user clicks:

```text
Google
  ↓
https://www.google.com
  ↓
Google website
```

Another example:

```html
<a href="https://www.wikipedia.org">Wikipedia</a>
```

The destination is an external website.

---

# 9.6 Internal vs External Links

### Internal Link

A link to another page within the same website.

```html
<a href="about.html">About Us</a>
```

Think:

```text
My Website
   │
   ├── Home
   ├── About
   └── Contact
```

The link connects pages within the same website.

---

### External Link

A link to another website.

```html
<a href="https://www.google.com">Google</a>
```

Think:

```text
My Website
     │
     ↓
Another Website
```

---

# 9.7 What is `target`?

The `target` attribute specifies **where the linked document should be opened**.

Example:

```html
<a href="about.html" target="_blank">About Us</a>
```

Here:

```text
href
 ↓
Where should I go?

target
 ↓
Where/how should I open it?
```

Your notes specifically cover:

```text
_self
_blank
```

---

# 9.8 `target="_self"`

`target="_self"` opens the linked document in the **same browsing context**, normally the current tab.

Example:

```html
<a href="about.html" target="_self">About Us</a>
```

Flow:

```text
Current Page
     ↓
Click link
     ↓
About Page
     ↓
Same tab
```

### Important

`_self` is generally the default target behavior for a normal link.

So this:

```html
<a href="about.html">About Us</a>
```

normally behaves like:

```html
<a href="about.html" target="_self">About Us</a>
```

---

# 9.9 `target="_blank"`

`target="_blank"` tells the browser to open the linked document in a **new browsing context**, commonly a new tab.

Example:

```html
<a href="https://www.google.com" target="_blank">
    Google
</a>
```

Flow:

```text
Current Page
     │
     ├──────────────→ stays open
     │
     └── Click link
             ↓
        New tab/context
             ↓
           Google
```

So the original page remains available while the destination opens separately.

---

# 9.10 `_self` vs `_blank`

| Target   | Where the link opens                     |
| -------- | ---------------------------------------- |
| `_self`  | Current browsing context/tab             |
| `_blank` | New browsing context, commonly a new tab |

### Easy memory

```text
_self
 ↓
Same

_blank
 ↓
New
```

---

# 9.11 Complete Example

```html
<!DOCTYPE html>

<html>

<head>
    <title>HTML Links</title>
</head>

<body>

    <h1>My Website</h1>

    <a href="about.html">About Us</a>

    <br><br>

    <a href="contact.html" target="_self">
        Contact Us
    </a>

    <br><br>

    <a href="https://www.google.com" target="_blank">
        Google
    </a>

</body>

</html>
```

There are three links here.

### Link 1

```html
<a href="about.html">About Us</a>
```

Goes to another page of the same website.

---

### Link 2

```html
<a href="contact.html" target="_self">
    Contact Us
</a>
```

Opens the contact page in the current browsing context.

---

### Link 3

```html
<a href="https://www.google.com" target="_blank">
    Google
</a>
```

Links to another website and requests a new browsing context.

---

# 9.12 Step-by-Step: What Happens When You Click a Link?

Suppose we have:

```html
<a href="about.html">About Us</a>
```

### Step 1

Browser displays:

```text
About Us
```

### Step 2

User clicks the text.

### Step 3

Browser reads:

```text
href="about.html"
```

### Step 4

Browser navigates to the specified destination.

```text
Current Page
     ↓
about.html
```

That's the basic job of an HTML link.

---

# 9.13 Link Text

The text between `<a>` and `</a>` is what the user normally clicks.

Example:

```html
<a href="about.html">About Us</a>
```

Here:

```text
href="about.html" → Destination

About Us          → Link text
```

You can change the link text:

```html
<a href="about.html">Learn More</a>
```

The destination is still:

```text
about.html
```

but the displayed clickable text is now:

```text
Learn More
```

---

# 9.14 Link to an External Website

A complete external URL can be placed in `href`.

```html
<a href="https://example.com">
    Visit Example
</a>
```

The important difference is:

```text
Internal:
about.html

External:
https://example.com
```

---

# 9.15 Common Mistakes

### Mistake 1 — Forgetting `href`

```html
<a>Google</a>
```

This creates an anchor element, but without a destination it does not provide the normal navigation behavior of a link.

Usually you need:

```html
<a href="https://www.google.com">Google</a>
```

---

### Mistake 2 — Putting `href` outside the tag

Incorrect:

```html
<a> href="about.html" About </a>
```

Correct:

```html
<a href="about.html">About</a>
```

The `href` attribute belongs inside the opening `<a>` tag.

---

### Mistake 3 — Confusing `href` and `target`

Remember:

```text
href
 ↓
Where to go?

target
 ↓
Where/how to open it?
```

Example:

```html
<a href="about.html" target="_blank">
    About
</a>
```

Here:

```text
href="_..."    → Destination
target="_blank" → Opening context
```

---

# 9.16 Quick Revision

```text
                <a>
                 │
        Creates a hyperlink
                 │
          ┌──────┴──────┐
          ↓             ↓
        href          target
          ↓             ↓
   Where to go?    Where to open?
                        │
                 ┌──────┴──────┐
                 ↓             ↓
              _self         _blank
                 ↓             ↓
              Same          New
```

---

# 9.17 Important Examples

### Link to another page

```html
<a href="about.html">About Us</a>
```

### Link to another page using `_self`

```html
<a href="about.html" target="_self">About Us</a>
```

### Link to another website

```html
<a href="https://www.google.com">Google</a>
```

### Link to another website using `_blank`

```html
<a href="https://www.google.com" target="_blank">
    Google
</a>
```

---

# 9.18 Final Revision Table

| Concept           | Meaning                                             | Example               |
| ----------------- | --------------------------------------------------- | --------------------- |
| `<a>`             | Creates a hyperlink                                 | `<a>...</a>`          |
| `href`            | Specifies destination                               | `href="about.html"`   |
| Internal link     | Links to another page/resource in your site         | `about.html`          |
| External link     | Links to another website                            | `https://example.com` |
| `target="_self"`  | Opens in current browsing context                   | `target="_self"`      |
| `target="_blank"` | Opens in a new browsing context, commonly a new tab | `target="_blank"`     |

### Core idea

> **`<a>` creates the link, `href` tells the browser where the link should go, and `target` tells the browser where the destination should be opened.**

```text
<a href="about.html" target="_self">
    About Us
</a>
```

Think:

**`<a>` = Door**
**`href` = Destination**
**`target` = Which place/window to open it in**
