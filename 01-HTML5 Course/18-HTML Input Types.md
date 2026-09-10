# 18. HTML Input Types

The `<input>` element is one of the most important elements used inside an HTML form.

The **`type` attribute** tells the browser **what kind of input control we want**.

For example:

```html
<input type="text">
```

means:

> "Create a text input."

While:

```html
<input type="email">
```

means:

> "Create an email input."

Your notes demonstrate these input types:

1. `text`
2. `email`
3. `number`
4. `date`
5. `radio`
6. `checkbox`
7. `submit`

---

# 1. Basic Syntax

The basic structure is:

```html
<input type="TYPE">
```

For example:

```html
<input type="text">
```

Here:

```text
<input>       → Input element
type          → Attribute
"text"        → Attribute value
```

So:

```text
<input type="text">
       ↑
    type tells
    what kind of input
```

---

# 2. `text`

## What is `type="text"`?

It creates a **single-line text input field**.

```html
<input type="text">
```

The user can enter ordinary text.

Example:

```html
<label>Name:</label>
<input type="text">
```

Conceptually:

```text
Name: [________________________]
```

### Used for:

* Name
* Username
* City
* Address
* Any ordinary short text

### Example

```html
<form>

    <label for="name">Name:</label>
    <input type="text" id="name" name="name">

</form>
```

If the user enters:

```text
Ravi
```

that value becomes the input's current value.

---

# 3. `email`

## What is `type="email"`?

It creates an input intended for an **email address**.

```html
<input type="email">
```

Example:

```html
<label>Email:</label>
<input type="email">
```

Conceptually:

```text
Email: [________________________]
```

The browser can perform built-in validation appropriate to an email input when the form is submitted.

For example:

```html
<input type="email" required>
```

Now the field must be filled, and the entered value is expected to be in an email-like format.

### Example

```html
<form>

    <label for="email">Email:</label>
    <input
        type="email"
        id="email"
        name="email"
        placeholder="Enter your email"
        required>

</form>
```

---

# 4. `number`

## What is `type="number"`?

It creates an input intended for **numeric values**.

```html
<input type="number">
```

Example:

```html
<label>Age:</label>
<input type="number">
```

Conceptually:

```text
Age: [ 22 ]
```

Browsers may provide controls for increasing or decreasing the value.

### Example

```html
<label for="age">Age:</label>
<input type="number" id="age" name="age">
```

---

## `number` with `min` and `max`

You can restrict the acceptable range.

```html
<input
    type="number"
    min="18"
    max="60">
```

This indicates that the acceptable number should be between 18 and 60.

---

# 5. `date`

## What is `type="date"`?

It creates an input for selecting/entering a **date**.

```html
<input type="date">
```

Example:

```html
<label>Date of Birth:</label>
<input type="date">
```

Depending on the browser, the user may get a date picker.

Conceptually:

```text
Date of Birth: [  DD/MM/YYYY  📅 ]
```

### Example

```html
<label for="dob">Date of Birth:</label>
<input type="date" id="dob" name="dob">
```

---

# 6. `radio`

## What is `type="radio"`?

Radio buttons are used when the user should generally select **one option from a group**.

Example:

```html
<input type="radio" name="gender" value="male">
Male

<input type="radio" name="gender" value="female">
Female
```

Conceptually:

```text
○ Male
○ Female
```

The important part is the **same `name`**.

```html
name="gender"
```

Both radio buttons belong to the same group.

---

# 7. Why Is `name` Important for Radio Buttons?

Consider:

```html
<input type="radio" name="gender" value="male">
Male

<input type="radio" name="gender" value="female">
Female
```

Both have:

```text
name="gender"
```

Therefore, they form one group.

The user generally chooses one:

```text
● Male
○ Female
```

or:

```text
○ Male
● Female
```

---

## Example With Three Options

```html
<label>Gender:</label>

<input type="radio" name="gender" value="male">
Male

<input type="radio" name="gender" value="female">
Female

<input type="radio" name="gender" value="other">
Other
```

Conceptually:

```text
Gender:

○ Male
○ Female
○ Other
```

---

# 8. `checkbox`

## What is `type="checkbox"`?

A checkbox allows the user to **select or deselect an option**.

```html
<input type="checkbox">
```

Example:

