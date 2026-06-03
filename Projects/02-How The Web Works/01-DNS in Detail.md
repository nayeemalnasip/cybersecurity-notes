# DNS in Detail - Project Summary

## Project Overview

This project focused on understanding the Domain Name System (DNS), the technology responsible for translating human-readable domain names into IP addresses. Throughout the room, I explored how DNS is structured, how domain hierarchies work, different DNS record types, and how DNS requests are processed across the Internet.

---

## Task Completion Process

### Understanding DNS Fundamentals

The first stage of the project focused on understanding the purpose of DNS and why it is critical for Internet communication.

I learned that DNS acts as the Internet's phonebook by converting domain names into IP addresses. Instead of remembering complex numerical addresses, users can access websites using easy-to-remember domain names.

**Outcome:**

* Understood the purpose of DNS.
* Learned how domain names are translated into IP addresses.
* Explored the role of DNS in everyday Internet usage.

---

### Exploring Domain Hierarchy

The next task focused on how domain names are structured and organized within the DNS hierarchy.

I studied:

* Top-Level Domains (TLDs)
* Country Code Top-Level Domains (ccTLDs)
* Second-Level Domains
* Subdomains

I learned the limitations and naming rules associated with domains and subdomains, including character restrictions and maximum lengths.

**Outcome:**

* Understood DNS hierarchical structure.
* Learned the difference between TLDs, ccTLDs, and subdomains.
* Explored domain naming standards and restrictions.

---

### Understanding DNS Record Types

In this task, I explored the various DNS records used to provide different services across a domain.

I studied:

* A Records (IPv4)
* AAAA Records (IPv6)
* CNAME Records
* MX Records
* TXT Records

I learned how each record serves a specific purpose in directing web traffic, handling email delivery, and verifying domain ownership.

**Outcome:**

* Understood common DNS record types.
* Learned how email routing works through MX records.
* Explored domain verification and security-related TXT records.
* Studied IPv4 and IPv6 DNS resolution.

---

### Learning the DNS Resolution Process

This task focused on understanding how a DNS query travels across the Internet.

I examined the complete DNS lookup path:

```text
Client → Recursive DNS Server → Root Server →
TLD Server → Authoritative DNS Server → Response
```

I also learned how DNS caching improves performance and how TTL values determine how long records remain cached.

**Outcome:**

* Understood recursive and authoritative DNS servers.
* Learned how DNS requests are resolved step-by-step.
* Explored DNS caching and TTL functionality.

---

### Practical DNS Enumeration Activities

The final practical exercise involved interacting with DNS records and retrieving information from a simulated environment.

During this activity, I successfully identified:

**CNAME Record**

```text
shops.myshopify.com
```

**TXT Record**

```text
THM{7012BBA60997F35A9516C2E16D2944FF}
```

**MX Record Priority**

```text
30
```

**A Record Address**

```text
10.10.10.10
```

This practical exercise provided hands-on experience with DNS enumeration and record analysis.

**Outcome:**

* Identified DNS records in a practical environment.
* Performed DNS enumeration techniques.
* Retrieved domain configuration information successfully.

---

## Skills Demonstrated

* DNS Fundamentals
* Domain Hierarchy Analysis
* TLD and ccTLD Identification
* Subdomain Enumeration Concepts
* DNS Record Analysis
* A Record Investigation
* AAAA Record Investigation
* MX Record Analysis
* TXT Record Analysis
* CNAME Resolution
* Recursive DNS Understanding
* Authoritative DNS Understanding
* DNS Caching Concepts
* TTL Analysis
* DNS Enumeration

---

## Project Conclusion

By completing this room, I developed a strong understanding of how DNS powers communication across the Internet. I learned how domain names are structured, how DNS records support various services, and how DNS requests are resolved through recursive and authoritative servers. The practical exercises strengthened my ability to analyze DNS infrastructure and perform basic DNS enumeration, which are essential skills in networking, system administration, and cybersecurity.
