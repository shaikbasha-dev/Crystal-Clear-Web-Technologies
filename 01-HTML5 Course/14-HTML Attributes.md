# 14. HTML Attributes

Before learning attributes, remember one very important idea:

> **A tag tells the browser what something is. An attribute gives that tag extra information about how it should behave or what information it should contain.**

For example:

```html
<img src="photo.jpg">
```

Here:

* `<img>` → tells the browser **"this is an image"**
* `src="photo.jpg"` → tells the browser **"this is where the image is located"**

So `src` is an **attribute**.

---

# 1. What is an Attribute?

An **attribute** provides additional information about an HTML element.

Attributes are normally written **inside the opening tag**.

### General syntax

```html
<tag attribute="value">
```

For example:

```html
<img src="photo.jpg">
```

Structure:

```text
<img
 │
 └── src="photo.jpg"
       │       │
   attribute  value
```

Another example:

```html
<a href="about.html" target="_blank">
    About
</a>
```

Here:

* `href` → attribute
* `"about.html"` → attribute value
* `target` → attribute
* `"_blank"` → attribute value

---

# 2. Why Do We Need Attributes?

A tag alone may not provide enough information.

For example:

```html
<img>
```

The browser knows:

> "This is supposed to be an image."

But it doesn't know **which image** to display.

So we provide:

```html
<img src="photo.jpg">
```

Now the browser knows:

> "Display the image located at `photo.jpg`."

Therefore:

```text
Tag       → What is it?
Attribute → Extra information about it
```

---

# 3. Attribute Structure

Look carefully:

```html
<img src="photo.jpg">
```

It can be broken into:

```text
<img     src     =     "photo.jpg"
 │       │             │
Tag   Attribute      Value
```

The basic pattern is:

```html
attribute="value"
```

For example:

```html
src="photo.jpg"
```

```text
src          → attribute name
=            → assignment
"photo.jpg"  → attribute value
```

---

# 4. Where Are Attributes Written?

Attributes are written inside the **opening tag**.

✅ Correct:

```html
<img src="photo.jpg">
```

For an element with opening and closing tags:

```html
<a href="home.html">Home</a>
```

The attribute is inside:

```html
<a href="home.html">
```

Not inside the closing tag.

---

# 5. Important Attributes From Your Notes

The attributes specifically listed in your notes are:

```text
src
width
height
target
type
border
required
placeholder
id
name
pattern
```

Let's understand each one.

---

# 6. `src` Attribute

`src` means **source**.

It specifies the location/source of a resource.

You have already seen it with images and multimedia.

### Image example

```html
<img src="photo.jpg">
```

Here:

```text
src → tells the browser where the image is.
```

### Audio example

```html
<audio controls>
    <source src="song.mp3" type="audio/mpeg">
</audio>
```

### Video example

```html
<video controls>
    <source src="movie.mp4" type="video/mp4">
</video>
```

### Memory

**`src` → Source → Where is the file?**

---

# 7. `width` Attribute

`width` specifies the width of an element in contexts where that HTML attribute applies, such as images and videos.

### Image

```html
<img src="photo.jpg" width="400">
```

### Video

```html
<video width="600">
    <source src="movie.mp4" type="video/mp4">
</video>
```

Think:

```text
width
←────────────→
```

### Memory

**`width` → How wide?**

---

# 8. `height` Attribute

`height` specifies the height.

Example:

```html
<img src="photo.jpg" height="300">
```

Video:

```html
<video width="600" height="400">
    <source src="movie.mp4" type="video/mp4">
</video>
```

Think:

```text
      ↑
      │
 height
      │
      ↓
```

### Memory

**`height` → How tall?**

---

# 9. `target` Attribute

The `target` attribute is commonly used with the `<a>` element to specify **where the linked document should open**.

Example:

```html
<a href="about.html" target="_blank">
    About
</a>
```

Here:

```text
href   → Where should I go?
target → Where should I open it?
```

---

# 10. `_self`

`target="_self"` means the link opens in the **same browsing context**, normally the current tab.

Example:

```html
<a href="about.html" target="_self">
    About
</a>
```

Conceptually:

```text
Current Tab
    │
    └── click link
           ↓
      About page
      in same tab
```

`_self` is also the default target behavior for ordinary links when no other target is specified.

---

# 11. `_blank`

`target="_blank"` requests that the linked document open in a **new browsing context**, commonly a new tab.

Example:

```html
<a href="https://example.com" target="_blank">
    Visit Website
</a>
```

Conceptually:

```text
Current Tab
     │
     └── click link
            ↓
       New Tab
            ↓
       Website
```

### Memory

```text
_self  → Same tab
_blank → New tab
```

---

# 12. `type` Attribute

The `type` attribute can tell the browser what **type of resource or input** is being used, depending on the element.

You have already seen it with `<source>`.

### Audio

```html
<source src="song.mp3" type="audio/mpeg">
```

Here:

```text
src  → where is the file?
type → what type of file is it?
```

### Video

```html
<source src="movie.mp4" type="video/mp4">
```

---

## `type` with `<input>`

`type` is also very important with forms.

Example:

```html
<input type="text">
```

