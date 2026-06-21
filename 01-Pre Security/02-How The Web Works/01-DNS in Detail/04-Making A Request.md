# DNS in Detail

## Making a DNS Request

### Overview

When a user enters a domain name into a browser, such as:

```text
www.tryhackme.com
```

the computer does not immediately know the server's IP address.

DNS follows a structured lookup process to translate the human-readable domain name into an IP address that computers can understand.

---

## DNS Lookup Process

### Step 1: Local Cache Check

The first place your computer checks is its local DNS cache.

If the domain has been visited recently:

```text
Domain Found → Return IP Address
```

No further DNS queries are required.

---

### Step 2: Recursive DNS Server

If the domain is not found locally, the request is sent to a:

```text
Recursive DNS Server
```

This server is usually provided by:

* ISP (Internet Service Provider)
* Public DNS Services

Examples:

* Google DNS
* Cloudflare DNS
* OpenDNS

The recursive server also checks its own cache.

---

### Step 3: Root DNS Server

If the recursive server cannot find the answer, it contacts a:

```text
Root DNS Server
```

Root servers sit at the top of the DNS hierarchy and act as the starting point of DNS resolution.

Their role is not to provide the final answer.

Instead, they direct requests to the correct:

```text
Top-Level Domain (TLD) Server
```

---

### Example

For:

```text
www.tryhackme.com
```

the root server identifies:

```text
.com
```

as the TLD and refers the request to a .com TLD server.

---

## Step 4: TLD Server

### What is a TLD Server?

A Top-Level Domain Server manages information related to a specific TLD.

Examples:

```text
.com
.org
.net
.edu
.gov
```

The TLD server does not contain the website's IP address.

Instead, it provides the location of the:

```text
Authoritative DNS Server
```

for that domain.

---

## Step 5: Authoritative DNS Server

### What is an Authoritative DNS Server?

This is the server responsible for storing the actual DNS records of a domain.

Examples of records stored:

* A Records
* AAAA Records
* CNAME Records
* MX Records
* TXT Records

For example:

```text
tryhackme.com
```

may use nameservers such as:

```text
kip.ns.cloudflare.com
uma.ns.cloudflare.com
```

These servers contain the final DNS information.

---

## Step 6: DNS Response Returned

Once the authoritative server finds the requested record:

```text
Domain → IP Address
```

the result is sent back to:

1. Recursive DNS Server
2. User's Computer

The browser can now connect to the destination server.

---

## Complete DNS Resolution Flow

```text
User Device
      │
      ▼
Local DNS Cache
      │
      ▼
Recursive DNS Server
      │
      ▼
Root DNS Server
      │
      ▼
TLD Server (.com)
      │
      ▼
Authoritative DNS Server
      │
      ▼
DNS Record Found
      │
      ▼
Recursive DNS Server
      │
      ▼
User Device
```

---

## DNS Caching

To improve performance, DNS responses are stored temporarily.

This process is known as:

```text
DNS Caching
```

Benefits:

* Faster website loading
* Reduced DNS traffic
* Lower server load
* Improved user experience

---

## TTL (Time To Live)

Every DNS record contains a value called:

```text
TTL (Time To Live)
```

TTL specifies how long a DNS record can remain cached.

Example:

```text
TTL = 3600
```

Meaning:

```text
3600 Seconds = 1 Hour
```

After the TTL expires, a new DNS lookup must be performed.

---

## Key Components Summary

| Component                | Function                                   |
| ------------------------ | ------------------------------------------ |
| Local Cache              | Stores recently resolved DNS records       |
| Recursive DNS Server     | Performs DNS lookups on behalf of users    |
| Root DNS Server          | Directs requests to the correct TLD server |
| TLD Server               | Provides Authoritative DNS Server location |
| Authoritative DNS Server | Stores actual DNS records                  |
| TTL                      | Defines cache lifetime                     |

---

## Key Notes

* DNS converts domain names into IP addresses.
* Computers first check local cache before querying external servers.
* Recursive DNS servers perform lookups for users.
* Root servers guide requests to appropriate TLD servers.
* TLD servers identify the authoritative nameserver.
* Authoritative servers contain actual DNS records.
* DNS caching improves speed and efficiency.
* TTL determines how long records remain cached.

---

## Learning Outcome

After completing this section, I understood the complete DNS resolution process from a user entering a domain name to receiving the corresponding IP address. I learned the roles of local caching, recursive DNS servers, root servers, TLD servers, authoritative DNS servers, and how TTL values improve DNS efficiency through caching.
