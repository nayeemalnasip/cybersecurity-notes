# How Websites Work

## Website Fundamentals

### Overview

When a user visits a website, the browser sends a request to a web server. The server processes that request and returns data that the browser uses to display the webpage.

A web server is simply a dedicated computer that stores website files and responds to user requests.

---

## Website Architecture

Every website is generally divided into two major components:

### Front-End (Client-Side)

The front-end is everything users can see and interact with directly in their browser.

Examples:

* Text
* Images
* Buttons
* Forms
* Menus
* Animations

---

### Back-End (Server-Side)

The back-end processes requests from users and sends responses back to the browser.

Responsibilities include:

* Authentication
* Database operations
* Business logic
* Data processing
* API communication

---

## Website Communication Process

```text
User → Browser → Web Server → Response → Browser → Webpage Display
```

### Step-by-Step Flow

1. User enters a website URL.
2. Browser sends a request to the server.
3. Server processes the request.
4. Server returns data.
5. Browser renders the webpage.

---

## Key Notes

* Websites work through requests and responses.
* Browsers communicate with web servers.
* Front-end handles user interaction.
* Back-end handles processing and data management.

---

# HTML (HyperText Markup Language)

## What is HTML?

HTML is the standard language used to create web pages.

It defines:

* Structure
* Content
* Layout of a webpage

HTML uses **Elements (Tags)** to tell browsers how content should appear.

---

## Core Technologies of Websites

### HTML

Responsible for:

```text
Website Structure
```

---

### CSS

Responsible for:

```text
Website Styling
```

Examples:

* Colors
* Fonts
* Layouts
* Animations

---

### JavaScript

Responsible for:

```text
Website Functionality
```

Examples:

* Interactive buttons
* Dynamic content
* Form validation

---

## Basic HTML Structure

```html
<!DOCTYPE html>
<html>
<head>
<title>My Website</title>
</head>

<body>
<h1>Welcome</h1>
<p>Hello World</p>
</body>
</html>
```

---

## HTML Structure Breakdown

### <!DOCTYPE html>

Defines the document as:

```text
HTML5
```

Purpose:

* Browser compatibility
* Standardization

---

### <html>

Root element of every webpage.

All HTML content is placed inside this tag.

---

### <head>

Contains page information.

Examples:

* Title
* Metadata
* CSS links
* JavaScript links

---

### <body>

Contains visible webpage content.

Examples:

* Headings
* Paragraphs
* Images
* Buttons

---

### <h1>

Creates a large heading.

Example:

```html
<h1>Cyber Security Notes</h1>
```

---

### <p>

Creates a paragraph.

Example:

```html
<p>This is a paragraph.</p>
```

---

## Common HTML Elements

### Button

```html
<button>Click Me</button>
```

---

### Image

```html
<img src="image.jpg">
```

---

### List

```html
<ul>
<li>Item 1</li>
<li>Item 2</li>
</ul>
```

---

## HTML Attributes

Attributes provide additional information about elements.

### Class Attribute

Used for styling multiple elements.

Example:

```html
<p class="important">
Important Text
</p>
```

---

### ID Attribute

Used to uniquely identify an element.

Example:

```html
<p id="example">
Unique Element
</p>
```

### Important Difference

```text
Class = Can be reused
ID = Must be unique
```

---

### SRC Attribute

Used to specify image locations.

Example:

```html
<img src="img/cat.jpg">
```

---

## Why IDs Matter

JavaScript frequently uses IDs to locate elements.

Example:

```html
<p id="demo">Hello</p>
```

JavaScript can then modify this specific element.

---

## Viewing HTML Source Code

Most browsers allow viewing webpage source code.

### Chrome

```text
Right Click → View Page Source
```

### Safari

```text
Right Click → Show Page Source
```

---

## Key Notes

* HTML builds webpage structure.
* Elements are created using tags.
* Attributes provide extra information.
* Classes can be reused.
* IDs must be unique.
* HTML works together with CSS and JavaScript.

---

# JavaScript (JS)

## What is JavaScript?

JavaScript is a programming language used to make websites interactive and dynamic.

Without JavaScript, websites would mostly be static pages.

---

## Role of JavaScript

| Technology | Purpose       |
| ---------- | ------------- |
| HTML       | Structure     |
| CSS        | Design        |
| JavaScript | Functionality |

---

## What Can JavaScript Do?

JavaScript can:

* Update content dynamically
* Handle user actions
* Create animations
* Validate forms
* Load content without refreshing pages
* Modify webpage appearance

---

## Adding JavaScript to a Website

### Method 1: Inside Script Tags

```html
<script>
alert("Hello");
</script>
```

---

### Method 2: External JavaScript File

```html
<script src="script.js"></script>
```

Benefits:

* Cleaner code
* Easier maintenance
* Reusable scripts

---

## JavaScript Example

### Changing HTML Content

HTML:

```html
<p id="demo">Hello</p>
```

JavaScript:

```javascript
document.getElementById("demo").innerHTML =
"Hack the Planet";
```

Result:

```text
Hello
↓
Hack the Planet
```

---

## Understanding the Code

### document

Represents the webpage.

---

### getElementById()

Finds an element using its ID.

Example:

```javascript
document.getElementById("demo")
```

---

### innerHTML

Changes the content inside an element.

Example:

```javascript
.innerHTML = "New Text"
```

---

## JavaScript Events

Events allow JavaScript to respond to user actions.

Common events:

| Event    | Trigger         |
| -------- | --------------- |
| onclick  | Mouse click     |
| onhover  | Mouse hover     |
| onkeyup  | Keyboard input  |
| onsubmit | Form submission |

---

## Button Click Example

```html
<button onclick='document.getElementById("demo").innerHTML="Button Clicked";'>
Click Me
</button>
```

### Result

Before Click:

```text
Hello
```

After Click:

```text
Button Clicked
```

---

## Why JavaScript is Important

Without JavaScript:

```text
Static Website
```

With JavaScript:

```text
Interactive Website
```

Examples:

* Login systems
* Live chat
* Notifications
* Online games
* Dynamic dashboards
* Real-time updates

---

## Key Notes

* JavaScript makes websites interactive.
* HTML provides structure.
* CSS provides styling.
* JS can modify HTML dynamically.
* Events trigger JavaScript actions.
* JavaScript can be embedded or loaded from external files.

---

## Learning Outcome

After completing this section, I understood how websites function through client-server communication, how HTML creates webpage structure, and how JavaScript adds interactivity and dynamic behavior. I also learned the purpose of common HTML elements, attributes, JavaScript events, and how modern websites combine HTML, CSS, and JavaScript to deliver rich user experiences.
