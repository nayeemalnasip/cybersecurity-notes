# HTML Injection

## Overview

HTML Injection is a web vulnerability that occurs when a website displays user input without properly filtering or sanitizing it.

If user input is directly rendered on a webpage, an attacker can inject their own HTML code, causing the browser to interpret and display it as part of the website.

---

## What Causes HTML Injection?

The vulnerability occurs when:

```text
User Input → Website → Displayed Directly on Page
```

without validation or sanitization.

If the website trusts user input, attackers can insert HTML elements that alter the appearance or behavior of the page.

---

## Simple Example

Imagine a website asks:

```text
What's your name?
```

User enters:

```text
Nayeem
```

The website displays:

```text
Hello Nayeem
```

This is normal behavior.

---

## Vulnerable Scenario

Suppose the website directly prints whatever the user enters.

User enters:

```html
<h1>Hacked Website</h1>
```

The browser interprets it as HTML and displays:

# Hacked Website

instead of showing the text itself.

---

## How HTML Injection Works

### Normal Flow

```text
User Input
      ↓
Application
      ↓
Output as Text
```

---

### Vulnerable Flow

```text
User Input
      ↓
Application
      ↓
Output as HTML
      ↓
Browser Executes HTML
```

---

## Example Vulnerable Code

```javascript
document.getElementById("output").innerHTML = userInput;
```

Problem:

```text
innerHTML
```

interprets HTML tags.

---

### User Input

```html
<h1>Owned</h1>
```

---

### Output

```html
<h1>Owned</h1>
```

Browser renders:

```text
Owned
```

as a large heading.

---

## Potential Malicious Inputs

### Change Page Content

```html
<h1>Website Compromised</h1>
```

---

### Insert Fake Messages

```html
<p>Your account has been suspended.</p>
```

---

### Add Images

```html
<img src="image.jpg">
```

---

### Create Fake Login Forms

```html
<form>
<input placeholder="Username">
<input placeholder="Password">
</form>
```

---

## Relationship with JavaScript

HTML Injection can become more dangerous when JavaScript is allowed.

Example:

```html
<script>
alert("Attack");
</script>
```

This evolves into more severe vulnerabilities such as:

```text
Cross-Site Scripting (XSS)
```

which will be studied later in web security.

---

## Why HTML Injection is Dangerous

Attackers can:

* Deface webpages
* Display fake information
* Trick users
* Modify website appearance
* Prepare for more advanced attacks

---

## Real-World Scenario

### Website Form

```text
What's your name?
```

---

### Attacker Input

```html
<h1>Welcome Admin</h1>
```

---

### Vulnerable Application

Displays:

```html
<h1>Welcome Admin</h1>
```

---

### Browser Result

# Welcome Admin

The attacker successfully controls part of the webpage.

---

## Root Cause

The main cause is:

```text
Trusting User Input
```

Developers assume users will only enter expected data.

Attackers intentionally provide unexpected input.

---

## Input Sanitization

### What is Sanitization?

Sanitization removes or filters dangerous characters before displaying them.

Example:

User enters:

```html
<h1>Hello</h1>
```

---

Sanitized Output:

```text
&lt;h1&gt;Hello&lt;/h1&gt;
```

Now the browser displays:

```text
<h1>Hello</h1>
```

instead of rendering it as HTML.

---

## Prevention Techniques

### Validate User Input

Only allow expected characters.

Example:

```text
A-Z
a-z
0-9
```

---

### Escape HTML Characters

Convert:

```html
<
>
"
'
```

into safe representations.

---

### Avoid Direct HTML Rendering

Avoid:

```javascript
innerHTML
```

Use:

```javascript
textContent
```

instead.

Example:

```javascript
element.textContent = userInput;
```

This displays input as text rather than HTML.

---

### Server-Side Filtering

Always validate input on the server.

Never rely only on browser-side validation.

---

## Secure vs Vulnerable Example

### Vulnerable

```javascript
output.innerHTML = userInput;
```

---

### Secure

```javascript
output.textContent = userInput;
```

---

## Key Notes

* HTML Injection occurs when user input is displayed without sanitization.
* Attackers can inject HTML tags into webpages.
* Browsers render injected HTML as part of the page.
* HTML Injection can alter webpage appearance.
* Never trust user input.
* Input validation and sanitization are essential security practices.
* Using `textContent` is safer than `innerHTML`.
* HTML Injection is often a stepping stone toward more serious vulnerabilities like XSS.

---

## Learning Outcome

After completing this section, I understood how HTML Injection occurs when websites display unsanitized user input, how attackers can manipulate webpage content by injecting HTML tags, and why trusting user input is dangerous. I also learned the importance of input validation, sanitization, output encoding, and secure coding practices to prevent client-side injection vulnerabilities.
