# 10. HTML Images

HTML provides the `<img>` tag to display an image on a webpage.

Think of an **image as a photograph placed inside a webpage**.

For example:

```html
<img src="photo.jpg">
```

The browser reads this and displays `photo.jpg`.

---

# 1. What is `<img>`?

`<img>` is the HTML tag used to **display an image on a webpage**.

### Syntax

```html
<img src="image.jpg">
```

Example:

```html
<!DOCTYPE html>
<html>
<body>

<h1>My Photo</h1>

<img src="photo.jpg">

</body>
</html>
```

### Important point

`<img>` is an **empty/void element**.

It does **not** have a separate closing tag.

❌ Wrong:

```html
<img src="photo.jpg"></img>
```

✅ Correct:

```html
<img src="photo.jpg">
```

---

# 2. `src` Attribute

`src` means **Source**.

It tells the browser:

> **"Where is the image located?"**

### Syntax

```html
<img src="image.jpg">
```

Here:

* `<img>` → display an image
* `src` → tells the location of the image
* `"image.jpg"` → image file

### Example

Suppose your HTML file and image are in the same folder:

```text
MyWebsite/
│
├── index.html
└── photo.jpg
```

Then:

```html
<img src="photo.jpg">
```

The browser searches for `photo.jpg` in the same folder.

---

# 3. Image Inside a Folder

Suppose your folder structure is:

```text
MyWebsite/
│
├── index.html
│
└── images/
    └── photo.jpg
```

Then:

```html
<img src="images/photo.jpg">
```

Here:

```text
images/photo.jpg
```

is the path to the image.

---

# 4. Image from Another Website

An image can also be loaded using a URL.

Example:

```html
<img src="https://example.com/photo.jpg">
```

The `src` contains the web address of the image.

So the browser understands:

> "Go to this location and get the image."

---

# 5. `width` Attribute

The `width` attribute specifies the **width of the image**.

Example:

```html
<img src="photo.jpg" width="300">
```

This displays the image with a width of approximately **300 pixels**.

You can also write:

```html
<img src="photo.jpg" width="500">
```

---

# 6. `height` Attribute

The `height` attribute specifies the **height of the image**.

Example:

```html
<img src="photo.jpg" height="300">
```

The image height is approximately **300 pixels**.

---

# 7. Using `width` and `height Together`

You can specify both.

```html
<img src="photo.jpg" width="400" height="300">
```

Conceptually:

```text
          400 px
    ┌──────────────────┐
    │                  │
    │      IMAGE       │ 300 px
    │                  │
    └──────────────────┘
```

So:

* `width="400"` → image width
* `height="300"` → image height

---

# 8. Image-Related Attributes

The commonly used attributes of `<img>` include:

| Attribute | Purpose                             |
| --------- | ----------------------------------- |
| `src`     | Specifies the image source/location |
| `width`   | Specifies image width               |
| `height`  | Specifies image height              |
| `alt`     | Alternative text for the image      |
| `title`   | Additional information/tooltip      |

Let's understand them.

---

# 9. `alt` Attribute

`alt` means **alternative text**.

Example:

```html
<img src="cat.jpg" alt="A white cat">
```

It describes what the image represents.

### Why is `alt` useful?

If the image cannot be displayed, the alternative text can be shown instead.

For example:

```html
<img src="wrong-image.jpg" alt="My profile photo">
```

If `wrong-image.jpg` doesn't exist, the browser cannot display the image, but the `alt` text provides a description.

### Another important use

`alt` text is also useful for **accessibility**, because screen readers can use it to describe images to users who cannot see them.

---

# 10. `title` Attribute

The `title` attribute provides additional information about an image.

Example:

```html
<img src="photo.jpg" title="My Profile Photo">
```

When the user moves the mouse over the image, browsers commonly display the title as a small tooltip.

---

# 11. Complete Example

```html
<!DOCTYPE html>
<html>
<head>
    <title>HTML Images</title>
</head>

<body>

<h1>My Image</h1>

<img 
    src="photo.jpg"
    width="400"
    height="300"
    alt="My profile photo"
    title="Profile Photo">

</body>
</html>
```

### What is happening?

```html
<img
```

We are telling HTML:

> "I want to display an image."

```html
src="photo.jpg"
```

> "Get the image from `photo.jpg`."

```html
width="400"
```

> "Display it with a width of 400."

```html
height="300"
```

> "Display it with a height of 300."

```html
alt="My profile photo"
```

> "This is the alternative description of the image."

```html
title="Profile Photo"
```

> "Show additional information when the user points at the image."

