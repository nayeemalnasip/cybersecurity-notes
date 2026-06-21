# DNS in Detail

## What is DNS?

### Overview

The **Domain Name System (DNS)** is a core Internet service that translates human-readable domain names into machine-readable IP addresses.

Every device connected to the Internet has a unique IP address that is used for communication. However, remembering numerical IP addresses for every website would be difficult for users.

DNS solves this problem by allowing people to use easy-to-remember domain names instead of numerical IP addresses.

---

## Why DNS is Important

Without DNS, users would need to remember IP addresses for every website they want to visit.

For example, instead of typing:

```text
104.26.10.229
```

Users can simply enter:

```text
tryhackme.com
```

DNS automatically translates the domain name into the correct IP address and directs the request to the appropriate server.

---

## Domain Names

### What is a Domain Name?

A domain name is a human-readable address used to identify a website on the Internet.

Examples:

```text
tryhackme.com
google.com
github.com
facebook.com
```

Domain names make Internet navigation easier and more user-friendly.

---

## IP Addresses

### What is an IP Address?

An IP address is a unique numerical identifier assigned to a device connected to a network.

Example:

```text
104.26.10.229
```

Computers and networking devices use IP addresses to locate and communicate with one another.

---

## DNS Resolution Process

When a user enters a website address into a browser, DNS performs a lookup to find the corresponding IP address.

### Example

User enters:

```text
tryhackme.com
```

DNS translates it into:

```text
104.26.10.229
```

The browser then uses this IP address to establish communication with the web server hosting the website.

---

## How DNS Simplifies Internet Usage

DNS provides a layer of abstraction between users and network infrastructure.

Instead of memorizing:

```text
104.26.10.229
172.217.168.46
140.82.121.4
```

Users only need to remember:

```text
tryhackme.com
google.com
github.com
```

This significantly improves usability and accessibility across the Internet.

---

## Benefits of DNS

### User-Friendly Access

Allows users to access websites using names rather than numbers.

### Faster Navigation

Makes locating and visiting websites more convenient.

### Simplified Communication

Provides an easy method for devices and services to be located on the Internet.

### Essential Internet Service

Acts as one of the foundational technologies that enable modern web browsing.

---

## Example Mapping

| Domain Name   | IP Address    |
| ------------- | ------------- |
| tryhackme.com | 104.26.10.229 |

---

## Key Notes

* DNS stands for **Domain Name System**.
* DNS translates domain names into IP addresses.
* Every device on the Internet has a unique IP address.
* Domain names are easier for humans to remember than IP addresses.
* Browsers rely on DNS to locate websites.
* DNS acts as the Internet's directory service.
* DNS makes web browsing simple and user-friendly.

---

## Learning Outcome

After completing this section, I understood how DNS enables communication across the Internet by translating domain names into IP addresses. I learned the relationship between domain names and IP addresses, how DNS resolution works, and why DNS is one of the most important services that makes modern Internet usage practical and accessible.
