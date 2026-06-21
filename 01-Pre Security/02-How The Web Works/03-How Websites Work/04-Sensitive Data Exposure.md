# Sensitive Data Exposure

## Overview

Sensitive Data Exposure occurs when a website unintentionally reveals confidential information to users through its frontend code, files, or responses.

This happens when developers fail to properly protect, remove, or hide sensitive information before publishing a website.

---

## What is Sensitive Data?

Sensitive data includes any information that should not be publicly accessible.

Examples:

* Usernames
* Passwords
* API Keys
* Authentication Tokens
* Database Credentials
* Private URLs
* Internal IP Addresses
* Configuration Files
* Personal User Information

---

## How Sensitive Data Gets Exposed

Websites are built using:

* HTML
* CSS
* JavaScript

Since browsers receive these files directly, users can inspect them through:

```text
View Page Source
```

or

```text
Developer Tools (F12)
```

If developers accidentally leave sensitive information inside the code, anyone can discover it.

---

## Common Examples of Sensitive Data Exposure

### Hardcoded Credentials

Example:

```html
<!-- Temporary Login -->

Username: admin
Password: Admin123
```

An attacker viewing the page source could immediately obtain valid credentials.

---

### Hidden Links

Example:

```html
<a href="/admin-panel" style="display:none">
Admin Panel
</a>
```

Although invisible on the webpage, the link remains visible in the source code.

---

### JavaScript Secrets

Example:

```javascript
const apiKey = "ABC123SECRETKEY";
```

Anyone can inspect JavaScript files and retrieve exposed secrets.

---

### Developer Comments

Example:

```html
<!-- Test Account:
User: testuser
Pass: Password123
-->
```

Comments are not displayed on the webpage but remain visible in source code.

---

## Why Sensitive Data Exposure is Dangerous

Exposed information can help attackers:

* Access user accounts
* Discover hidden application areas
* Escalate privileges
* Access backend systems
* Bypass authentication
* Launch further attacks

---

## Real-World Attack Scenario

### Step 1

Attacker opens:

```text
View Page Source
```

---

### Step 2

Finds:

```html
<!-- Temporary Admin Login -->

admin:admin123
```

---

### Step 3

Uses credentials to log in.

---

### Step 4

Gains unauthorized access to administrative functions.

---

## How to Check for Sensitive Data Exposure

When performing a web security assessment:

### Review HTML Source

```text
Right Click → View Page Source
```

Look for:

* Credentials
* Hidden URLs
* Comments
* Tokens

---

### Inspect JavaScript Files

Check:

```text
<script src="app.js"></script>
```

Look for:

* API keys
* Secrets
* Internal endpoints

---

### Use Browser Developer Tools

Open:

```text
F12 → Sources
```

or

```text
F12 → Network
```

Inspect:

* Requests
* Responses
* JavaScript files
* Hidden resources

---

## Prevention Methods

### Remove Sensitive Information

Never store:

* Passwords
* API Keys
* Secrets

inside frontend code.

---

### Use Server-Side Storage

Store sensitive information on:

```text
Backend Servers
```

instead of:

```text
Frontend HTML/JavaScript
```

---

### Remove Developer Comments

Before deployment:

```html
<!-- Remove all testing comments -->
```

---

### Use Environment Variables

Store secrets securely using:

```text
Environment Variables
```

instead of hardcoding them.

---

### Principle of Least Exposure

Only expose information that users actually need.

---

## Common Locations to Check During Pentesting

| Location            | What to Look For      |
| ------------------- | --------------------- |
| HTML Source         | Credentials, Comments |
| JavaScript Files    | API Keys, Tokens      |
| Hidden Inputs       | Internal Values       |
| Network Responses   | Sensitive Data        |
| Robots.txt          | Hidden Directories    |
| Configuration Files | Secrets               |

---

## Key Notes

* Sensitive Data Exposure occurs when confidential information is visible to users.
* Frontend source code is one of the first places attackers inspect.
* HTML comments often reveal useful information.
* Hidden links can expose administrative areas.
* JavaScript files may contain API keys or secrets.
* Sensitive information should always remain on the server side.
* Reviewing source code is one of the first steps in web application security testing.

---

## Learning Outcome

After completing this section, I understood what Sensitive Data Exposure is, how sensitive information can accidentally appear in HTML and JavaScript source code, why exposed credentials are dangerous, and how attackers leverage this information to gain unauthorized access. I also learned how to identify exposed data during security assessments and the best practices for preventing such vulnerabilities in web applications.