This creates a text input.

Other examples:

```html
<input type="email">
```

```html
<input type="password">
```

```html
<input type="number">
```

```html
<input type="submit">
```

So with `<input>`:

```text
type → What kind of input should this be?
```

---

# 13. `border` Attribute

In basic HTML examples, the `border` attribute can be used with `<table>` to specify a table border.

Example:

```html
<table border="1">
```

Conceptually:

```text
┌──────────┬──────┐
│ Name     │ Age  │
├──────────┼──────┤
│ Ravi     │ 22   │
└──────────┴──────┘
```

The value:

```html
border="1"
```

indicates a border.

### Important modern note

For modern web development, table borders and presentation are normally handled using **CSS** rather than the old HTML `border` attribute.

But because `border` is specifically present in your notes, you should understand its basic usage:

```html
<table border="1">
```

---

# 14. `required` Attribute

`required` is commonly used with form controls.

It tells the browser:

> **"The user must provide a value before submitting the form."**

Example:

```html
<input type="text" required>
```

If the user leaves it empty and tries to submit the form, the browser can prevent submission and ask the user to fill it.

---

## Example

```html
<form>

    <label>Name:</label>
    <input type="text" required>

    <input type="submit">

</form>
```

The name field is required.

### Important point

`required` is a **boolean attribute**.

You will commonly see:

```html
<input required>
```

rather than needing a value such as:

```html
<input required="true">
```

---

# 15. `placeholder` Attribute

`placeholder` displays a **temporary hint** inside an input field.

Example:

```html
<input type="text" placeholder="Enter your name">
```

The user sees something like:

```text
┌──────────────────────────────┐
│ Enter your name              │
└──────────────────────────────┘
```

When the user starts typing, the placeholder normally disappears.

### Another example

```html
<input type="email" placeholder="Enter your email">
```

The placeholder gives the user a hint about what to enter.

### Important:

`placeholder` is **not the actual value** entered by the user.

Think:

> **Placeholder = temporary instruction/hint.**

---

# 16. `id` Attribute

The `id` attribute gives an HTML element a **unique identifier** within the page.

Example:

```html
<p id="message">Hello</p>
```

Here:

```text
id = "message"
```

identifies that particular element.

JavaScript can later use this ID to find the element:

```javascript
document.getElementById("message");
```

CSS can also use an ID selector:

```css
#message {
    color: red;
}
```

### Important rule

An `id` should normally be **unique on a page**.

For example:

```html
<input id="username">
```

is a good use.

---

# 17. `name` Attribute

The `name` attribute gives a form control a **name/identifier used when form data is submitted**.

Example:

```html
<input type="text" name="username">
```

Here:

```text
name = username
```

When form data is sent, the field's name is used as the key for that value.

For example, conceptually:

```text
username = Ravi
```

### Example

```html
<form>

    <input type="text" name="username">
    <input type="email" name="email">

</form>
```

The controls have names:

```text
username
email
```

---

# 18. `id` vs `name`

This is a very important distinction.

| `id`                                  | `name`                                                |
| ------------------------------------- | ----------------------------------------------------- |
| Identifies an element in the document | Names a form control for form submission/data         |
| Normally unique on the page           | Multiple controls can share a `name` when appropriate |
| Commonly used by CSS and JavaScript   | Important for form data                               |
| Example: `id="username"`              | Example: `name="username"`                            |

You will often see both together:

```html
<input type="text" id="username" name="username">
```

This is completely normal.

---

# 19. `pattern` Attribute

The `pattern` attribute is used with applicable form controls to specify a **regular-expression pattern that the entered value must match**.

It is useful for validation.

For example:

```html
<input type="text" pattern="[A-Za-z]+">
```

This pattern means the value should contain letters from `A-Z` or `a-z`.

So:

```text
Ravi
John
Mahaboob
```

can match the pattern.

But a value containing digits such as:

```text
Ravi123
```

does not match that particular pattern.

---

# 20. `pattern` + `required`

These attributes can work together.

```html
<input 
    type="text"
    name="username"
    placeholder="Enter username"
    pattern="[A-Za-z]+"
    required>
```

Now:

```text
type        → Text input
name        → username
placeholder → Hint to user
pattern     → Required format
required    → Value cannot be empty
```

---

# 21. A Complete Form Example Using Your Attributes

Let's combine several attributes:

```html
<!DOCTYPE html>
<html>

<head>
    <title>HTML Attributes</title>
</head>

<body>

<form>

    <label for="username">Username:</label>

    <input
        type="text"
        id="username"
        name="username"
        placeholder="Enter your username"
        pattern="[A-Za-z]+"
        required>

    <br><br>

    <input type="submit">

</form>

</body>

</html>
```

Let's understand it:

```html
<input
```

Creates an input element.

```html
type="text"
```

Creates a text input.

```html
id="username"
```

Gives the element its document identifier.

```html
name="username"
```

Gives the form control its submission name.

```html
placeholder="Enter your username"
```

Shows a temporary hint.

```html
pattern="[A-Za-z]+"
```

Defines the required input pattern.

```html
required
```

Makes the field mandatory.

---

