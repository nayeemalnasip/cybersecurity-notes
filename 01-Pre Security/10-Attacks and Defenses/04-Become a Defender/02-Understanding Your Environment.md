# Defensive Security Fundamentals

## Understanding Your Environment

### Overview

Before defenders can effectively secure an organization, they must first understand what assets exist, how they are connected, and which systems are most critical to business operations. This process is known as **environment awareness** or **asset visibility**.

Just as city guards need a map of the city they protect, cybersecurity defenders require visibility into networks, systems, users, applications, and infrastructure to detect threats, respond to incidents, and maintain security.

---

## Main Concept

### What is Environment Visibility?

Environment visibility is the ability to identify, monitor, and understand all assets, systems, users, and network activity within an organization's infrastructure.

Without visibility, defenders cannot effectively:

* Protect assets
* Detect attacks
* Investigate incidents
* Respond to threats

### Core Principle

```text
Know What Exists
↓
Monitor Activity
↓
Detect Threats
↓
Protect Assets
```

---

## How It Works

### Step 1: Identify Assets

Determine what systems and resources belong to the organization.

Examples:

```text
Employee Devices
Servers
Databases
Applications
Network Devices
Cloud Resources
```

---

### Step 2: Understand Relationships

Determine how systems communicate and depend on one another.

Example:

```text
Employee Device
↓
Web Application
↓
Database Server
```

---

### Step 3: Establish Visibility

Collect information from various monitoring sources.

Examples:

```text
System Logs
Network Traffic
Security Alerts
User Activity
```

---

### Step 4: Monitor Activity

Observe normal and abnormal behavior.

Examples:

```text
Successful Logins
Failed Logins
File Access
Network Connections
```

---

### Step 5: Detect and Respond

Identify suspicious activity and take action when necessary.

---

## Important Components

### The City Analogy

Defensive security can be understood using a city model.

| Defensive Security Concept | City Analogy        | Security Equivalent              |
| -------------------------- | ------------------- | -------------------------------- |
| Assets                     | Homes and Buildings | Servers, Devices, Users          |
| Visibility                 | Cameras and Patrols | Logs, Monitoring, Alerts         |
| Suspicious Activity        | Break-in Attempts   | Failed Logins, Malicious Traffic |
| Protection                 | Police and Gates    | Firewalls, Security Controls     |

---

## What Defenders Do

### Prevention

Prevent attacks before they occur.

#### Examples

* Firewalls
* Antivirus Software
* Multi-Factor Authentication (MFA)
* Security Patching

#### Process

```text
Threat
↓
Security Control
↓
Attack Prevented
```

---

### Detection

Identify suspicious or malicious activity.

#### Sources

```text
Logs
Alerts
Network Monitoring
Security Tools
```

#### Examples

* Multiple Failed Logins
* Malware Detection
* Unusual Network Traffic

---

### Mitigation

Reduce the impact of an active security incident.

#### Examples

```text
Block Malicious IP Address
Disable Compromised Account
Isolate Infected Device
```

---

### Analysis

Investigate what happened and determine the impact.

#### Questions

```text
How did the attack occur?
Which systems were affected?
What data was accessed?
```

#### Sources

* Log Files
* Security Alerts
* Network Traffic
* Endpoint Data

---

### Response and Improvement

Restore operations and strengthen defenses.

#### Activities

```text
Recover Systems
Patch Vulnerabilities
Improve Monitoring
Update Security Policies
```

---

## Understanding Scope

### What is Scope?

Scope defines which systems, networks, devices, and services defenders are responsible for protecting.

Defenders focus on organizational assets rather than the entire internet.

---

### Typical Scope Components

#### Employee Devices

Used by staff to perform daily work.

Examples:

```text
Laptops
Desktops
Mobile Devices
```

#### City Analogy

```text
Homes
```

---

#### Web Server

Hosts websites and web applications.

Examples:

```text
Corporate Website
Customer Portal
Online Store
```

#### City Analogy

```text
Shops and Public Buildings
```

---

#### Mail Server

Handles organizational email communication.

Examples:

```text
Email Delivery
Email Storage
Communication Services
```

#### City Analogy

```text
Post Office
```

---

#### Firewall

Controls network traffic entering and leaving the environment.

Functions:

```text
Allow Traffic
Block Traffic
Enforce Security Policies
```

#### City Analogy

```text
City Gate
```

---

#### Internet

External networks outside organizational control.

Examples:

```text
Public Websites
Third-Party Networks
External Users
```

#### City Analogy

```text
Outside the City
```

---

## Infrastructure Mapping

### Example Environment

```text
Internet
    │
    ▼
Firewall
    │
 ┌──┴──┐
 │     │
 ▼     ▼
Mail   Web Server
Server
 │
 ▼
Employee Devices
```

---

## Advantages / Benefits

### Improved Visibility

Provides awareness of organizational assets.

### Faster Threat Detection

Enables identification of suspicious activity.

### Better Incident Response

Helps defenders understand affected systems.

### Reduced Risk

Allows proactive protection of critical assets.

### Stronger Security Posture

Improves overall organizational defense capabilities.

---

## Key Characteristics

* Visibility is fundamental to defensive security.
* Organizations must know what assets exist.
* Monitoring helps identify suspicious activity.
* Prevention reduces attack opportunities.
* Detection identifies threats that bypass defenses.
* Mitigation limits damage during incidents.
* Analysis determines attack causes and impact.
* Response restores systems and improves security.
* Scope defines what defenders protect.
* Infrastructure mapping improves situational awareness.

---

## Example

### Protecting a Business Environment

A company operates:

```text
Employee Devices
Mail Server
Web Server
Firewall
```

Defenders monitor:

```text
System Logs
Network Traffic
Authentication Events
Security Alerts
```

When suspicious login attempts occur:

```text
Detection
↓
Investigation
↓
IP Blocked
↓
Threat Mitigated
```

The organization maintains security and business continuity.

---

## Key Notes

* Defensive security begins with understanding the environment.
* Visibility is essential for effective monitoring.
* Assets must be identified and mapped.
* Prevention stops attacks before they occur.
* Detection identifies suspicious activity.
* Mitigation reduces incident impact.
* Analysis investigates attack details.
* Response restores operations and strengthens defenses.
* Firewalls control network access.
* Infrastructure awareness improves security effectiveness.

---

## Learning Outcome

After completing this section, I understood the importance of environment visibility in defensive security and why defenders must first identify and understand the systems they are responsible for protecting. I learned how prevention, detection, mitigation, analysis, and response work together to secure an organization, how common infrastructure components such as employee devices, web servers, mail servers, and firewalls fit into a network environment, and how asset visibility and infrastructure mapping help defenders detect threats and respond effectively to security incidents.
