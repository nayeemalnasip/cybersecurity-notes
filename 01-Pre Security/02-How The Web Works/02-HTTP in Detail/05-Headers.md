# HTTP Fundamentals

## HTTP Headers

### Overview

HTTP Headers are additional pieces of information sent between a client (browser) and a web server during HTTP communication.

Headers help both sides understand:

* Who is making the request.
* What data is being sent.
* How data should be processed.
* How data should be stored or cached.

Without headers, modern websites would not function properly because servers rely on this information to deliver content correctly.

---

## What Are HTTP Headers?

Headers are key-value pairs that provide extra information during an HTTP request or response.

### Example Request Header

```http
GET / HTTP/1.1
Host: example.com
User-Agent: Mozilla/5.0
```

In this example:

```text
Host = example.com
User-Agent = Mozilla/5.0
```

These values provide important details to the server.

---

# Common Request Headers

Request headers are sent from the client (browser) to the server.

---

## Host Header

### Purpose

The Host header tells the web server which website the client wants to access.

### Example

```http
Host: tryhackme.com
```

### Why It Is Important

A single server can host multiple websites.

Without the Host header, the server would not know which website to return.

### Example

```text
Server IP:
192.168.1.10

Hosted Websites:
site1.com
site2.com
site3.com
```

The Host header specifies the desired website.

---

## User-Agent Header

### Purpose

Identifies the browser, operating system, and software version making the request.

### Example

```http
User-Agent: Mozilla/5.0 Firefox/87.0
```

### Why It Is Important

Web servers can:

* Optimize content for browsers.
* Enable browser-specific features.
* Provide compatible website versions.

### Common Information

```text
Browser Name
Browser Version
Operating System
Device Type
```

---

## Content-Length Header

### Purpose

Tells the server how much data is being sent.

### Example

```http
Content-Length: 150
```

### Why It Is Important

When uploading data such as:

* Forms
* Files
* Login credentials

The server needs to know the exact size of the incoming data.

---

## Accept-Encoding Header

### Purpose

Tells the server which compression methods the browser supports.

### Example

```http
Accept-Encoding: gzip, deflate
```

### Why It Is Important

Compressed data:

* Loads faster
* Uses less bandwidth
* Improves performance

---

## Cookie Header

### Purpose

Sends stored user information back to the server.

### Example

```http
Cookie: sessionid=abc123
```

### Common Uses

* User authentication
* Session management
* Personalization
* Shopping carts

---

# Common Response Headers

Response headers are sent from the server back to the client.

---

## Set-Cookie Header

### Purpose

Stores information in the user's browser.

### Example

```http
Set-Cookie: sessionid=abc123
```

### Why It Is Important

Used for:

* Login sessions
* User tracking
* Remember Me functionality
* Preferences storage

---

## Cache-Control Header

### Purpose

Controls how long content should remain in browser cache.

### Example

```http
Cache-Control: max-age=3600
```

### Meaning

```text
3600 seconds = 1 hour
```

The browser can use cached content for one hour before requesting it again.

### Benefits

* Faster page loading
* Reduced bandwidth usage
* Better user experience

---

## Content-Type Header

### Purpose

Tells the browser what type of data is being returned.

### Example

```http
Content-Type: text/html
```

### Common Content Types

| Content Type           | Description  |
| ---------------------- | ------------ |
| text/html              | HTML Page    |
| text/css               | CSS File     |
| application/javascript | JavaScript   |
| image/png              | PNG Image    |
| application/pdf        | PDF Document |
| video/mp4              | Video File   |

### Why It Is Important

The browser uses this information to properly display or process content.

---

## Content-Encoding Header

### Purpose

Specifies how the response data was compressed.

### Example

```http
Content-Encoding: gzip
```

### Benefits

* Smaller response size
* Faster downloads
* Reduced network traffic

---

# Request vs Response Headers

| Request Headers | Response Headers |
| --------------- | ---------------- |
| Host            | Set-Cookie       |
| User-Agent      | Cache-Control    |
| Content-Length  | Content-Type     |
| Accept-Encoding | Content-Encoding |
| Cookie          | Set-Cookie       |

---

# Real-World Example

### Client Request

```http
GET / HTTP/1.1
Host: tryhackme.com
User-Agent: Firefox/87.0
Accept-Encoding: gzip
Cookie: sessionid=abc123
```

### Server Response

```http
HTTP/1.1 200 OK
Content-Type: text/html
Content-Encoding: gzip
Cache-Control: max-age=3600
Set-Cookie: userid=12345
```

Communication flow:

```text
Browser → Request Headers → Server
Server → Response Headers → Browser
```

---

## Cyber Security Perspective

HTTP Headers are extremely important during:

* Web Application Testing
* Penetration Testing
* Security Assessments
* Bug Bounty Hunting

Security professionals often analyze headers to identify:

* Server software
* Session handling
* Authentication mechanisms
* Security misconfigurations
* Information leakage

Examples:

```text
Server Header → Reveals server software
Set-Cookie → Reveals session tokens
Content-Type → Helps identify file handling
Cache-Control → Impacts sensitive data exposure
```

---

## Key Notes

* HTTP headers provide additional information during communication.
* Request headers are sent from client to server.
* Response headers are sent from server to client.
* Host identifies the target website.
* User-Agent identifies the client software.
* Content-Length specifies data size.
* Accept-Encoding enables compression.
* Cookies store session and user information.
* Content-Type defines the data format.
* Cache-Control manages browser caching.
* Headers are widely used during web security testing.

---

## Learning Outcome

After completing this section, I understood how HTTP headers provide essential information during communication between browsers and web servers. I learned the purpose of common request and response headers, how they influence web functionality, and why they are important for performance, session management, and cybersecurity analysis.