# 22. Attributes We Have Already Used

You have already learned several of these attributes in previous topics.

### Image

```html
<img src="photo.jpg" width="400" height="300">
```

Attributes:

```text
src
width
height
```

---

### Link

```html
<a href="about.html" target="_blank">About</a>
```

Attribute:

```text
target
```

---

### Audio

```html
<audio controls>
    <source src="song.mp3" type="audio/mpeg">
</audio>
```

Attributes:

```text
src
type
```

---

### Video

```html
<video width="600" height="400" controls>
    <source src="movie.mp4" type="video/mp4">
</video>
```

Attributes:

```text
width
height
src
type
```

---

### Table

```html
<table border="1">
```

Attribute:

```text
border
```

---

### Form

```html
<input
    type="text"
    id="username"
    name="username"
    placeholder="Enter username"
    pattern="[A-Za-z]+"
    required>
```

Attributes:

```text
type
id
name
placeholder
pattern
required
```

---

# 23. Attribute vs Tag

This is one of the most important concepts.

Consider:

```html
<img src="photo.jpg" width="400">
```

### Tag

```html
<img>
```

tells us:

> **This is an image.**

### Attributes

```html
src="photo.jpg"
width="400"
```

give additional information:

> **Which image?**

> **How wide?**

So:

```text
              HTML
               │
        ┌──────┴──────┐
        ↓             ↓
       TAG        ATTRIBUTES
        ↓             ↓
    What is it?   Extra information
```

---

# 24. One Tag Can Have Multiple Attributes

Yes!

For example:

```html
<img
    src="photo.jpg"
    width="400"
    height="300"
    alt="Profile photo">
```

Here one `<img>` element has multiple attributes:

```text
src
width
height
alt
```

Similarly:

```html
<input
    type="text"
    id="username"
    name="username"
    placeholder="Enter username"
    required>
```

has several attributes.

---

# 25. Important Attribute Rules

### Rule 1: Attributes go inside the opening tag

✅

```html
<img src="photo.jpg">
```

---

### Rule 2: Attribute values are commonly written in quotes

✅

```html
<img src="photo.jpg">
```

---

### Rule 3: Multiple attributes are separated by spaces

✅

```html
<img src="photo.jpg" width="400" height="300">
```

---

### Rule 4: Attribute names are written before `=`

```text
attribute = value
```

Example:

```html
width="400"
```

---

### Rule 5: Not every attribute works with every tag

For example:

```html
<img src="photo.jpg">
```

makes sense.

But:

```html
<p src="photo.jpg">Hello</p>
```

does not make `src` meaningful for a paragraph.

Different HTML elements support different attributes.

---

# 26. Quick Revision Table

| Attribute     | Main purpose                                                |
| ------------- | ----------------------------------------------------------- |
| `src`         | Specifies source/location of a resource                     |
| `width`       | Specifies width where applicable                            |
| `height`      | Specifies height where applicable                           |
| `target`      | Specifies where a link opens                                |
| `type`        | Specifies a type/format depending on the element            |
| `border`      | Basic/legacy table border attribute                         |
| `required`    | Makes a form control mandatory                              |
| `placeholder` | Shows a temporary input hint                                |
| `id`          | Identifies an element                                       |
| `name`        | Names a form control, especially for submitted data         |
| `pattern`     | Specifies a validation pattern for applicable form controls |

---

# 27. Interview Questions

### Q1. What is an HTML attribute?

An HTML attribute provides additional information about an HTML element and is generally written in the opening tag.

### Q2. Where are attributes written?

Inside the opening tag.

```html
<img src="photo.jpg">
```

### Q3. Can an element have multiple attributes?

Yes.

```html
<img src="photo.jpg" width="400" height="300">
```

### Q4. What is `src`?

It specifies the source/location of a resource.

### Q5. What is `target="_blank"`?

It requests that a linked document open in a new browsing context, commonly a new tab.

### Q6. What is `required`?

It indicates that a form control must have a value before the form can be submitted.

### Q7. What is `placeholder`?

It provides a temporary hint inside a form control.

### Q8. Difference between `id` and `name`?

`id` identifies an element in the document, while `name` gives a form control a name used when form data is submitted.

### Q9. What is `pattern`?

It specifies a regular-expression pattern that applicable form input must match.

---

# 🧠 Final Revision

The easiest way to remember attributes is:

```text
TAG
 ↓
"What am I?"

ATTRIBUTE
 ↓
"Give me more information."
```

Example:

```html
<img src="photo.jpg" width="400" height="300">
```

```text
<img>          → I am an image
src            → Here is my image
width          → Make me this wide
height         → Make me this tall
```

And your complete list:

```text
src         → Source
width       → Width
height      → Height
target      → Link opening location
type        → Type/format
border      → Table border (legacy HTML attribute)
required    → Must be filled
placeholder → Temporary hint
id          → Element identifier
name        → Form control name
pattern     → Input format/validation rule
```

### The most important formula

```html
<tag attribute="value">
```

For example:

```html
<input type="text" id="username" name="username" placeholder="Enter name" required>
```

**Tag = what it is.**

**Attribute = extra information about it.**
