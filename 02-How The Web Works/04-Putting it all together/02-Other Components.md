# Putting It All Together

## Other Components of Modern Web Infrastructure

### Overview

Modern websites rely on more than just DNS, web servers, and HTTP/HTTPS communication. To ensure scalability, availability, performance, and security, organizations use additional infrastructure components such as Load Balancers, Content Delivery Networks (CDNs), Databases, and Web Application Firewalls (WAFs). These components work together to provide a fast, reliable, and secure experience for users worldwide.

---

## Main Concept

### What are Other Web Components?

Other web components are supporting technologies that enhance the functionality, performance, and security of web applications.

These components help organizations:

* Handle large amounts of traffic
* Improve website speed
* Store and manage data
* Protect against cyber attacks
* Ensure service availability

Common supporting components include:

```text
Load Balancer
CDN (Content Delivery Network)
Database
WAF (Web Application Firewall)
```

---

## How It Works

### Load Balancer Workflow

1. User sends a request to a website.
2. Request reaches the load balancer first.
3. Load balancer analyzes server availability.
4. It selects the most suitable server.
5. Request is forwarded to that server.
6. Server processes the request and returns a response.
7. Load balancer continues monitoring server health.

---

### CDN Workflow

1. User requests a static file.
2. CDN identifies the nearest edge server.
3. Content is delivered from the closest location.
4. Website loads faster with reduced latency.

---

### Database Workflow

1. User submits information.
2. Web server sends the data to a database.
3. Database stores the information.
4. When needed, the server retrieves data from the database.
5. Information is displayed to the user.

---

### WAF Workflow

1. User sends a web request.
2. Request passes through the WAF.
3. WAF analyzes traffic for suspicious behavior.
4. Malicious requests are blocked.
5. Legitimate requests are forwarded to the web server.

---

## Important Components

### Load Balancer

A Load Balancer distributes incoming traffic across multiple servers to improve performance and availability.

#### Functions

* Traffic Distribution
* High Availability
* Failover Protection
* Server Health Monitoring

#### Common Load Balancing Algorithms

##### Round Robin

Traffic is distributed sequentially among servers.

Example:

```text
Request 1 → Server A
Request 2 → Server B
Request 3 → Server C
Request 4 → Server A
```

##### Weighted Load Balancing

Traffic is directed to the least busy or highest-capacity server.

Example:

```text
Server A = 20 Requests
Server B = 5 Requests

Next Request → Server B
```

#### Health Checks

Load balancers periodically verify whether servers are functioning correctly.

If a server becomes unavailable:

```text
Healthy → Receives Traffic
Unhealthy → Removed from Traffic Pool
```

---

### CDN (Content Delivery Network)

A CDN is a globally distributed network of servers that delivers static content from locations closest to users.

#### Common Static Content

```text
Images
CSS Files
JavaScript Files
Videos
Fonts
```

#### Benefits

* Reduced Latency
* Faster Website Loading
* Reduced Server Load
* Better User Experience

#### Example

Without CDN:

```text
Bangladesh User
      ↓
USA Server
```

With CDN:

```text
Bangladesh User
      ↓
Nearest CDN Edge Server
```

Content loads significantly faster.

---

### Database

A Database is a structured system used to store, manage, and retrieve website information.

#### Functions

* Store User Accounts
* Store Password Hashes
* Store Website Content
* Store Transactions
* Store Logs and Analytics

#### Popular Databases

```text
MySQL
Microsoft SQL Server (MSSQL)
MongoDB
PostgreSQL
```

#### Example Data

```sql
SELECT username
FROM users;
```

#### Database Types

##### Relational Databases

Store data in tables.

Examples:

```text
MySQL
PostgreSQL
MSSQL
```

##### NoSQL Databases

Store flexible, document-based data.

Example:

```text
MongoDB
```

---

### WAF (Web Application Firewall)

A WAF is a security layer positioned between users and the web server.

#### Primary Purpose

Protect web applications from malicious traffic and attacks.

#### Security Functions

* Request Inspection
* Attack Detection
* Bot Filtering
* Rate Limiting
* Traffic Monitoring

#### Common Threats Blocked

```text
SQL Injection
Cross-Site Scripting (XSS)
Command Injection
Directory Traversal
DDoS Attempts
Malicious Bots
```

#### Rate Limiting

Limits the number of requests allowed from a single IP address.

Example:

```text
Allowed:
100 Requests / Minute

Exceed Limit:
Blocked Temporarily
```

#### Request Filtering

```text
Normal Request
       ↓
Allowed

Malicious Request
       ↓
Blocked
```

---

## Advantages / Benefits

### Load Balancer

* Distributes traffic efficiently
* Prevents server overload
* Improves availability
* Supports failover mechanisms

### CDN

* Faster content delivery
* Reduced latency
* Lower bandwidth costs
* Better global accessibility

### Database

* Organized data storage
* Fast retrieval of information
* Scalability
* Data consistency

### WAF

* Protection against web attacks
* Traffic filtering
* Rate limiting
* Reduced attack surface

---

## Key Characteristics

* Load balancers distribute requests across multiple servers.
* Health checks identify unhealthy servers automatically.
* CDNs store and serve static content globally.
* Databases manage website information and user data.
* WAFs inspect and filter incoming web traffic.
* Rate limiting prevents excessive requests from attackers.
* These components improve security, performance, reliability, and scalability.
* Large-scale websites rely heavily on these technologies.

---

## Example

### User Accessing an E-Commerce Website

```text
User
 ↓
WAF
 ↓
Load Balancer
 ↓
Web Server
 ↓
Database
```

Static content:

```text
Images
CSS
JavaScript
```

is served through:

```text
CDN
```

Process:

1. User sends request.
2. WAF inspects traffic.
3. Load Balancer selects an available server.
4. Web Server processes request.
5. Database provides required data.
6. CDN delivers images and static files.
7. Website loads quickly and securely.

---

## Key Notes

* Load Balancers improve performance and provide failover support.
* Health Checks ensure only healthy servers receive traffic.
* CDNs reduce latency by serving content from nearby locations.
* Databases store and manage website information.
* WAFs protect web applications from common cyber attacks.
* Rate Limiting helps mitigate abuse and denial-of-service attempts.
* These technologies form the backbone of modern large-scale web applications.
* Understanding these components is essential for web security assessments and penetration testing.

---

## Learning Outcome

After completing this section, I understood the critical supporting components that make modern websites scalable, reliable, and secure. I learned how Load Balancers distribute traffic and perform health checks, how CDNs improve performance by delivering content from geographically closer servers, how databases store and retrieve application data, and how Web Application Firewalls protect web applications from attacks such as SQL Injection, XSS, and denial-of-service attempts. This knowledge provides a strong foundation for understanding enterprise web architectures and cybersecurity defenses.
