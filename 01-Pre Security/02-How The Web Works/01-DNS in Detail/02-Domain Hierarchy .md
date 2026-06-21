# DNS in Detail

## Domain Hierarchy

### Overview

DNS uses a hierarchical structure to organize domain names across the Internet. This hierarchy helps DNS efficiently locate and manage websites by breaking domain names into different levels.

A domain name is typically composed of:

```text
Subdomain → Second-Level Domain → Top-Level Domain
```

Example:

```text
admin.tryhackme.com
```

Where:

```text
admin       = Subdomain
tryhackme   = Second-Level Domain
.com        = Top-Level Domain (TLD)
```

---

## Top-Level Domain (TLD)

### What is a TLD?

A **Top-Level Domain (TLD)** is the rightmost part of a domain name.

Example:

```text
tryhackme.com
```

In this example:

```text
.com
```

is the TLD.

---

## Types of TLDs

### Generic Top-Level Domain (gTLD)

Historically used to indicate the purpose of a website.

Examples:

| TLD  | Purpose      |
| ---- | ------------ |
| .com | Commercial   |
| .org | Organization |
| .edu | Education    |
| .gov | Government   |

Modern gTLDs include:

```text
.online
.club
.website
.biz
```

---

### Country Code Top-Level Domain (ccTLD)

Used to represent specific countries or regions.

Examples:

| TLD    | Country        |
| ------ | -------------- |
| .ca    | Canada         |
| .uk    | United Kingdom |
| .co.uk | United Kingdom |
| .bd    | Bangladesh     |

---

## Second-Level Domain (SLD)

### What is a Second-Level Domain?

The **Second-Level Domain (SLD)** is the part immediately to the left of the TLD.

Example:

```text
tryhackme.com
```

Here:

```text
tryhackme
```

is the Second-Level Domain.

---

## SLD Rules

When registering a domain name:

### Allowed Characters

```text
a-z
0-9
-
```

### Restrictions

* Maximum 63 characters.
* Cannot start with a hyphen (-).
* Cannot end with a hyphen (-).
* Cannot contain consecutive hyphens.

---

## Subdomains

### What is a Subdomain?

A subdomain appears to the left of the Second-Level Domain and is separated using a period (.).

Example:

```text
admin.tryhackme.com
```

Here:

```text
admin
```

is the subdomain.

---

## Multiple Subdomains

DNS allows multiple levels of subdomains.

Example:

```text
jupiter.servers.tryhackme.com
```

Structure:

```text
jupiter   → Subdomain
servers   → Subdomain
tryhackme → Second-Level Domain
.com      → Top-Level Domain
```

---

## Subdomain Rules

Subdomains follow the same naming rules as Second-Level Domains.

### Allowed Characters

```text
a-z
0-9
-
```

### Restrictions

* Maximum 63 characters per subdomain.
* Cannot start with a hyphen.
* Cannot end with a hyphen.
* Cannot contain consecutive hyphens.

---

## Domain Length Limit

The complete domain name can be up to:

```text
253 Characters
```

There is no practical limit to the number of subdomains that can be created, provided the total domain length remains within the allowed limit.

---

## DNS Hierarchy Example

```text
jupiter.servers.tryhackme.com
│
├── jupiter      (Subdomain)
├── servers      (Subdomain)
├── tryhackme    (Second-Level Domain)
└── .com         (Top-Level Domain)
```

---

## Key Notes

* DNS uses a hierarchical naming structure.
* TLDs are located at the far right of a domain name.
* TLDs can be Generic (gTLD) or Country Code (ccTLD).
* The Second-Level Domain identifies the main domain owner.
* Subdomains help organize services and resources within a domain.
* Multiple subdomains can exist within a single domain.
* A complete domain name can contain up to 253 characters.

---

## Learning Outcome

After completing this section, I understood how DNS organizes domain names using a hierarchical structure. I learned the roles of Top-Level Domains (TLDs), Second-Level Domains (SLDs), and Subdomains, as well as the naming rules and restrictions that govern domain creation and organization on the Internet.