---

# 12. One-Line Example

You can put everything in one line:

```html
<img src="photo.jpg" width="400" height="300" alt="My profile photo" title="Profile Photo">
```

This is perfectly valid HTML.

---

# 13. Important: `<img>` vs `<a>`

Students commonly confuse these two.

| `<img>`                          | `<a>`                                   |
| -------------------------------- | --------------------------------------- |
| Displays an image                | Creates a hyperlink                     |
| Used for pictures                | Used for navigation                     |
| Uses `src`                       | Uses `href`                             |
| Example: `<img src="photo.jpg">` | Example: `<a href="home.html">Home</a>` |

### Easy memory trick

**`img` → `src`**

**`a` → `href`**

Think:

> **Image comes from a SOURCE → `src`**

> **Anchor goes somewhere through a HYPERLINK REFERENCE → `href`**

---

# 14. `<img>` Does Not Need `</img>`

This is very important.

`<img>` is a **void element**, so there is no closing tag.

✅ Correct:

```html
<img src="photo.jpg">
```

❌ Incorrect:

```html
<img src="photo.jpg"></img>
```

---

# 15. Common Image Mistakes

### Mistake 1: Wrong attribute

❌

```html
<img href="photo.jpg">
```

`href` is not the normal source attribute for an image.

✅

```html
<img src="photo.jpg">
```

---

### Mistake 2: Wrong file name

Suppose the actual file is:

```text
myphoto.jpg
```

But you write:

```html
<img src="photo.jpg">
```

The image may not appear because the browser cannot find the specified file.

---

### Mistake 3: Wrong folder path

Suppose:

```text
website/
   index.html
   images/
      photo.jpg
```

Then this is correct:

```html
<img src="images/photo.jpg">
```

Not:

```html
<img src="photo.jpg">
```

because `photo.jpg` is inside the `images` folder.

---

### Mistake 4: Forgetting quotes

Prefer:

```html
<img src="photo.jpg">
```

rather than:

```html
<img src=photo.jpg>
```

---

# 16. Image Formats

Common image file formats you may encounter are:

* `.jpg` / `.jpeg`
* `.png`
* `.gif`
* `.webp`
* `.svg`

Example:

```html
<img src="photo.jpg">
```

```html
<img src="logo.png">
```

```html
<img src="animation.gif">
```

The important thing for the HTML code is that the `src` points to the correct image resource.

---

# 17. Image Syntax to Remember

### Basic

```html
<img src="image.jpg">
```

### With dimensions

```html
<img src="image.jpg" width="300" height="200">
```

### With alternative text

```html
<img src="image.jpg" alt="Description of image">
```

### Complete

```html
<img src="image.jpg"
     width="300"
     height="200"
     alt="Description of image"
     title="Image title">
```

---

# 18. Quick Revision Table

| Term                | Meaning                          |
| ------------------- | -------------------------------- |
| `<img>`             | Displays an image                |
| `src`               | Image source/location            |
| `width`             | Image width                      |
| `height`            | Image height                     |
| `alt`               | Alternative description of image |
| `title`             | Additional information/tooltip   |
| `<img>` closing tag | Not required                     |
| Image path          | Location of image file           |

---

# 19. Interview Questions

### Q1. What is the use of `<img>`?

`<img>` is used to display an image on an HTML webpage.

### Q2. What is `src`?

`src` specifies the source or location of the image.

### Q3. Does `<img>` have a closing tag?

No. `<img>` is a void/empty element and does not require a closing tag.

### Q4. What is the use of `width`?

It specifies the width of the displayed image.

### Q5. What is the use of `height`?

It specifies the height of the displayed image.

### Q6. What is `alt`?

`alt` provides alternative text describing the image, especially useful when the image cannot be displayed and for accessibility.

### Q7. Difference between `src` and `href`?

* `src` → specifies the **source** of a resource, such as an image.
* `href` → specifies the **destination/reference** of a hyperlink.

Example:

```html
<img src="photo.jpg">
```

```html
<a href="about.html">About</a>
```

---

# 🧠 Final Memory Trick

Remember the basic image formula:

```text
<img
   src      → WHERE is the image?
   width    → HOW WIDE?
   height   → HOW TALL?
   alt      → WHAT is the image?
   title    → EXTRA INFORMATION?
>
```

### Most important code:

```html
<img src="photo.jpg" width="400" height="300" alt="My photo">
```

**`<img>` = show picture**

**`src` = find picture**

**`width` = width**

**`height` = height**

**`alt` = describe picture**

That covers **Topic 10: HTML Images**.
