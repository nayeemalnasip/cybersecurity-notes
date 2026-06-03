# HTTP in Detail

## What is HTTP?

### Overview

HTTP stands for:

```text
HyperText Transfer Protocol
```

HTTP is the primary protocol used for communication between a web browser and a web server. Whenever a user visits a website, HTTP is responsible for requesting and delivering web content such as:

* HTML Pages
* Images
* Videos
* CSS Files
* JavaScript Files
* Documents

HTTP was developed by:

```text
Tim Berners-Lee
```

between:

```text
1989 – 1991
```

and became one of the foundational technologies of the World Wide Web (WWW).

---

## How HTTP Works

When a user enters a website address into a browser:

```text
https://example.com
```

the browser sends an HTTP request to the web server.

The server processes the request and returns an HTTP response containing the requested content.

### Basic Communication Flow

```text
User Browser
      │
      ▼
HTTP Request
      │
      ▼
Web Server
      │
      ▼
HTTP Response
      │
      ▼
Website Displayed
```

---

## Functions of HTTP

HTTP provides a standard set of rules that allow:

* Browsers to communicate with web servers.
* Web pages to be requested and delivered.
* Data to be exchanged across the Internet.
* Different systems and applications to understand web communication.

---

## Common Data Transferred Using HTTP

HTTP can transfer many types of content:

```text
HTML
CSS
JavaScript
Images
Videos
Audio Files
Documents
API Responses
```

---

## What is HTTPS?

### Overview

HTTPS stands for:

```text
HyperText Transfer Protocol Secure
```

HTTPS is the secure version of HTTP.

It performs the same functions as HTTP but adds encryption to protect data during transmission.

---

## Why HTTPS is Important

Without HTTPS:

```text
Data travels in plain text.
```

Attackers monitoring the network may be able to view:

* Usernames
* Passwords
* Personal Information
* Payment Details
* Sensitive Data

---

## How HTTPS Protects Data

HTTPS uses:

```text
SSL/TLS Encryption
```

to secure communication between a browser and a web server.

This encryption ensures that:

* Data cannot easily be read by attackers.
* Information remains confidential.
* Data integrity is maintained.
* Users connect to the legitimate website.

---

## HTTP vs HTTPS

| Feature                         | HTTP                        | HTTPS                              |
| ------------------------------- | --------------------------- | ---------------------------------- |
| Full Form                       | HyperText Transfer Protocol | HyperText Transfer Protocol Secure |
| Encryption                      | No                          | Yes                                |
| Data Protection                 | None                        | Encrypted                          |
| Secure Authentication           | No                          | Yes                                |
| URL Prefix                      | http://                     | https://                           |
| Recommended for Modern Websites | No                          | Yes                                |

---

## Security Benefits of HTTPS

### Confidentiality

Protects information from being viewed by unauthorized users.

### Integrity

Prevents data from being modified during transmission.

### Authentication

Helps verify that users are communicating with the correct website and not a malicious impersonator.

---

## Example

### HTTP

```text
http://example.com
```

Data is transmitted without encryption.

---

### HTTPS

```text
https://example.com
```

Data is encrypted before transmission.

---

## Key Notes

* HTTP stands for HyperText Transfer Protocol.
* HTTP is used to communicate with web servers.
* Tim Berners-Lee developed HTTP between 1989 and 1991.
* HTTP transfers webpages, images, videos, and other web content.
* HTTPS is the secure version of HTTP.
* HTTPS uses SSL/TLS encryption.
* HTTPS protects confidentiality, integrity, and authentication.
* Modern websites should always use HTTPS.

---

## Learning Outcome

After completing this section, I understood how HTTP enables communication between browsers and web servers and how HTTPS improves security through encryption. I learned the differences between HTTP and HTTPS, their roles in web communication, and why HTTPS is essential for protecting sensitive information on modern websites.