```html
<label>Skills:</label>

<input type="checkbox" name="skill" value="java">
Java

<input type="checkbox" name="skill" value="html">
HTML

<input type="checkbox" name="skill" value="css">
CSS
```

Conceptually:

```text
Skills:

☐ Java
☐ HTML
☐ CSS
```

The user can select multiple options:

```text
☑ Java
☑ HTML
☐ CSS
```

---

# 9. Radio vs Checkbox

This is **very important**.

### Radio

Generally:

> **Choose one from a group.**

```text
○ Male
○ Female
○ Other
```

### Checkbox

Generally:

> **Choose multiple options if needed.**

```text
☑ Java
☑ HTML
☐ CSS
```

### Comparison

| Radio                            | Checkbox                                    |
| -------------------------------- | ------------------------------------------- |
| `type="radio"`                   | `type="checkbox"`                           |
| Used for one choice from a group | Used for multiple/independent choices       |
| Same `name` groups the choices   | Each checkbox can be independently selected |
| Example: Gender                  | Example: Skills                             |

### Memory trick

```text
RADIO     → One choice from a group

CHECKBOX  → Tick whatever applies
```

---

# 10. `submit`

## What is `type="submit"`?

It creates a **submit button** for the form.

```html
<input type="submit">
```

Conceptually:

```text
┌──────────┐
│  Submit  │
└──────────┘
```

When the user clicks it, the form submission process is triggered.

---

# 11. Changing the Submit Button Text

You can use the `value` attribute.

```html
<input type="submit" value="Register">
```

Output:

```text
┌───────────┐
│  Register │
└───────────┘
```

Another example:

```html
<input type="submit" value="Login">
```

Output:

```text
┌─────────┐
│  Login  │
└─────────┘
```

---

# 12. Complete Example Using All Seven Input Types

Let's create one form containing all the input types from your notes.

```html
<!DOCTYPE html>
<html>

<head>
    <title>Input Types</title>
</head>

<body>

<h1>Student Form</h1>

<form>

    <label for="name">Name:</label>
    <input type="text" id="name" name="name">

    <br><br>

    <label for="email">Email:</label>
    <input type="email" id="email" name="email">

    <br><br>

    <label for="age">Age:</label>
    <input type="number" id="age" name="age">

    <br><br>

    <label for="dob">Date of Birth:</label>
    <input type="date" id="dob" name="dob">

    <br><br>

    <label>Gender:</label>

    <input type="radio" name="gender" value="male">
    Male

    <input type="radio" name="gender" value="female">
    Female

    <br><br>

    <label>Skills:</label>

    <input type="checkbox" name="skill" value="java">
    Java

    <input type="checkbox" name="skill" value="html">
    HTML

    <input type="checkbox" name="skill" value="css">
    CSS

    <br><br>

    <input type="submit" value="Register">

</form>

</body>

</html>
```

---

# 13. Understanding the Complete Program

### Name

```html
<input type="text" id="name" name="name">
```

Creates a normal text field.

```text
Name: [________________]
```

---

### Email

```html
<input type="email" id="email" name="email">
```

Creates an email input.

```text
Email: [________________]
```

---

### Age

```html
<input type="number" id="age" name="age">
```

Creates a numeric input.

```text
Age: [____]
```

---

### Date

```html
<input type="date" id="dob" name="dob">
```

Creates a date input.

```text
Date of Birth: [________]
```

---

### Gender

```html
<input type="radio" name="gender" value="male">
Male

<input type="radio" name="gender" value="female">
Female
```

Creates radio buttons.

```text
○ Male
○ Female
```

---

### Skills

```html
<input type="checkbox" name="skill" value="java">
Java
```

Creates a checkbox.

```text
☐ Java
```

Multiple checkboxes can be selected.

---

### Submit

```html
<input type="submit" value="Register">
```

Creates the Register button.

---

# 14. Visualizing the Whole Form

```text
┌────────────── Student Form ───────────────┐
│                                           │
│ Name:          [________________]         │
│                                           │
│ Email:         [________________]         │
│                                           │
│ Age:           [____]                     │
│                                           │
│ Date of Birth: [__________]               │
│                                           │
│ Gender:        ○ Male  ○ Female           │
│                                           │
│ Skills:        ☑ Java  ☐ HTML  ☑ CSS      │
│                                           │
│                  [ Register ]             │
│                                           │
└───────────────────────────────────────────┘
```

