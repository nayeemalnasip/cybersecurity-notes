# DNS in Detail

## DNS Record Types

### Overview

DNS does much more than simply translate domain names into IP addresses. It uses different types of DNS records to store and provide specific information about domains, services, email servers, and other resources.

Each DNS record serves a unique purpose and helps devices locate the correct destination or service.

---

## A Record

### What is an A Record?

An **A (Address) Record** maps a domain name to an **IPv4 address**.

When a user visits a website, DNS can use an A Record to identify the server's IPv4 address.

### Example

```text
tryhackme.com → 104.26.10.229
```

### Purpose

* Resolves domain names to IPv4 addresses.
* Used by web browsers to locate web servers.
* One of the most common DNS record types.

---

## AAAA Record

### What is an AAAA Record?

An **AAAA Record** functions similarly to an A Record but resolves a domain name to an **IPv6 address**.

### Example

```text
tryhackme.com → 2606:4700:20::681a:be5
```

### Purpose

* Resolves domain names to IPv6 addresses.
* Supports modern IP addressing standards.
* Helps overcome IPv4 address limitations.

---

## CNAME Record

### What is a CNAME Record?

A **CNAME (Canonical Name) Record** maps one domain name to another domain name rather than directly to an IP address.

### Example

```text
store.tryhackme.com
        ↓
shops.shopify.com
```

DNS must then perform another lookup for:

```text
shops.shopify.com
```

to determine the final IP address.

### Purpose

* Creates aliases for domains.
* Simplifies domain management.
* Allows services to point to external providers.

---

## MX Record

### What is an MX Record?

An **MX (Mail Exchange) Record** identifies the mail servers responsible for handling email for a domain.

### Example

```text
tryhackme.com
        ↓
alt1.aspmx.l.google.com
```

### Priority Values

MX records include a priority number that determines the order in which mail servers should be used.

Example:

```text
Priority 10 → Primary Mail Server
Priority 20 → Backup Mail Server
```

If the primary server becomes unavailable, email can automatically be delivered to a backup server.

### Purpose

* Directs email traffic.
* Supports email redundancy.
* Improves mail delivery reliability.

---

## TXT Record

### What is a TXT Record?

A **TXT (Text) Record** stores text-based information within DNS.

These records can contain any text and are commonly used for security, verification, and email authentication purposes.

---

## Common TXT Record Uses

### Domain Verification

Used by third-party services to verify ownership of a domain.

Example:

```text
@ TXT "MS=ms12345678"
```

---

### SPF (Sender Policy Framework)

Defines which mail servers are authorized to send email on behalf of a domain.

Example:

```text
@ TXT "v=spf1 ip4:192.0.2.0/24 include:_spf.google.com include:amazonses.com ~all"
```

---

### DMARC

Used to protect domains from email spoofing and phishing attacks.

Example:

```text
_dmarc.example.com TXT "v=DMARC1; p=reject;"
```

---

### ACME Challenge

Used during SSL/TLS certificate validation.

Example:

```text
_acme-challenge.example.com TXT "token_value_here"
```

---

## DNS Record Summary

| Record Type | Purpose                                             |
| ----------- | --------------------------------------------------- |
| A           | Resolves domain names to IPv4 addresses             |
| AAAA        | Resolves domain names to IPv6 addresses             |
| CNAME       | Maps one domain name to another domain name         |
| MX          | Identifies email servers for a domain               |
| TXT         | Stores text-based information and verification data |

---

## Key Notes

* DNS supports multiple record types beyond website resolution.
* A Records resolve domains to IPv4 addresses.
* AAAA Records resolve domains to IPv6 addresses.
* CNAME Records create aliases between domain names.
* MX Records identify mail servers and support email delivery.
* TXT Records store text-based information used for verification and security.
* Multiple DNS record types often work together to support a single domain.

---

## Learning Outcome

After completing this section, I understood the purpose of common DNS record types and how they support different Internet services. I learned how A and AAAA records resolve IP addresses, how CNAME records create aliases, how MX records manage email routing, and how TXT records are used for verification, authentication, and security-related configurations.
