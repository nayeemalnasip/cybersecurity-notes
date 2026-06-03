# HTTP Fundamentals

## HTTP Status Codes

### Overview

When a client (browser) sends an HTTP request to a web server, the server responds with a status code.

An HTTP status code tells the client:

* Whether the request was successful.
* Whether the request should be redirected.
* Whether an error occurred.
* Who is responsible for the error (client or server).

Status codes are always included in the first line of an HTTP response.

Example:

```http
HTTP/1.1 200 OK
```

In this example:

```text
200 = Status Code
OK = Status Message
```

---

## HTTP Status Code Categories

HTTP status codes are divided into five major groups.

### 1xx – Informational Responses

These status codes indicate that the server has received part of the request and expects the client to continue sending data.

```text
100 – 199
```

### Purpose

* Request received.
* Continue sending data.
* Rarely seen in normal web browsing.

---

## 2xx – Success Responses

These status codes indicate that the request was completed successfully.

```text
200 – 299
```

### Purpose

* Resource retrieved successfully.
* Data processed successfully.
* Request completed without errors.

---

## 3xx – Redirection Responses

These status codes tell the client that the requested resource has moved to another location.

```text
300 – 399
```

### Purpose

* Redirect user to a different page.
* Redirect to a new domain.
* Inform search engines of page changes.

---

## 4xx – Client Error Responses

These errors occur because something is wrong with the client's request.

```text
400 – 499
```

### Purpose

* Invalid requests.
* Missing information.
* Authentication problems.
* Permission issues.

---

## 5xx – Server Error Responses

These errors occur on the server side.

```text
500 – 599
```

### Purpose

* Server malfunction.
* Application failure.
* Maintenance issues.
* Resource exhaustion.

---

# Common HTTP Status Codes

## 200 – OK

### Meaning

The request completed successfully.

### Example

```text
User opens a webpage successfully.
```

### Result

```text
Resource delivered normally.
```

---

## 201 – Created

### Meaning

A new resource has been created successfully.

### Example

```text
Creating a new user account.
Creating a new blog post.
```

### Result

```text
Resource successfully created.
```

---

## 301 – Moved Permanently

### Meaning

The resource has permanently moved to a new location.

### Example

```text
oldsite.com → newsite.com
```

### Result

```text
Browser automatically redirects.
Search engines update their records.
```

---

## 302 – Found (Temporary Redirect)

### Meaning

The resource has temporarily moved.

### Example

```text
Website maintenance page.
Temporary campaign page.
```

### Result

```text
Browser redirects temporarily.
```

---

## 400 – Bad Request

### Meaning

The request sent by the client is invalid or incomplete.

### Example

```text
Missing required parameters.
Incorrect request format.
```

### Result

```text
Server rejects the request.
```

---

## 401 – Unauthorized

### Meaning

Authentication is required before accessing the resource.

### Example

```text
Login required page.
Private dashboard.
```

### Result

```text
User must authenticate first.
```

---

## 403 – Forbidden

### Meaning

The server understands the request but refuses access.

### Example

```text
Accessing admin resources without permission.
```

### Result

```text
Access denied.
```

---

## 404 – Page Not Found

### Meaning

The requested page or resource does not exist.

### Example

```text
https://example.com/unknown-page
```

### Result

```text
Resource cannot be found.
```

---

## 405 – Method Not Allowed

### Meaning

The HTTP method used is not permitted.

### Example

```text
Sending GET request where POST is required.
```

### Result

```text
Server rejects the method.
```

---

## 500 – Internal Server Error

### Meaning

The server encountered an unexpected problem.

### Example

```text
Application crash.
Database failure.
Programming error.
```

### Result

```text
Server cannot process the request.
```

---

## 503 – Service Unavailable

### Meaning

The server is temporarily unavailable.

### Example

```text
Server maintenance.
High traffic overload.
```

### Result

```text
Service temporarily unavailable.
```

---

## HTTP Status Codes Cheat Sheet

| Status Code | Meaning                    |
| ----------- | -------------------------- |
| 200         | OK                         |
| 201         | Created                    |
| 301         | Moved Permanently          |
| 302         | Found (Temporary Redirect) |
| 400         | Bad Request                |
| 401         | Unauthorized               |
| 403         | Forbidden                  |
| 404         | Page Not Found             |
| 405         | Method Not Allowed         |
| 500         | Internal Server Error      |
| 503         | Service Unavailable        |

---

## Real-World Cyber Security Perspective

Security professionals frequently encounter HTTP status codes during:

* Web Application Testing
* Vulnerability Assessments
* Penetration Testing
* API Security Testing
* Directory Enumeration
* Access Control Testing

Examples:

```text
200 → Resource exists and accessible
401 → Authentication required
403 → Resource exists but access denied
404 → Resource does not exist
500 → Potential application error worth investigating
```

These responses often provide valuable information during reconnaissance and security assessments.

---

## Key Notes

* HTTP status codes indicate the result of a server request.
* Status codes are divided into 5 categories (1xx–5xx).
* 2xx responses indicate success.
* 3xx responses indicate redirection.
* 4xx responses indicate client-side errors.
* 5xx responses indicate server-side errors.
* 404 is the most common "Page Not Found" error.
* 500 indicates an internal server problem.
* Understanding status codes is essential for web troubleshooting and cybersecurity testing.

---

## Learning Outcome

After completing this section, I understood how HTTP status codes communicate the outcome of requests between clients and web servers. I learned the five status code categories, the purpose of common responses such as 200, 301, 404, and 500, and how these codes are used during web application analysis, troubleshooting, and cybersecurity assessments.
