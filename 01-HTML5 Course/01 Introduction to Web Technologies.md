# 1. Introduction to Web Technologies

Before learning HTML5, CSS3 and JavaScript separately, we first need to understand **what Web Technology is and how these three technologies work together**.

---

## 1.1 What is Web Technology?

Imagine you want to build a house.

You cannot build a complete house with just one thing. You need different things for different purposes:

* Bricks → structure
* Paint → appearance
* Electricity → functionality
* Doors and windows → interaction

A web application is similar.

Different technologies are used to create different parts of a website or web application.

These technologies are broadly called **Web Technologies**.

### Simple definition

> **Web Technology refers to the technologies used to create and develop websites and web applications that can be accessed through the web.**

Some important technologies we will learn in this course are:

```text
HTML5       → Structure
CSS3        → Appearance
JavaScript  → Behavior
```

---

# 1.2 What is a Web Application?

Let's first understand the word **application**.

An application is a program that allows us to perform some task.

For example:

* Calculator → performs calculations
* Word processor → allows us to write documents
* Music application → allows us to play music

A **web application** is an application that we access through a **web browser**.

For example, imagine an online shopping application.

You can:

1. Open the website.
2. Search for a product.
3. View the product.
4. Add it to a cart.
5. Enter your details.
6. Place an order.

You are interacting with an application through the browser.

### Simple definition

> **A web application is an application that is accessed and used through a web browser.**

### Simple example

```text
Online Shopping
       ↓
Open Browser
       ↓
Open Website
       ↓
Search Product
       ↓
Add to Cart
       ↓
Place Order
```

All of this happens through a web application.

---

# 1.3 Webpage vs Web Application

These two terms can be confusing.

### Webpage

A webpage can primarily provide information.

For example:

```text
Our College

About our college...

Courses offered:
Java
Python
Web Technologies
```

You mainly **read the information**.

### Web Application

A web application allows you to **perform operations**.

For example:

```text
Online Banking

Enter Account Number
Enter Password

[ Login ]

[ Transfer Money ]
[ Check Balance ]
```

Here you are interacting with the application.

### Easy way to remember

> **Webpage → mainly shows information**

> **Web application → allows users to interact and perform tasks**

---

# 1.4 What Happens When a Web Application Runs in a Browser?

This is one of the most important basic ideas.

Suppose you open a web application in Google Chrome.

What actually happens?

Let's understand it step by step.

---

## Step 1 — You open the browser

For example:

```text
Computer
   ↓
Google Chrome
```

The browser is the program through which you access the web application.

---

## Step 2 — You request a web application

You enter a website address or click a link.

For example:

```text
Browser
   ↓
Request
   ↓
Web Server
```

The browser sends a request for the required resource/application.

---

## Step 3 — The server receives the request

The server receives the request and processes it.

Depending on the application, the server may need to:

* Find information
* Process data
* Communicate with a database
* Generate a response

---

## Step 4 — The server sends a response

After processing the request, the server sends a response back.

```text
Browser
   ↓
Request
   ↓
Server
   ↓
Processing
   ↓
Response
   ↓
Browser
```

---

## Step 5 — Browser displays the result

The browser receives the response and displays the web application to the user.

The browser interprets technologies such as:

```text
HTML
CSS
JavaScript
```

and uses them to create the page that you see and interact with.

---

# 1.5 Front-End

Now imagine you are using an online shopping website.

You can see:

* Product names
* Product images
* Buttons
* Menus
* Search box
* Prices
* Forms

You can also interact with them.

This visible and interactive part is called the **Front-End**.

### Simple definition

> **Front-end is the part of a web application that the user sees and interacts with.**

### Example

```text
              Web Application
                    ↓
                 Front-End
                    ↓
       ┌────────────┼────────────┐
       ↓            ↓            ↓
     Text         Images       Buttons
       ↓            ↓            ↓
             User interacts
```

---

# 1.6 Client-Side

The user's browser is commonly referred to as the **client**.

For example:

```text
                 Internet
                    │
        ┌───────────┴───────────┐
        ↓                       ↓
     Client                  Server
        ↓                       ↓
     Browser              Web Application
```

The browser is on the user's side.

Therefore, the work performed in the browser is commonly referred to as **client-side processing**.

### Simple understanding

```text
Client
  ↓
User's browser
```

```text
Server
  ↓
System that provides/processes the application
```

So:

> **Front-end development is mainly concerned with what happens on the client side and what the user sees and interacts with.**

---

# 1.7 HTML

Now we come to the first major technology.

Suppose you want to create this webpage:

```text
Welcome to My Website

This is my first webpage.

[ Click Me ]
```

The browser needs to know:

* Where is the heading?
* Where is the paragraph?
* Where is the button?

**HTML provides the structure.**

HTML stands for:

> **HyperText Markup Language**

### Simple definition

> **HTML is a markup language used to structure the content of a webpage.**

HTML can define things such as:

* Headings
* Paragraphs
* Images
* Links
* Tables
* Forms
* Buttons

For example:

```html
<h1>Welcome to My Website</h1>

<p>This is my first webpage.</p>

<button>Click Me</button>
```

HTML tells the browser what these things are.

---

# 1.8 CSS

Now imagine the HTML page looks very plain.

You want:

* Heading in blue
* Bigger text
* Beautiful button
* Background color
* Proper spacing
* Better layout

HTML alone is not responsible for all of this styling.

This is where **CSS** comes in.

