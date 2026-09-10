# 13. HTML Tables

An **HTML table** is used to display information in the form of **rows and columns**.

A simple way to imagine it is:

```text
             Columns
        ↓       ↓       ↓
       Name    Age     City
       ───────────────────
       Ravi    25      Delhi
       John    28      Mumbai
       Ali     22      Hyderabad
        ↑
       Rows
```

A table is useful when information needs to be organized into a grid.

---

# 1. What is `<table>`?

`<table>` is the main HTML tag used to create a **table**.

Example:

```html
<table>
    ...
</table>
```

Think of `<table>` as the **container** that holds the entire table.

---

# 2. What is `<tr>`?

`<tr>` means **Table Row**.

It creates one horizontal row in a table.

Example:

```html
<tr>
    ...
</tr>
```

For example:

```text
<tr>  →  one complete row
```

A table can contain many `<tr>` elements.

---

# 3. What is `<th>`?

`<th>` means **Table Header** or **Table Heading**.

It is used for a heading of a column or row.

Example:

```html
<th>Name</th>
```

Browsers generally display table headings in **bold and centered** text by default.

For example:

```html
<table>
    <tr>
        <th>Name</th>
        <th>Age</th>
        <th>City</th>
    </tr>
</table>
```

Output conceptually:

```text
┌──────────┬──────┬──────────┐
│   Name   │ Age  │   City   │  ← headings
└──────────┴──────┴──────────┘
```

---

# 4. What is `<td>`?

`<td>` means **Table Data**.

It represents the actual data inside a table cell.

Example:

```html
<td>Ravi</td>
```

For example:

```html
<tr>
    <td>Ravi</td>
    <td>25</td>
    <td>Delhi</td>
</tr>
```

Conceptually:

```text
┌──────────┬──────┬──────────┐
│   Ravi   │  25  │  Delhi   │
└──────────┴──────┴──────────┘
```

---

# 5. Understanding `<table>`, `<tr>`, `<th>`, `<td>`

This is the most important part.

Think about building a table.

```text
<table>
    ↓
Entire table

<tr>
    ↓
One row

<th>
    ↓
Heading cell

<td>
    ↓
Data cell
```

So the structure is:

```html
<table>

    <tr>
        <th>Heading</th>
        <th>Heading</th>
    </tr>

    <tr>
        <td>Data</td>
        <td>Data</td>
    </tr>

</table>
```

---

# 6. First Complete Table

Let's create a student table.

```html
<table>

    <tr>
        <th>Name</th>
        <th>Age</th>
        <th>Course</th>
    </tr>

    <tr>
        <td>Ravi</td>
        <td>22</td>
        <td>Java</td>
    </tr>

    <tr>
        <td>John</td>
        <td>24</td>
        <td>Python</td>
    </tr>

</table>
```

Conceptually:

```text
Name       Age       Course
────────────────────────────
Ravi       22        Java
John       24        Python
```

---

# 7. How Does the Browser Understand It?

Look at this:

```html
<table>
```

The browser understands:

> "Start a table."

Then:

```html
<tr>
```

means:

> "Start a row."

Then:

```html
<th>Name</th>
<th>Age</th>
<th>Course</th>
```

means:

> "Put three heading cells in this row."

Then:

```html
</tr>
```

means:

> "The row is finished."

Next:

```html
<tr>
    <td>Ravi</td>
    <td>22</td>
    <td>Java</td>
</tr>
```

means:

> "Create another row containing three data cells."

---

# 8. Rows

A **row** goes horizontally.

Example:

```text
Name       Age       Course
────────────────────────────  ← Row 1
Ravi       22        Java
────────────────────────────  ← Row 2
John       24        Python
────────────────────────────  ← Row 3
```

In HTML, each row is represented using:

```html
<tr>
```

### Example

```html
<tr>
    <td>Ravi</td>
    <td>22</td>
    <td>Java</td>
</tr>
```

That represents **one row**.

---

# 9. Columns

A **column** goes vertically.

Example:

```text
Name       Age       Course
 ↓          ↓          ↓
Ravi       22        Java
John       24        Python
Ali        23        HTML
```

Here there are **3 columns**:

1. Name
2. Age
3. Course

The number of columns is determined by the cells placed in each row.

For example:

