# Putting It All Together

## How Web Servers Work

### Overview

A web server is one of the most important components of modern web applications. It is responsible for receiving client requests, processing them, and delivering web content through the HTTP/HTTPS protocols. Web servers can host multiple websites, serve both static and dynamic content, and execute backend scripts that generate interactive web pages. Understanding how web servers operate is fundamental for web application security, penetration testing, and cybersecurity analysis.

---

## Main Concept

### What is a Web Server?

A Web Server is software that listens for incoming HTTP or HTTPS requests from clients (such as web browsers) and responds by delivering the requested web resources.

The web server retrieves files from a predefined location known as the **Root Directory** and sends them to users over the network.

Common web server software includes:

```text
Apache HTTP Server
Nginx
Microsoft IIS
Node.js
```

These servers are responsible for:

* Handling client requests
* Serving website content
* Managing virtual hosts
* Executing backend applications
* Communicating with databases
* Delivering dynamic web pages

---

## How It Works

### Step 1: User Requests a Website

The user enters a URL into a browser.

Example:

```text
http://www.example.com/picture.jpg
```

---

### Step 2: Browser Sends HTTP Request

The browser sends an HTTP request to the web server.

```http
GET /picture.jpg HTTP/1.1
Host: www.example.com
```

---

### Step 3: Web Server Receives Request

The web server listens on ports:

```text
HTTP  → Port 80
HTTPS → Port 443
```

It receives the request and determines which file is being requested.

---

### Step 4: Locate File in Root Directory

The web server searches for the requested file inside its configured root directory.

Linux (Apache/Nginx):

```bash
/var/www/html
```

Windows (IIS):

```text
C:\inetpub\wwwroot
```

Example:

```text
URL:
http://www.example.com/picture.jpg

Server File:
 /var/www/html/picture.jpg
```

---

### Step 5: Send Response

The file is returned to the client through an HTTP response.

```http
HTTP/1.1 200 OK
Content-Type: image/jpeg
```

The browser then displays the content.

---

## Important Components

### Root Directory

A Root Directory is the location where website files are stored on the server.

#### Common Locations

Linux:

```bash
/var/www/html
```

Windows:

```text
C:\inetpub\wwwroot
```

#### Purpose

* Stores website files
* Provides content to users
* Acts as the website's main directory

---

### Virtual Hosts

Virtual Hosts allow multiple websites to be hosted on a single web server.

Instead of requiring separate servers, multiple domains can share the same machine.

Example:

```text
one.com  → /var/www/website_one
two.com  → /var/www/website_two
```

When a request arrives:

1. Server checks the HTTP Host header.
2. Matches the hostname to a Virtual Host configuration.
3. Loads the correct website.

Example Request:

```http
GET / HTTP/1.1
Host: one.com
```

The server will serve:

```text
/var/www/website_one
```

---

### Static Content

Static Content consists of files that do not change when requested.

#### Examples

```text
HTML Files
Images
CSS Files
JavaScript Files
Videos
PDF Documents
```

#### Characteristics

* Same content for every user
* No processing required
* Faster delivery
* Lower server workload

Example:

```text
logo.png
style.css
script.js
```

---

### Dynamic Content

Dynamic Content changes depending on user actions, database information, or application logic.

#### Examples

* Blog posts
* Search results
* User profiles
* Shopping carts
* Social media feeds

#### Characteristics

* Generated in real-time
* Uses backend programming
* Often retrieves data from databases

Example:

```text
Search Query:
Cyber Security

Results:
Generated Dynamically
```

Different users may receive different content.

---

### Frontend

The Frontend is everything users can see and interact with inside their browser.

#### Components

```text
HTML
CSS
JavaScript
Images
Videos
```

#### Responsibilities

* User Interface
* Design
* Layout
* User Interaction

Example:

```html
<h1>Welcome to My Website</h1>
```

Users can view this code after it is rendered.

---

### Backend

The Backend operates behind the scenes and processes application logic.

#### Responsibilities

* Process Requests
* Execute Code
* Access Databases
* Handle Authentication
* Generate Dynamic Content

Users cannot directly see backend code.

Example Workflow:

```text
User Request
      ↓
Backend Processing
      ↓
Database Query
      ↓
HTML Response
```

---

### Scripting and Backend Languages

Backend languages enable websites to become interactive and dynamic.

#### Popular Backend Languages

```text
PHP
Python
Ruby
Node.js
Perl
```

#### Capabilities

* Process user input
* Query databases
* Generate webpages
* Communicate with APIs
* Perform authentication
* Handle business logic

---

### PHP Example

User Request:

```text
http://example.com/index.php?name=adam
```

Backend Code:

```php
<?php
$name = $_GET['name'];
echo "Hello " . $name;
?>
```

Output Sent to Browser:

```html
Hello adam
```

Important:

```text
User Sees:
Hello adam

User Does NOT See:
PHP Source Code
```

The server executes PHP on the backend and only sends the generated result.

---

## Advantages / Benefits

### Web Servers

* Deliver website content efficiently
* Handle multiple client connections
* Support multiple websites
* Enable dynamic web applications
* Integrate with databases
* Provide scalable web hosting

### Virtual Hosts

* Host multiple domains on one server
* Reduce infrastructure costs
* Simplify management

### Dynamic Content

* Personalized user experiences
* Real-time updates
* Interactive functionality

### Backend Languages

* Powerful automation
* Database integration
* Application logic processing

---

## Key Characteristics

* Web servers listen for HTTP/HTTPS requests.
* Content is served from a root directory.
* Virtual Hosts allow multiple websites on one server.
* Static content remains unchanged between requests.
* Dynamic content is generated based on application logic.
* Frontend is visible to users.
* Backend operates behind the scenes.
* Backend languages process user input and communicate with databases.
* Dynamic applications introduce additional security risks if not properly secured.

---

## Example

### User Accessing a Blog Website

```text
User
 ↓
Browser
 ↓
Web Server
 ↓
Backend Application
 ↓
Database
 ↓
Generated HTML
 ↓
Browser Display
```

Scenario:

1. User searches for "Cyber Security".
2. Web Server forwards request to backend.
3. Backend queries database.
4. Database returns matching blog posts.
5. Backend generates HTML page.
6. Browser displays search results.

Each user may receive different content depending on their request.

---

## Key Notes

* Apache, Nginx, IIS, and Node.js are common web servers.
* Web servers serve content from a configured root directory.
* Virtual Hosts enable multiple websites on a single server.
* Static content does not change between requests.
* Dynamic content is generated by backend applications.
* Frontend is visible to users; Backend remains hidden.
* Backend languages interact with databases and external services.
* Dynamic websites are more powerful but introduce additional security risks.
* Understanding frontend and backend architecture is critical for web penetration testing and vulnerability assessment.

---

## Learning Outcome

After completing this section, I understood how web servers receive and process HTTP requests, serve content from root directories, and host multiple websites using Virtual Hosts. I learned the difference between static and dynamic content, how frontend and backend components interact, and how backend programming languages such as PHP, Python, Ruby, and Node.js generate dynamic web pages. I also gained insight into how web applications communicate with databases and why backend functionality introduces additional security considerations that are important in cybersecurity and web application penetration testing.