CSS stands for:

> **Cascading Style Sheets**

### Simple definition

> **CSS is used to style and control the appearance of HTML elements on a webpage.**

For example:

```css
h1 {
    color: blue;
}

button {
    font-size: 20px;
}
```

Now CSS tells the browser:

> "Make the heading blue."

> "Make the button text bigger."

---

# 1.9 JavaScript

Now imagine the user clicks the button.

You want the website to respond:

```text
User clicks button
        ↓
Something happens
        ↓
Message appears
```

This is where **JavaScript** comes in.

### Simple definition

> **JavaScript is a programming language used to add behavior and interactivity to web pages and web applications.**

For example:

```javascript
button.onclick = function() {
    alert("Hello!");
};
```

The idea is:

```text
User
 ↓
Clicks button
 ↓
JavaScript detects the action
 ↓
JavaScript performs an action
 ↓
Message appears
```

---

# 1.10 Relationship Between HTML, CSS and JavaScript

This is the most important concept in this introductory topic.

Imagine a **person**.

### HTML → Skeleton

The skeleton provides the basic structure.

Similarly, HTML provides the structure of the webpage.

```text
HTML
 ↓
Structure
```

---

### CSS → Clothes and Appearance

Clothes and appearance make the person look different.

Similarly, CSS controls the appearance of the webpage.

```text
CSS
 ↓
Appearance
```

---

### JavaScript → Actions and Behavior

A person can move, speak and perform actions.

Similarly, JavaScript gives the webpage behavior and interactivity.

```text
JavaScript
 ↓
Behavior / Actions
```

---

# 1.11 Complete Analogy

Think about building a house.

```text
                 HOUSE / WEBPAGE
                       │
          ┌────────────┼────────────┐
          ↓            ↓            ↓
        HTML          CSS       JavaScript
          ↓            ↓            ↓
     Structure      Design       Behavior
          ↓            ↓            ↓
      Walls etc.   Paint etc.   Actions
```

Or remember it as:

```text
HTML       → WHAT exists?
CSS        → HOW does it look?
JavaScript → WHAT does it do?
```

---

# 1.12 One Simple Example

Suppose we want a webpage containing a button.

### HTML — Creates the button

```html
<button id="myButton">Click Me</button>
```

HTML says:

> There is a button called "Click Me."

---

### CSS — Makes the button look better

```css
#myButton {
    font-size: 20px;
}
```

CSS says:

> Make the button's text bigger.

---

### JavaScript — Makes the button perform an action

```javascript
document.getElementById("myButton").onclick = function() {
    alert("Button clicked!");
};
```

JavaScript says:

> When the user clicks this button, show a message.

---

# 1.13 Putting Everything Together

```text
                    WEB APPLICATION
                           │
                           ↓
                       WEB BROWSER
                           │
             ┌─────────────┼─────────────┐
             ↓             ↓             ↓
           HTML           CSS       JavaScript
             ↓             ↓             ↓
        STRUCTURE      APPEARANCE      BEHAVIOR
             │             │             │
             └─────────────┼─────────────┘
                           ↓
                    COMPLETE WEBPAGE
                           ↓
                       USER SEES IT
                           ↓
                    USER INTERACTS
```

---

# 1.14 Very Important Difference

| Technology     | Main Job  | Simple Meaning          |
| -------------- | --------- | ----------------------- |
| **HTML**       | Structure | What exists on the page |
| **CSS**        | Styling   | How it looks            |
| **JavaScript** | Behavior  | What it does            |

### Remember:

> 🦴 **HTML = Structure**

> 🎨 **CSS = Appearance**

> ⚙️ **JavaScript = Behavior**

---

# 1.15 Complete Flow to Remember

When you think about Web Technologies, remember this flow:

```text
User
  ↓
Web Browser
  ↓
Web Application
  ↓
Front-End
  ↓
HTML + CSS + JavaScript
  ↓
HTML → Structure
CSS → Appearance
JavaScript → Behavior
  ↓
Interactive Webpage
```

---

# 1.16 Interview Questions

### 1. What is Web Technology?

Web Technology refers to the technologies used to create and develop websites and web applications.

### 2. What is a Web Application?

A web application is an application accessed and used through a web browser.

### 3. What is Front-End?

Front-end is the part of a web application that the user can see and interact with.

### 4. What is client-side?

Client-side refers to processing or functionality that occurs on the user's side, typically within the web browser.

### 5. What is HTML?

HTML is a markup language used to structure the content of web pages.

### 6. What is CSS?

CSS is used to style and control the appearance of HTML elements.

### 7. What is JavaScript?

JavaScript is a programming language used to add behavior and interactivity to web pages and applications.

### 8. How are HTML, CSS and JavaScript related?

> **HTML provides structure, CSS provides presentation, and JavaScript provides behavior and interactivity.**

---

# 🧠 Final Revision

If you remember only one thing from this topic, remember:

```text
                WEB TECHNOLOGIES
                       ↓
              WEB APPLICATION
                       ↓
                  WEB BROWSER
                       ↓
                FRONT-END
                       ↓
        ┌──────────────┼──────────────┐
        ↓              ↓              ↓
      HTML            CSS        JavaScript
        ↓              ↓              ↓
   Structure       Appearance      Behavior
        ↓              ↓              ↓
       WHAT?          HOW?          ACTION?
```

**HTML builds the structure.
CSS makes the structure look good.
JavaScript makes the webpage respond and perform actions.**