```html
<tr>
    <th>Name</th>
    <th>Age</th>
    <th>Course</th>
</tr>
```

creates three heading cells, forming three columns.

---

# 10. Table Heading

Table headings are created using `<th>`.

Example:

```html
<tr>
    <th>Name</th>
    <th>Age</th>
    <th>City</th>
</tr>
```

Output conceptually:

```text
Name        Age        City
```

These tell the user what the columns represent.

---

# 11. Table Data

Actual information is placed using `<td>`.

Example:

```html
<tr>
    <td>Ravi</td>
    <td>25</td>
    <td>Delhi</td>
</tr>
```

Here:

```text
Ravi  → data
25    → data
Delhi → data
```

---

# 12. `<th>` vs `<td>`

This is an important interview question.

| `<th>`                                                   | `<td>`                                         |
| -------------------------------------------------------- | ---------------------------------------------- |
| Table Header                                             | Table Data                                     |
| Represents heading                                       | Represents actual data                         |
| Used for column/row headings                             | Used for normal cells                          |
| Browser usually displays it bold and centered by default | Browser normally displays regular cell content |

Example:

```html
<th>Name</th>
```

means:

> "Name is a heading."

Whereas:

```html
<td>Ravi</td>
```

means:

> "Ravi is data."

---

# 13. Table Border

A table without borders can be difficult to understand visually.

A border can be added using the `border` attribute in basic HTML examples:

```html
<table border="1">
```

Example:

```html
<table border="1">

    <tr>
        <th>Name</th>
        <th>Age</th>
    </tr>

    <tr>
        <td>Ravi</td>
        <td>22</td>
    </tr>

</table>
```

Conceptually:

```text
┌──────────┬──────┐
│   Name   │ Age  │
├──────────┼──────┤
│   Ravi   │  22  │
└──────────┴──────┘
```

The `border="1"` makes the table boundaries visible.

### Important modern practice

For modern HTML development, table appearance/borders are normally controlled using **CSS**, rather than relying on the old HTML `border` attribute.

For example:

```html
<table class="student-table">
```

and CSS:

```css
.student-table {
    border: 1px solid black;
}
```

For your basic HTML understanding, remember that you may see:

```html
<table border="1">
```

in introductory examples.

---

# 14. Complete Table Program

```html
<!DOCTYPE html>
<html>

<head>
    <title>Student Table</title>
</head>

<body>

<h1>Student Details</h1>

<table border="1">

    <tr>
        <th>Name</th>
        <th>Age</th>
        <th>Course</th>
    </tr>

    <tr>
        <td>Ravi</td>
        <td>22</td>
        <td>Java</td>
    </tr>

    <tr>
        <td>John</td>
        <td>24</td>
        <td>Python</td>
    </tr>

    <tr>
        <td>Ali</td>
        <td>23</td>
        <td>HTML</td>
    </tr>

</table>

</body>

</html>
```

### Output

```text
Student Details

┌──────────┬─────┬────────┐
│   Name   │ Age │ Course │
├──────────┼─────┼────────┤
│   Ravi   │ 22  │ Java   │
├──────────┼─────┼────────┤
│   John   │ 24  │ Python │
├──────────┼─────┼────────┤
│   Ali    │ 23  │ HTML   │
└──────────┴─────┴────────┘
```

---

# 15. Understanding the Program Step-by-Step

### Step 1

```html
<table border="1">
```

Create the table and give it a visible border.

### Step 2

```html
<tr>
```

Create the first row.

### Step 3

```html
<th>Name</th>
<th>Age</th>
<th>Course</th>
```

Create three heading cells.

### Step 4

```html
</tr>
```

Finish the first row.

### Step 5

```html
<tr>
    <td>Ravi</td>
    <td>22</td>
    <td>Java</td>
</tr>
```

Create a second row containing Ravi's data.

### Step 6

Repeat the same structure for the other students.

---

# 16. Table Structure

Consider:

```html
<table border="1">

    <tr>
        <th>Name</th>
        <th>Age</th>
    </tr>

    <tr>
        <td>Ravi</td>
        <td>22</td>
    </tr>

</table>
```

Its structure is:

