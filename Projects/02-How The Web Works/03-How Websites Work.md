# How Websites Work

## Project Overview

This project focused on understanding how websites function, how web technologies interact, and how common web security vulnerabilities can be identified. The practical exercises covered website architecture, HTML, JavaScript, Sensitive Data Exposure, and HTML Injection.

Throughout the project, I explored both the development and security perspectives of modern web applications by analyzing source code, manipulating webpage content, and identifying security weaknesses.

---

# Website Architecture

## Understanding How Websites Work

A website operates through communication between a client (browser) and a server.

### Components of a Website

### Front-End (Client-Side)

The Front-End is the portion of a website rendered directly inside the user's browser.

Examples include:

* Text
* Images
* Buttons
* Forms
* Navigation Menus

### Back-End (Server-Side)

The Back-End processes requests from users and returns appropriate responses.

Examples include:

* Authentication Systems
* Databases
* APIs
* Business Logic

---

## Practical Result

### Question

What term best describes the component of a web application rendered by your browser?

### Answer

```text
Front End
```

### How I Completed It

I reviewed the website architecture explanation and identified that anything displayed and interacted with through the browser belongs to the Front-End (Client-Side) component.

---

# HTML Fundamentals

## Understanding HTML

HTML (HyperText Markup Language) is the foundation of every website.

HTML defines:

* Website Structure
* Content Layout
* Page Elements

Common HTML elements include:

```html
<h1>Heading</h1>
<p>Paragraph</p>
<img src="image.png">
<button>Click Me</button>
```

---

## Practical Exercise 1

### Objective

Render HTML code inside the provided editor.

### Result

```text
HTML_HERO
```

### How I Completed It

I entered valid HTML code into the editor and rendered the page successfully. After the HTML was processed correctly, the hidden flag became visible.

---

## Practical Exercise 2

### Objective

Fix the broken image.

### Result

```text
HTML_IS_FUN
```

### How I Completed It

I analyzed the HTML source code and identified an incorrect image path. After correcting the image source reference, the image loaded successfully and revealed the hidden text.

---

## Practical Exercise 3

### Objective

Add a dog image to the webpage.

### HTML Used

```html
<img src="img/dog-1.png">
```

### Result

```text
DOGS_RULE
```

### How I Completed It

I inserted the required image tag into the HTML document, rendered the page again, and extracted the hidden text displayed inside the dog image.

---

# JavaScript Fundamentals

## Understanding JavaScript

JavaScript adds functionality and interactivity to web pages.

Examples include:

* Dynamic Content Updates
* Form Validation
* Animations
* Interactive Buttons

---

## Practical Exercise 1

### Objective

Change the content of the demo element.

### Result

```text
Hack the Planet
```

### JavaScript Used

```javascript
document.getElementById("demo").innerHTML = "Hack the Planet";
```

### How I Completed It

I located the target element using its ID and modified its content using JavaScript DOM manipulation.

---

## Practical Exercise 2

### Objective

Create a button that changes text when clicked.

### Result

```text
Button Clicked
```

### How I Completed It

I implemented the provided button code, rendered the page, and triggered the onclick event to update the displayed text.

---

# Sensitive Data Exposure

## Understanding the Vulnerability

Sensitive Data Exposure occurs when confidential information is accidentally exposed within frontend source code.

Common examples include:

* Passwords
* API Keys
* Tokens
* Hidden URLs
* Developer Notes

---

## Practical Exercise

### Objective

Inspect the source code of the website.

### Result

```text
testpasswd
```

### How I Completed It

I opened the webpage source code using the browser's source inspection feature and searched for hidden credentials. The password was exposed within the source code and was successfully identified.

---

## Security Lesson Learned

Never store:

* Credentials
* API Keys
* Secrets

inside client-side code because attackers can easily access them through source code inspection.

---

# HTML Injection

## Understanding HTML Injection

HTML Injection occurs when user input is displayed without sanitization.

### Vulnerable Flow

```text
User Input
     ↓
No Validation
     ↓
Rendered as HTML
```

This allows attackers to inject their own HTML elements into the webpage.

---

## Practical Exercise

### Objective

Inject a malicious hyperlink into the webpage.

### Payload Example

```html
<a href="http://hacker.com">Click Here</a>
```

### Result

```text
HTML_INJ3CTI0N
```

### How I Completed It

I entered HTML code into the vulnerable input field. Because the application failed to sanitize user input, the browser rendered the injected hyperlink successfully, revealing the challenge flag.

---

# Security Concepts Learned

## Sensitive Data Exposure

### Risks

* Credential Leakage
* Information Disclosure
* Unauthorized Access

### Prevention

* Remove sensitive information from source code.
* Store secrets on backend systems.
* Conduct source code reviews before deployment.

---

## HTML Injection

### Risks

* Website Defacement
* Fake Content Injection
* Social Engineering Attacks

### Prevention

* Input Validation
* Input Sanitization
* Output Encoding
* Secure Development Practices

---

# Challenge Results

| Task                        | Objective                           | Result          |
| --------------------------- | ----------------------------------- | --------------- |
| Website Architecture        | Identify browser-rendered component | Front End       |
| HTML Rendering              | Render HTML successfully            | HTML_HERO       |
| Broken Image Analysis       | Fix image path                      | HTML_IS_FUN     |
| HTML Image Injection        | Add dog image                       | DOGS_RULE       |
| JavaScript DOM Manipulation | Modify content                      | Hack the Planet |
| JavaScript Event Handling   | Trigger button event                | Button Clicked  |
| Source Code Review          | Find hidden password                | testpasswd      |
| HTML Injection              | Inject malicious HTML               | HTML_INJ3CTI0N  |

---

# Project Outcome

By completing this project, I gained practical knowledge of website architecture, client-side technologies, and fundamental web security concepts. I learned how HTML structures webpages, how JavaScript controls dynamic behavior, how source code can unintentionally expose sensitive information, and how input validation failures can lead to HTML Injection vulnerabilities.

This project strengthened my understanding of both web development fundamentals and introductory web application security assessment techniques, providing a solid foundation for advanced topics such as Cross-Site Scripting (XSS), Authentication Security, and Web Application Penetration Testing.
