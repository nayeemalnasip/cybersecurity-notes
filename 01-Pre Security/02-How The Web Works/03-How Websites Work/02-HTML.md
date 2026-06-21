# HTML Fundamentals

## Overview

HTML (**HyperText Markup Language**) is the standard language used to create web pages. It provides the structure of a website and tells the browser how content should be displayed.

Websites are primarily built using three technologies:

```text
HTML       → Structure
CSS        → Styling & Design
JavaScript → Interactivity & Functionality
```

HTML acts as the foundation of every webpage.

---

## What is HTML?

HTML consists of **elements (tags)** that define different parts of a webpage.

These tags instruct the browser how content should appear to users.

### Examples of HTML Elements

```html
<h1>Heading</h1>

<p>This is a paragraph.</p>

<button>Click Me</button>

<img src="image.jpg">
```

Each tag serves a specific purpose in building webpage content.

---

## Basic HTML Structure

Every HTML page follows a standard structure:

```html
<!DOCTYPE html>
<html>
<head>
    <title>My Website</title>
</head>

<body>

    <h1>Welcome to My Website</h1>

    <p>This is my first webpage.</p>

</body>
</html>
```

---

## HTML Structure Breakdown

### 1. DOCTYPE Declaration

```html
<!DOCTYPE html>
```

Purpose:

* Declares the document as an HTML5 document.
* Helps browsers render pages consistently.

---

### 2. HTML Element

```html
<html>
```

Purpose:

* Root element of the webpage.
* All other HTML elements are placed inside it.

---

### 3. Head Element

```html
<head>
```

Purpose:

* Stores page information.
* Not directly visible to users.

Common contents:

* Page Title
* Meta Tags
* CSS Links
* Scripts

Example:

```html
<head>
    <title>My Website</title>
</head>
```

---

### 4. Body Element

```html
<body>
```

Purpose:

* Contains all visible content displayed in the browser.

Examples:

* Text
* Images
* Buttons
* Forms
* Videos

Example:

```html
<body>
    <h1>Hello World</h1>
</body>
```

---

## Common HTML Tags

### Heading Tag

```html
<h1>Cyber Security Notes</h1>
```

Purpose:

* Creates large headings.

---

### Paragraph Tag

```html
<p>This is a paragraph.</p>
```

Purpose:

* Displays normal text content.

---

### Button Tag

```html
<button>Submit</button>
```

Purpose:

* Creates clickable buttons.

---

### Image Tag

```html
<img src="img/cat.jpg">
```

Purpose:

* Displays images.

---

## HTML Attributes

Attributes provide additional information about elements.

### Example

```html
<p class="bold-text">
    Welcome
</p>
```

Here:

```text
class = Attribute
bold-text = Value
```

---

## Class Attribute

### Example

```html
<p class="red-text">
    Hello
</p>
```

Purpose:

* Used for styling elements with CSS.
* Multiple elements can share the same class.

Example:

```html
<p class="red-text">Text 1</p>
<p class="red-text">Text 2</p>
```

Both elements use the same class.

---

## ID Attribute

### Example

```html
<p id="example">
    Hello
</p>
```

Purpose:

* Uniquely identifies an element.
* Used by CSS and JavaScript.

### Important Rule

Unlike classes:

```text
Class → Can be reused
ID    → Must be unique
```

Correct Example:

```html
<p id="header"></p>
<p id="footer"></p>
```

Incorrect Example:

```html
<p id="header"></p>
<p id="header"></p>
```

---

## Multiple Attributes

An element can contain multiple attributes.

Example:

```html
<p class="red-text" id="intro">
    Welcome
</p>
```

Here the element contains:

```text
Class Attribute
ID Attribute
```

---

## Viewing Website HTML

You can inspect the HTML source code of any website.

### Google Chrome

```text
Right Click
   ↓
View Page Source
```

### Safari

```text
Right Click
   ↓
Show Page Source
```

This allows developers and security professionals to analyze webpage structure.

---

## HTML in Cyber Security

Understanding HTML is important because web application security testing often involves examining webpage source code.

Common activities include:

* Source Code Review
* Web Enumeration
* Identifying Hidden Inputs
* Discovering Sensitive Information
* Understanding Application Structure

HTML is often the first layer analyzed during web application penetration testing.

---

## Key Notes

* HTML stands for HyperText Markup Language.
* HTML provides the structure of a webpage.
* CSS provides styling.
* JavaScript provides interactivity.
* `<html>` is the root element.
* `<head>` contains page information.
* `<body>` contains visible content.
* Tags are the building blocks of HTML.
* Attributes provide additional information.
* Class attributes can be reused.
* ID attributes must be unique.

---

## Learning Outcome

After completing this section, I understood how HTML forms the foundation of every website. I learned the standard HTML document structure, the purpose of common tags, how attributes such as class and id work, and how browsers interpret HTML to display webpages. This knowledge provides an essential foundation for web development, web application analysis, and cybersecurity testing.