```text
                    TABLE
                      │
             ┌────────┴────────┐
             ↓                 ↓
           ROW 1             ROW 2
             │                 │
        ┌────┴────┐       ┌────┴────┐
        ↓         ↓       ↓         ↓
       <th>      <th>    <td>      <td>
       Name      Age     Ravi       22
```

---

# 17. How to Count Rows and Columns

Consider:

```html
<table border="1">

    <tr>
        <th>Name</th>
        <th>Age</th>
        <th>City</th>
    </tr>

    <tr>
        <td>Ravi</td>
        <td>22</td>
        <td>Delhi</td>
    </tr>

    <tr>
        <td>John</td>
        <td>24</td>
        <td>Mumbai</td>
    </tr>

</table>
```

There are:

**3 rows**

```text
Row 1 → Name | Age | City
Row 2 → Ravi | 22  | Delhi
Row 3 → John | 24  | Mumbai
```

And **3 columns**:

```text
Column 1 → Name/Ravi/John
Column 2 → Age/22/24
Column 3 → City/Delhi/Mumbai
```

---

# 18. Common Confusion: `<tr>` vs `<td>`

### `<tr>`

Means:

> **Table Row**

```html
<tr>
    ...
</tr>
```

### `<td>`

Means:

> **Table Data**

```html
<td>Ravi</td>
```

Think:

```text
<tr> = whole horizontal row

<td> = one cell inside that row
```

---

# 19. Common Confusion: `<th>` vs `<td>`

Suppose we have:

```text
Name     Age
Ravi     22
```

Then:

```html
<th>Name</th>
<th>Age</th>
```

are headings.

And:

```html
<td>Ravi</td>
<td>22</td>
```

are data.

So:

```text
<th> → What does this column mean?

<td> → What is the actual value?
```

---

# 20. Common Mistakes

### Mistake 1: Putting `<td>` directly inside `<table>`

❌

```html
<table>
    <td>Ravi</td>
</table>
```

Normally, table cells should be placed inside a row.

✅

```html
<table>
    <tr>
        <td>Ravi</td>
    </tr>
</table>
```

---

### Mistake 2: Forgetting `<tr>`

❌

```html
<table>
    <th>Name</th>
    <th>Age</th>
</table>
```

Use rows:

✅

```html
<table>
    <tr>
        <th>Name</th>
        <th>Age</th>
    </tr>
</table>
```

---

### Mistake 3: Using `<td>` for headings

You can technically create a cell with `<td>`, but semantically a heading should use `<th>`.

Prefer:

```html
<th>Name</th>
```

instead of:

```html
<td>Name</td>
```

when "Name" is the column heading.

---

# 21. Real-World Uses of HTML Tables

Tables are useful for structured data such as:

### Student details

```text
Name | Age | Course
```

### Employee details

```text
ID | Name | Salary
```

### Product information

```text
Product | Price | Quantity
```

### Exam results

```text
Student | Subject | Marks
```

### Timetables

```text
Day | Subject | Time
```

---

# 22. Important Tags to Remember

| Tag       | Full Meaning | Purpose                |
| --------- | ------------ | ---------------------- |
| `<table>` | Table        | Creates the table      |
| `<tr>`    | Table Row    | Creates a row          |
| `<th>`    | Table Header | Creates a heading cell |
| `<td>`    | Table Data   | Creates a data cell    |

---

# 🧠 Final Memory Trick

Imagine an Excel sheet:

```text
                 TABLE
                   ↓
       ┌───────────┴───────────┐
       ↓                       ↓
     ROW                     ROW
       ↓                       ↓
   ┌───┼───┬───┐           ┌───┼───┬───┐
   │   │   │   │           │   │   │   │
  TH  TH  TH  TH          TD  TD  TD  TD
```

Remember:

> **`<table>` = entire table**

> **`<tr>` = one row**

> **`<th>` = heading**

> **`<td>` = data**

And:

```text
Rows    → Horizontal →
Columns → Vertical   ↓
```

### Most important syntax

```html
<table border="1">

    <tr>
        <th>Name</th>
        <th>Age</th>
        <th>Course</th>
    </tr>

    <tr>
        <td>Ravi</td>
        <td>22</td>
        <td>Java</td>
    </tr>

</table>
```

**The key pattern is:**

```text
<table>
   ↓
<tr>  → row
   ↓
<th>/<td> → cells
```

Once you understand that structure, HTML tables become very straightforward.
