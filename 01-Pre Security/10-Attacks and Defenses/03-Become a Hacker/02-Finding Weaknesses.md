# Offensive Security Fundamentals

## Finding Weaknesses and Web Content Discovery

### Overview

One of the first activities performed during an offensive security assessment is identifying publicly accessible resources that may expose sensitive information or functionality. Attackers and penetration testers often search for hidden directories, files, login portals, administrative panels, and forgotten web pages that developers may have unintentionally left accessible.

This process is commonly known as **Content Discovery** or **Directory Enumeration** and is an important phase of reconnaissance and vulnerability assessment.

---

## Main Concept

### What is Content Discovery?

Content Discovery is the process of identifying hidden or undisclosed files, directories, pages, and resources hosted on a web server.

These resources may not be linked from the main website but can still be accessible if the correct URL is known.

### Purpose

```text
Identify Hidden Resources
↓
Analyze Exposure
↓
Discover Vulnerabilities
↓
Improve Security
```

---

## How It Works

### Step 1: Identify the Target

The tester receives authorization to assess a website.

Example:

```text
http://www.onlineshop.thm/
```

---

### Step 2: Test Common Paths

A tester manually checks commonly used pages.

Examples:

```text
/sitemap
/mail
/register
/login
/admin
```

---

### Step 3: Analyze Responses

Possible responses include:

| HTTP Status   | Meaning                 |
| ------------- | ----------------------- |
| 200 OK        | Resource Exists         |
| 301/302       | Redirect                |
| 403 Forbidden | Access Denied           |
| 404 Not Found | Resource Does Not Exist |

Example:

```text
/admin → 200 OK
```

This indicates that the page exists.

---

### Step 4: Identify Hidden Resources

Discovered pages may reveal:

* Login Portals
* Administrative Dashboards
* Development Pages
* Backup Files
* Internal Applications

---

### Step 5: Assess Security Impact

Determine whether the discovered resources create a security risk.

Example:

```text
Public Admin Panel
↓
Potential Unauthorized Access
```

---

## Important Components

### Red Teaming

A realistic attack simulation performed against an organization.

#### Purpose

* Test defenses
* Assess detection capabilities
* Measure incident response effectiveness

---

### Penetration Testing

An authorized security assessment designed to identify vulnerabilities.

#### Objectives

* Discover weaknesses
* Demonstrate impact
* Provide remediation guidance

---

### Vulnerability

A flaw or weakness that may be exploited.

Examples:

| Type           | Example               |
| -------------- | --------------------- |
| Authentication | Weak Password         |
| Configuration  | Public Admin Page     |
| Software       | Unpatched Application |
| Access Control | Excessive Permissions |

---

### Exploit

A method used to take advantage of a vulnerability.

Example:

```text
Vulnerability
↓
Exploit
↓
Unauthorized Access
```

---

### Scope

The defined boundaries of an assessment.

Examples:

```text
Allowed:
www.example.com

Not Allowed:
mail.example.com
vpn.example.com
```

Testing must remain within the approved scope.

---

## Manual Content Discovery

### URL Enumeration

A tester manually attempts to access common pages.

Examples:

```text
http://www.onlineshop.thm/login
http://www.onlineshop.thm/register
http://www.onlineshop.thm/admin
```

### Benefits

* Simple
* Fast for small targets
* Useful during initial reconnaissance

### Limitation

Inefficient when thousands of potential directories exist.

---

## Automated Content Discovery

### Gobuster

Gobuster is a command-line tool used to discover hidden directories and files on web servers.

#### Purpose

* Directory Enumeration
* File Discovery
* Virtual Host Discovery

---

### Gobuster Command

```bash
gobuster dir --url http://www.onlineshop.thm/ -w /usr/share/wordlists/dirbuster/directory-list.txt
```

---

### Command Breakdown

| Parameter | Description                |
| --------- | -------------------------- |
| gobuster  | Launches the Gobuster tool |
| dir       | Directory enumeration mode |
| --url     | Specifies the target URL   |
| -w        | Specifies the wordlist     |

---

### Example Structure

```bash
gobuster dir \
--url http://target-website.com \
-w wordlist.txt
```

---

## Wordlists

### What is a Wordlist?

A wordlist is a collection of common filenames and directory names used during content discovery.

Example Entries:

```text
admin
login
dashboard
backup
config
uploads
```

Gobuster systematically tests each entry against the target website.

---

## Directory Enumeration Process

```text
Wordlist
↓
Generate Requests
↓
Send Requests to Web Server
↓
Analyze Responses
↓
Identify Existing Resources
```

---

## Commonly Discovered Resources

### Authentication Pages

```text
/login
/register
/signin
```

### Administrative Pages

```text
/admin
/admin-panel
/dashboard
```

### Development Resources

```text
/dev
/test
/staging
```

### Backup Files

```text
backup.zip
database.sql
config.bak
```

---

## Advantages / Benefits

### Identifies Hidden Resources

Finds pages not linked from the website.

### Improves Security Visibility

Reveals exposed functionality.

### Supports Vulnerability Discovery

Helps identify attack surfaces.

### Automates Enumeration

Reduces manual effort.

### Accelerates Reconnaissance

Quickly maps accessible resources.

---

## Key Characteristics

* Content discovery is part of reconnaissance.
* Hidden pages may still be publicly accessible.
* Manual enumeration works for small targets.
* Automated tools improve efficiency.
* Gobuster is a common directory enumeration tool.
* Wordlists drive automated discovery.
* HTTP response codes help identify valid resources.
* Ethical testing requires authorization and defined scope.

---

## Example

### Online Shop Assessment

A penetration tester is authorized to assess:

```text
http://www.onlineshop.thm
```

#### Manual Testing

Checks:

```text
/login
/register
/admin
```

Finds:

```text
/admin
```

---

#### Automated Testing

Runs:

```bash
gobuster dir --url http://www.onlineshop.thm/ -w /usr/share/wordlists/dirbuster/directory-list.txt
```

Finds:

```text
/admin
/dashboard
/uploads
```

---

#### Result

```text
Hidden Resources Identified
↓
Potential Security Risks Evaluated
↓
Recommendations Provided
```

---

## Key Notes

* Offensive Security focuses on proactively finding weaknesses.
* Permission and scope are mandatory requirements.
* Content Discovery identifies hidden web resources.
* Manual URL testing is useful for small assessments.
* Gobuster automates directory enumeration.
* Wordlists contain common directory and file names.
* HTTP status codes indicate resource availability.
* Hidden pages may expose sensitive functionality.
* Directory enumeration is a common reconnaissance technique.
* Findings should be documented and remediated.

---

## Learning Outcome

After completing this section, I understood how offensive security professionals identify hidden web resources through content discovery and directory enumeration. I learned the importance of scope and authorization during assessments, the difference between vulnerabilities and exploits, how tools such as Gobuster automate the discovery of hidden directories and files, and how exposed resources can increase an organization's attack surface and security risk.
