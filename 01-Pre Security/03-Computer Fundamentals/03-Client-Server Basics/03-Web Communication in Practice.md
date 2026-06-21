# Client-Server Basics

## Web Communication in Practice

### Overview

When we browse websites, our browsers communicate with web servers using a protocol called **HTTP (Hypertext Transfer Protocol)** or its secure version, **HTTPS (Hypertext Transfer Protocol Secure)**. This protocol allows clients (web browsers) and servers (web servers) to exchange information across the Internet.

HTTP is the foundation of web communication and is one of the most important protocols in networking, web development, and cybersecurity.

---

## Main Concept

### What is HTTP(S)?

HTTP(S) is a **stateless client-server protocol** used to transfer web content between clients and servers.

Basic Communication Flow:

```text
Browser (Client)
        ↓ Request
Web Server
        ↓ Response
Browser
```

Examples of web content:

```text
HTML Pages
Images
CSS Files
JavaScript Files
Videos
Documents
```

---

### What Does "Stateless" Mean?

HTTP treats every request as an independent request.

The server does not automatically remember previous requests.

Example:

```text
Request 1 → Login
Request 2 → Open Profile
Request 3 → View Settings
```

Without additional mechanisms, the server would not know these requests came from the same user.

---

### How Modern Websites Maintain State

Web applications use:

```text
Cookies
Session IDs
Authentication Tokens
```

Example:

```text
User Logs In
       ↓
Server Creates Session ID
       ↓
Browser Stores Session Cookie
       ↓
Cookie Sent with Future Requests
```

This allows users to remain logged in while browsing.

---

## How It Works

### Step 1: User Requests a Website

The user enters a website address.

Example:

```text
https://tryhackme.com
```

---

### Step 2: Browser Creates HTTP Request

The browser automatically constructs an HTTP request.

Example:

```http
GET / HTTP/1.1
Host: tryhackme.com
```

---

### Step 3: Request Sent to Server

The request travels through the network.

```text
Browser
    ↓
Internet
    ↓
Web Server
```

---

### Step 4: Server Processes Request

The web server receives and processes the request.

```text
Request Received
        ↓
Resource Located
        ↓
Response Generated
```

---

### Step 5: Server Returns Response

The server sends a response back.

Example:

```http
HTTP/1.1 200 OK
```

---

### Step 6: Browser Displays Content

The browser renders the returned content.

```text
HTML
CSS
JavaScript
Images
```

Result:

```text
Web Page Displayed
```

---

## Important Components

### HTTP Methods

#### What are HTTP Methods?

HTTP methods define the action the client wants the server to perform.

The HTTP specification defines nine core methods:

```text
GET
POST
PUT
DELETE
PATCH
HEAD
OPTIONS
CONNECT
TRACE
```

---

### GET Method

#### What is GET?

GET is used to retrieve resources from a server.

Example:

```http
GET /index.html HTTP/1.1
Host: tryhackme.com
```

Purpose:

```text
Request Information
Request Files
Request Web Pages
```

---

#### Example

When a user visits:

```text
https://tryhackme.com
```

The browser sends:

```http
GET /
```

The server returns:

```text
Homepage Content
```

---

### Request Components

When inspecting a web request in browser developer tools, several important fields appear.

---

#### Scheme

Indicates which protocol was used.

Examples:

```text
HTTP
HTTPS
```

Example:

```text
https://tryhackme.com
```

Scheme:

```text
HTTPS
```

---

#### Host

The server name being contacted.

Example:

```text
tryhackme.com
```

---

#### Filename

The specific resource requested.

Example:

```text
/
```

Often translates to:

```text
index.html
```

---

#### Address

The IP address of the server.

Example:

```text
127.0.0.1
```

Meaning:

```text
Localhost
This Computer
```

---

#### Status

Indicates the result of the request.

Example:

```text
200 OK
```

Meaning:

```text
Request Successful
```

---

### Common HTTP Status Codes

#### 200 OK

```text
Success
```

The request completed successfully.

---

#### 404 Not Found

```text
Resource Not Found
```

The requested page does not exist.

---

#### 403 Forbidden

```text
Access Denied
```

The server refuses access.

---

#### 500 Internal Server Error

```text
Server-Side Problem
```

The server encountered an unexpected error.

---

### HTTP Response Structure

A response contains two main sections.

---

#### Response Header

Contains metadata about the response.

Examples:

```text
Status Code
Content Type
Server Information
Date
```

---

#### Response Body

Contains the actual content requested.

Examples:

```html
<html>
<head>
<title>Welcome</title>
</head>
<body>
Hello World
</body>
</html>
```

The browser uses this content to build the webpage.

---

## Advantages / Benefits

### HTTP(S)

* Standardized web communication
* Supported by all modern browsers
* Simple request-response model
* Works across different platforms
* Enables global web access

### HTTPS

* Encrypts communication
* Protects sensitive information
* Prevents eavesdropping
* Improves user privacy

---

## Key Characteristics

* HTTP is a client-server protocol.
* HTTP is stateless by default.
* Sessions and cookies provide stateful behavior.
* GET requests retrieve resources.
* Browsers automatically generate HTTP requests.
* Servers respond with status codes and content.
* Responses contain headers and bodies.
* Developer Tools can inspect network requests and responses.

---

## Example

### Loading a Website

User enters:

```text
https://tryhackme.com
```

Communication Process:

```text
Browser Opens Website
         ↓
Creates GET Request
         ↓
Request Sent to Server
         ↓
Server Processes Request
         ↓
Returns HTTP Response
         ↓
Status: 200 OK
         ↓
HTML Returned
         ↓
Browser Renders Page
```

Example Request:

```http
GET / HTTP/1.1
Host: tryhackme.com
```

Example Response:

```http
HTTP/1.1 200 OK
Content-Type: text/html
```

---

## Key Notes

* HTTP and HTTPS power modern websites.
* HTTP is stateless by design.
* Cookies and sessions help maintain user state.
* GET is the most common method for retrieving web resources.
* HTTP requests contain important metadata such as hostnames and requested resources.
* HTTP responses include status codes and content.
* Browser Developer Tools can be used to inspect requests and responses.
* Understanding HTTP communication is essential for web security, penetration testing, vulnerability assessment, and cybersecurity analysis.

---

## Learning Outcome

After completing this section, I understood how web communication occurs using the HTTP and HTTPS protocols. I learned that HTTP is a stateless client-server protocol and how modern web applications use sessions, cookies, and authentication tokens to maintain state between requests. I explored the GET method, examined the structure of HTTP requests and responses, and learned the purpose of important fields such as Scheme, Host, Address, Filename, and Status Code. I also gained practical experience using browser developer tools to inspect web traffic, providing a strong foundation for future studies in web technologies, web application security, and penetration testing.
