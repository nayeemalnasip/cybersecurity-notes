# HTTP in Detail - Project Summary

## Project Overview

This project focused on understanding how the **HyperText Transfer Protocol (HTTP)** works and how web browsers communicate with web servers. Throughout the room, I explored the differences between HTTP and HTTPS, learned how requests and responses are exchanged, studied HTTP methods, status codes, headers, cookies, and completed practical exercises involving real HTTP requests.

---

## Task Completion Process

### Understanding HTTP and HTTPS

The first section introduced the foundation of web communication.

I learned that **HTTP (HyperText Transfer Protocol)** is the protocol used to transfer web content such as HTML pages, images, videos, and other resources between clients and servers.

I also explored **HTTPS (HyperText Transfer Protocol Secure)**, which adds encryption to HTTP communications. HTTPS protects data confidentiality and ensures communication with the legitimate web server.

### Key Concepts Learned

```text
HTTP  = HyperText Transfer Protocol
HTTPS = HyperText Transfer Protocol Secure
```

### Outcome

* Understood the purpose of HTTP.
* Learned the difference between HTTP and HTTPS.
* Recognized the importance of encryption in web communication.

---

## Requests and Responses

The next section focused on how browsers communicate with web servers using HTTP requests and responses.

I learned that every web interaction begins with a request from the client and ends with a response from the server.

### URL Structure

A URL contains several important components:

```text
Scheme
Host
Port
Path
Query String
Fragment
```

### Example URL

```text
http://user:password@tryhackme.com:80/view-room?id=1#task3
```

### Common Response Information

A web server typically responds with:

* HTTP Version
* Status Code
* Content Type
* Content Length
* Requested Data

### Outcome

* Understood the structure of URLs.
* Learned how HTTP requests are constructed.
* Understood how web servers return responses.

---

## HTTP Methods

HTTP methods define the action a client wants to perform on a resource.

### Common HTTP Methods

| Method | Purpose              |
| ------ | -------------------- |
| GET    | Retrieve information |
| POST   | Create new data      |
| PUT    | Update existing data |
| DELETE | Remove data          |

### Practical Understanding

```text
GET     → View data
POST    → Create data
PUT     → Update data
DELETE  → Remove data
```

### Outcome

* Learned the most common HTTP methods.
* Understood how applications interact with web servers.
* Identified appropriate methods for different operations.

---

## HTTP Status Codes

Web servers use status codes to inform clients about the result of their requests.

### Status Code Categories

| Range   | Meaning       |
| ------- | ------------- |
| 100-199 | Informational |
| 200-299 | Success       |
| 300-399 | Redirection   |
| 400-499 | Client Errors |
| 500-599 | Server Errors |

### Common Status Codes

| Code | Meaning               |
| ---- | --------------------- |
| 200  | OK                    |
| 201  | Created               |
| 301  | Moved Permanently     |
| 302  | Found                 |
| 400  | Bad Request           |
| 401  | Not Authorized        |
| 403  | Forbidden             |
| 404  | Page Not Found        |
| 405  | Method Not Allowed    |
| 500  | Internal Server Error |
| 503  | Service Unavailable   |

### Outcome

* Learned how web servers communicate success and failure.
* Understood common HTTP error codes.
* Improved ability to troubleshoot web applications.

---

## HTTP Headers

Headers provide additional information during communication between clients and servers.

### Common Request Headers

| Header          | Purpose                       |
| --------------- | ----------------------------- |
| Host            | Specifies target website      |
| User-Agent      | Browser information           |
| Content-Length  | Size of data being sent       |
| Accept-Encoding | Supported compression methods |
| Cookie          | Sends stored user information |

### Common Response Headers

| Header           | Purpose                       |
| ---------------- | ----------------------------- |
| Set-Cookie       | Stores cookie on client       |
| Cache-Control    | Controls browser caching      |
| Content-Type     | Defines returned content type |
| Content-Encoding | Indicates compression method  |

### Outcome

* Understood how headers influence communication.
* Learned how browsers identify themselves.
* Explored content handling and caching mechanisms.

---

## Cookies

Cookies are small pieces of data stored on a user's device by a web server.

Because HTTP is stateless, cookies allow websites to remember users between requests.

### Common Uses of Cookies

* User Authentication
* Session Management
* Personal Preferences
* Tracking User Activity

### Cookie Workflow

```text
Server → Set-Cookie
Browser → Stores Cookie
Browser → Sends Cookie on Future Requests
```

### Outcome

* Learned how websites maintain sessions.
* Understood authentication using cookies.
* Explored browser cookie storage and transmission.

---

## Practical HTTP Exercises

To reinforce the concepts learned, I completed multiple practical challenges involving HTTP requests.

### Activities Completed

#### GET Request

```text
GET /room
```

#### GET Request with Parameter

```text
GET /blog?id=1
```

#### DELETE Request

```text
DELETE /user/1
```

#### PUT Request

```text
PUT /user/2
username=admin
```

#### POST Request

```text
POST /login
username=thm
password=letmein
```

### Outcome

* Practiced constructing HTTP requests.
* Applied HTTP methods in real scenarios.
* Gained experience interacting with web applications.

---

## Skills Demonstrated

* HTTP Fundamentals
* HTTPS Security
* URL Structure Analysis
* HTTP Request & Response Processing
* HTTP Methods (GET, POST, PUT, DELETE)
* HTTP Status Code Interpretation
* HTTP Header Analysis
* Cookie Management
* Web Application Communication
* Basic Web Troubleshooting

---

## Project Conclusion

By completing this room, I gained a solid understanding of how web communication works through HTTP and HTTPS. I learned how browsers interact with servers using requests and responses, how HTTP methods control actions on resources, how status codes indicate outcomes, and how headers and cookies support web functionality. The practical exercises provided hands-on experience with real-world HTTP interactions, creating a strong foundation for future web application security testing and penetration testing activities.
