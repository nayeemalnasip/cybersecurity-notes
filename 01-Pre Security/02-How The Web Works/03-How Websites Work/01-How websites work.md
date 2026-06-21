# How Websites Work

## Website Fundamentals

### Overview

A website is a collection of web pages that users access through a web browser such as Google Chrome, Firefox, Microsoft Edge, or Safari.

When a user visits a website, the browser sends a request to a web server. The web server processes the request and returns the required data, which the browser then displays to the user.

---

## How Websites Work

### Basic Communication Process

The communication between a browser and a web server follows a simple process:

```text
User → Browser → Web Server
                     ↓
User ← Browser ← Response
```

### Step-by-Step Process

#### Step 1: User Requests a Website

A user enters a website address (URL) into a browser.

Example:

```text
https://example.com
```

---

#### Step 2: Browser Sends Request

The browser sends an HTTP/HTTPS request to the web server hosting the website.

```text
GET / HTTP/1.1
```

---

#### Step 3: Web Server Processes Request

The server receives the request and determines what information the user needs.

The server may:

* Retrieve files
* Process data
* Query databases
* Generate dynamic content

---

#### Step 4: Server Sends Response

The server sends a response back to the browser.

The response may contain:

* HTML
* CSS
* JavaScript
* Images
* Videos
* Other resources

---

#### Step 5: Browser Renders Website

The browser interprets the received files and displays the website visually to the user.

```text
HTML → Structure
CSS → Design
JavaScript → Functionality
```

---

## Main Components of a Website

Every website is generally divided into two major parts:

### 1. Front End (Client-Side)

The Front End is everything the user sees and interacts with in their browser.

### Examples

* Buttons
* Navigation Menus
* Images
* Forms
* Text
* Animations

### Common Front-End Technologies

```text
HTML
CSS
JavaScript
```

### Responsibilities

* Display content
* Handle user interaction
* Improve user experience
* Communicate with the backend

---

## 2. Back End (Server-Side)

The Back End is responsible for processing requests and managing data behind the scenes.

Users cannot directly see the backend.

### Common Backend Functions

* Process user requests
* Handle authentication
* Access databases
* Store information
* Generate responses

### Common Backend Technologies

```text
PHP
Python
Node.js
Java
ASP.NET
```

### Responsibilities

* Business Logic
* Database Management
* Security Controls
* User Authentication
* API Processing

---

## Front End vs Back End

| Feature          | Front End             | Back End                   |
| ---------------- | --------------------- | -------------------------- |
| Runs On          | User Browser          | Web Server                 |
| Visible To User  | Yes                   | No                         |
| Purpose          | Display Information   | Process Requests           |
| Technologies     | HTML, CSS, JavaScript | PHP, Python, Java, Node.js |
| Handles Database | No                    | Yes                        |

---

## Website Communication Flow

```text
User
  ↓
Browser
  ↓
HTTP/HTTPS Request
  ↓
Web Server
  ↓
Backend Processing
  ↓
Response Sent
  ↓
Browser Renders Page
  ↓
User Views Website
```

---

## Security Perspective

Understanding how websites work is essential in cybersecurity because most modern attacks target web applications.

Examples include:

* SQL Injection (SQLi)
* Cross-Site Scripting (XSS)
* Authentication Bypass
* Session Hijacking
* File Upload Vulnerabilities

Before learning web attacks, it is important to understand how browsers, servers, and websites communicate.

---

## Key Notes

* A website consists of Front End and Back End components.
* Browsers communicate with web servers using HTTP/HTTPS.
* Front End is responsible for user interaction and display.
* Back End processes requests and manages data.
* Web servers return responses that browsers render into webpages.
* Understanding website architecture is the foundation of Web Application Security.

---

## Learning Outcome

After completing this section, I understood the basic architecture of websites, how browsers communicate with web servers, the difference between Front End and Back End components, and how web applications process user requests. This knowledge provides the foundation required for studying web application security and penetration testing.
