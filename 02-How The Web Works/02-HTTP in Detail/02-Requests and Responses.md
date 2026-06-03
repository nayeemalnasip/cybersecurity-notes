# HTTP in Detail

## Requests and Responses

### Overview

Communication between a web browser and a web server happens through:

```text
HTTP Requests
HTTP Responses
```

When a user visits a website, the browser sends a request to the web server, and the server replies with a response containing the requested content.

Before a browser can communicate with a server, it needs a URL that tells it exactly where and how to access the resource.

---

# What is a URL?

### URL (Uniform Resource Locator)

A URL is the address used to locate and access resources on the Internet.

Example:

```text
http://user:password@tryhackme.com:80/view-room?id=1#task3
```

A URL contains several components that help the browser understand how to access the resource.

---

## URL Structure

### Scheme

Specifies the protocol used for communication.

Examples:

```text
HTTP
HTTPS
FTP
```

Example:

```text
https://
```

---

### User Information

Some services allow authentication directly through a URL.

Example:

```text
user:password
```

Although this method is rarely used today due to security concerns.

---

### Host

The destination server.

Can be:

```text
Domain Name
IP Address
```

Example:

```text
tryhackme.com
```

---

### Port

Specifies which service port to connect to.

Common Ports:

```text
HTTP  = 80
HTTPS = 443
```

Possible Range:

```text
1 - 65535
```

Example:

```text
:80
```

---

### Path

Specifies the exact resource or location on the server.

Example:

```text
/view-room
```

---

### Query String

Additional information sent to the server.

Example:

```text
?id=1
```

Meaning:

```text
Request Resource ID 1
```

---

### Fragment

References a specific location on a webpage.

Example:

```text
#task3
```

Often used to jump directly to a section of a long webpage.

---

## Complete URL Breakdown

```text
http://user:password@tryhackme.com:80/view-room?id=1#task3
│
├── Scheme       → http
├── User Info    → user:password
├── Host         → tryhackme.com
├── Port         → 80
├── Path         → /view-room
├── Query String → id=1
└── Fragment     → task3
```

---

# Making an HTTP Request

When a browser needs information from a server, it sends an HTTP Request.

Basic Request:

```http
GET / HTTP/1.1
```

However, modern browsers send additional information using:

```text
HTTP Headers
```

---

## Example HTTP Request

```http
GET / HTTP/1.1
Host: tryhackme.com
User-Agent: Mozilla/5.0 Firefox/87.0
Referer: https://tryhackme.com/
```

---

## Request Breakdown

### Line 1

```http
GET / HTTP/1.1
```

Meaning:

* GET Request Method
* Request Homepage (/)
* Using HTTP Version 1.1

---

### Line 2

```http
Host: tryhackme.com
```

Specifies the website being requested.

---

### Line 3

```http
User-Agent: Mozilla/5.0 Firefox/87.0
```

Identifies the browser and version.

---

### Line 4

```http
Referer: https://tryhackme.com/
```

Indicates which page referred the user.

---

### Final Blank Line

HTTP requests always end with an empty line.

This tells the server:

```text
Request Complete
```

---

# HTTP Response

After receiving a request, the server returns an HTTP Response.

---

## Example HTTP Response

```http
HTTP/1.1 200 OK
Server: nginx/1.15.8
Date: Fri, 09 Apr 2021 13:34:03 GMT
Content-Type: text/html
Content-Length: 98
```

---

## Response Breakdown

### Status Line

```http
HTTP/1.1 200 OK
```

Contains:

* HTTP Version
* Status Code
* Status Message

Example:

```text
200 OK
```

means:

```text
Request Successful
```

---

### Server Header

```http
Server: nginx/1.15.8
```

Shows:

* Web Server Software
* Server Version

---

### Date Header

```http
Date: Fri, 09 Apr 2021 13:34:03 GMT
```

Displays:

* Current Server Date
* Time
* Timezone

---

### Content-Type Header

```http
Content-Type: text/html
```

Tells the browser what type of content is being returned.

Examples:

```text
text/html
image/png
video/mp4
application/pdf
application/json
```

---

### Content-Length Header

```http
Content-Length: 98
```

Indicates the size of the response.

Used to ensure:

```text
No Data Is Missing
```

during transmission.

---

### Blank Line

Marks the end of the HTTP headers.

---

### Response Body

Contains the actual content requested.

Examples:

* HTML Pages
* Images
* Videos
* JSON Data
* Documents

---

# HTTP Communication Flow

```text
Browser
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
Browser Renders Content
```

---

## Important Headers

### Request Headers

```text
Host
User-Agent
Referer
Cookie
Authorization
Accept
```

---

### Response Headers

```text
Server
Date
Content-Type
Content-Length
Set-Cookie
Cache-Control
```

---

## Key Notes

* URL stands for Uniform Resource Locator.
* URLs tell browsers where and how to access resources.
* HTTP communication occurs through requests and responses.
* Browsers send requests to web servers.
* Servers return responses containing requested resources.
* HTTP headers provide additional information.
* Content-Type defines the data format being returned.
* Content-Length verifies complete data delivery.
* HTTP requests and responses always end headers with a blank line.

---

## Learning Outcome

After completing this section, I understood how web browsers communicate with web servers using HTTP requests and responses. I learned how URLs are structured, how HTTP requests are formed, how servers respond with resources, and how HTTP headers provide important information during web communication.
