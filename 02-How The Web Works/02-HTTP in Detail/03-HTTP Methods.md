# HTTP Fundamentals

## HTTP Methods

### Overview

HTTP (HyperText Transfer Protocol) uses different request methods to define what action a client wants to perform on a web server.

Whenever a browser, application, or API communicates with a server, it sends an HTTP request containing a specific method that tells the server what operation should be performed.

The most commonly used HTTP methods are:

```text
GET
POST
PUT
DELETE
```

---

## GET Method

### What is GET?

The GET method is used to retrieve information from a web server.

It requests existing resources without modifying any data on the server.

### Example

```http
GET /index.html HTTP/1.1
Host: example.com
```

### Common Uses

* Opening web pages
* Viewing blog posts
* Retrieving API data
* Loading images and files

### Characteristics

* Retrieves data only
* Does not modify server data
* Fast and widely used
* Can be cached by browsers

---

## POST Method

### What is POST?

The POST method is used to send data to a web server.

It is commonly used when creating new records or submitting information through forms.

### Example

```http
POST /register HTTP/1.1
Host: example.com
```

### Common Uses

* User registration
* Login forms
* Uploading files
* Creating database records

### Characteristics

* Sends data to the server
* Creates new resources
* Data is placed inside the request body
* Not typically cached

---

## PUT Method

### What is PUT?

The PUT method is used to update existing information on a server.

It sends updated data and replaces or modifies an existing resource.

### Example

```http
PUT /users/1 HTTP/1.1
Host: example.com
```

### Common Uses

* Updating user profiles
* Editing account information
* Modifying existing records

### Characteristics

* Updates existing data
* Replaces or modifies resources
* Commonly used in REST APIs

---

## DELETE Method

### What is DELETE?

The DELETE method is used to remove resources from a web server.

### Example

```http
DELETE /users/1 HTTP/1.1
Host: example.com
```

### Common Uses

* Deleting user accounts
* Removing database records
* Deleting uploaded files

### Characteristics

* Removes resources permanently
* Requires proper authorization
* Commonly used in REST APIs

---

## HTTP Methods Comparison

| Method | Purpose       | Action |
| ------ | ------------- | ------ |
| GET    | Retrieve Data | Read   |
| POST   | Submit Data   | Create |
| PUT    | Update Data   | Update |
| DELETE | Remove Data   | Delete |

---

## Real-World Example

Imagine an online shopping website:

### View Product

```text
GET /products/10
```

The website retrieves product information.

### Place an Order

```text
POST /orders
```

The website creates a new order.

### Update Shipping Address

```text
PUT /orders/10
```

The website updates order details.

### Cancel Order

```text
DELETE /orders/10
```

The website removes the order.

---

## Key Notes

* HTTP methods tell a server what action should be performed.
* GET retrieves information from a server.
* POST submits data and creates new records.
* PUT updates existing resources.
* DELETE removes resources from a server.
* GET and POST are the most frequently used HTTP methods.
* PUT and DELETE are commonly used in APIs and web applications.

---

## Learning Outcome

After completing this section, I understood how HTTP methods control communication between clients and web servers. I learned the differences between GET, POST, PUT, and DELETE requests, their real-world applications, and how they are used to perform Create, Read, Update, and Delete (CRUD) operations in modern web applications.