Each control is created by a different `type`.

---

# 15. One `<input>` Element, Many Behaviors

This is a very important concept.

All of these use the same element:

```html
<input>
```

But the `type` changes its behavior.

```html
<input type="text">
```

↓

**Text box**

```html
<input type="email">
```

↓

**Email input**

```html
<input type="number">
```

↓

**Number input**

```html
<input type="date">
```

↓

**Date input**

```html
<input type="radio">
```

↓

**Radio button**

```html
<input type="checkbox">
```

↓

**Checkbox**

```html
<input type="submit">
```

↓

**Submit button**

So remember:

> **`<input>` is the element; `type` tells it what kind of control to behave as.**

---

# 16. Input Type Comparison

| Type       | What it creates | Typical use                  |
| ---------- | --------------- | ---------------------------- |
| `text`     | Text field      | Name, username               |
| `email`    | Email field     | Email address                |
| `number`   | Numeric input   | Age, quantity                |
| `date`     | Date input      | Date of birth                |
| `radio`    | Radio button    | One choice from a group      |
| `checkbox` | Checkbox        | Multiple/independent choices |
| `submit`   | Submit button   | Submit the form              |

---

# 17. Important Attributes Often Used With Input Types

You already learned these attributes, and they frequently appear with input types.

### `id`

```html
<input type="text" id="username">
```

Identifies the element.

### `name`

```html
<input type="text" name="username">
```

Provides the form field's name for submitted data.

### `placeholder`

```html
<input type="text" placeholder="Enter username">
```

Provides a temporary hint.

### `required`

```html
<input type="email" required>
```

Makes the field required.

### `value`

```html
<input type="submit" value="Register">
```

Sets the button's displayed value/text for an input submit control.

---

# 18. Common Confusion: `text` vs `number`

### Text

```html
<input type="text">
```

For general text.

### Number

```html
<input type="number">
```

For numeric input.

Think:

```text
Name → text

Age → number
```

---

# 19. Common Confusion: Radio vs Checkbox

Suppose a form asks:

### Gender

```text
○ Male
○ Female
○ Other
```

Usually use:

```html
<input type="radio">
```

Because the user generally selects one.

But for:

### Skills

```text
☑ Java
☑ HTML
☑ CSS
```

use:

```html
<input type="checkbox">
```

because multiple skills can be selected.

---

# 20. Common Confusion: `submit` Is Not Just Normal Text

Compare:

```html
<input type="text">
```

with:

```html
<input type="submit">
```

The first creates an input field.

The second creates a submit control.

The difference comes from:

```text
type="text"
```

versus:

```text
type="submit"
```

---

# 21. Interview Questions

### Q1. What is an input type?

The `type` attribute of `<input>` specifies the kind of input control the browser should create.

### Q2. What is `type="text"`?

It creates a single-line text input.

### Q3. What is `type="email"`?

It creates an input intended for email addresses and enables appropriate built-in browser validation.

### Q4. What is `type="number"`?

It creates an input intended for numeric values.

### Q5. What is `type="date"`?

It creates a control for entering/selecting a date.

### Q6. What is the difference between radio and checkbox?

Radio buttons are generally used to select one option from a group, while checkboxes allow multiple or independent selections.

### Q7. What is `type="submit"`?

It creates a submit control that can trigger form submission.

### Q8. Why is the `name` attribute important for radio buttons?

Radio buttons with the same `name` belong to the same group, allowing the user to select one option from that group.

---

# 🧠 Final Revision

Remember the seven types from your notes:

```text
<input type="text">
        ↓
     Text

<input type="email">
        ↓
     Email

<input type="number">
        ↓
     Number

<input type="date">
        ↓
     Date

<input type="radio">
        ↓
     One choice from group

<input type="checkbox">
        ↓
     Multiple/independent choices

<input type="submit">
        ↓
     Submit form
```

### Super-easy memory pattern

```text
TEXT      → Write text
EMAIL     → Enter email
NUMBER    → Enter number
DATE      → Select date
RADIO     → Pick one
CHECKBOX  → Tick multiple
SUBMIT    → Send form
```

And the most important concept:

> **`<input>` is the form element, and the `type` attribute decides what kind of input control the browser provides.**
