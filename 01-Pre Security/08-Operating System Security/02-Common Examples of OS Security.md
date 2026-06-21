## Introduction to Operating System Security

### Overview

Operating System (OS) Security focuses on protecting the operating system, hardware resources, applications, and user data from unauthorized access, modification, and disruption. Since the operating system acts as the bridge between hardware and software, securing it is essential for maintaining the confidentiality, integrity, and availability of information.

---

## Operating System Fundamentals

### What is an Operating System?

An **Operating System (OS)** is system software that manages computer hardware resources and provides services for applications and users.

The OS acts as an intermediary between:

* Hardware Components
* Applications
* Users

### Operating System Architecture

| Layer            | Description                                           |
| ---------------- | ----------------------------------------------------- |
| User             | Interacts with applications                           |
| Applications     | Software programs such as browsers and messaging apps |
| Operating System | Manages hardware and software resources               |
| Hardware         | CPU, RAM, Storage, Keyboard, Monitor, etc.            |

```text
+------------------+
|      User        |
+------------------+
|   Applications   |
+------------------+
| Operating System |
+------------------+
|    Hardware      |
+------------------+
```

---

## Computer Hardware Components

### What is Hardware?

Hardware refers to the physical components of a computer that can be touched and physically connected.

### Common Hardware Components

| Component  | Function                                          |
| ---------- | ------------------------------------------------- |
| CPU        | Executes instructions and processes data          |
| RAM        | Temporary memory for running applications         |
| HDD / SSD  | Permanent storage for files and operating systems |
| Keyboard   | Input device                                      |
| Mouse      | Input device                                      |
| Monitor    | Output device                                     |
| Printer    | Output device                                     |
| USB Device | Portable storage and connectivity                 |

---

## Role of the Operating System

### How It Works

The operating system performs the following functions:

1. Controls hardware resources
2. Manages running applications
3. Handles memory allocation
4. Provides user interfaces
5. Controls file systems
6. Enforces security policies
7. Facilitates communication between software and hardware

Without an operating system:

* Applications cannot directly interact with hardware safely.
* Resource conflicts would occur.
* Users would not be able to efficiently operate computers.

---

## Types of Operating Systems

### Desktop Operating Systems

Used for personal computers and laptops.

| Operating System | Vendor                |
| ---------------- | --------------------- |
| Windows 11       | Microsoft             |
| macOS            | Apple                 |
| Linux Desktop    | Open Source Community |

---

### Mobile Operating Systems

Designed for smartphones and tablets.

| Operating System | Vendor |
| ---------------- | ------ |
| Android          | Google |
| iOS              | Apple  |

---

### Server Operating Systems

Designed for enterprise servers and data centers.

| Operating System    | Vendor                |
| ------------------- | --------------------- |
| Windows Server 2022 | Microsoft             |
| IBM AIX             | IBM                   |
| Oracle Solaris      | Oracle                |
| Linux Server        | Open Source Community |

---

## Information Security Foundations

### The CIA Triad

Operating system security is built upon three fundamental security principles:

| Principle       | Description                               |
| --------------- | ----------------------------------------- |
| Confidentiality | Protect data from unauthorized access     |
| Integrity       | Prevent unauthorized modification of data |
| Availability    | Ensure systems and data remain accessible |

---

### Confidentiality

Confidentiality ensures that only authorized users can access sensitive information.

#### Examples

* Personal photos
* Email accounts
* Banking applications
* Password databases
* Confidential business documents

#### Threats

* Unauthorized access
* Data breaches
* Password theft
* Malware infections

---

### Integrity

Integrity ensures that information remains accurate and unaltered.

#### Examples

* Financial records
* Academic documents
* System configurations
* Database entries

#### Threats

* File tampering
* Malware modifications
* Unauthorized edits
* Data corruption

---

### Availability

Availability ensures systems and services remain accessible when needed.

#### Examples

* Accessing online banking
* Opening important documents
* Using communication platforms
* Running business applications

#### Threats

* System crashes
* Hardware failures
* Malware attacks
* Ransomware infections

---

## Common Examples of Operating System Security Risks

### Authentication and Weak Passwords

#### What is Authentication?

Authentication is the process of verifying a user's identity before granting access.

### Authentication Factors

| Factor Type        | Example                       |
| ------------------ | ----------------------------- |
| Something You Know | Password, PIN                 |
| Something You Are  | Fingerprint, Face Recognition |
| Something You Have | Mobile Phone, Security Token  |

---

### Weak Password Risks

Attackers commonly exploit weak passwords to gain unauthorized access.

#### Common Weak Password Examples

```text
123456
123456789
password
abc123
password1
qwerty
qwertyuiop
iloveyou
monkey
dragon
```

### Why Weak Passwords Are Dangerous

* Easy to guess
* Vulnerable to dictionary attacks
* Vulnerable to brute-force attacks
* Often reused across multiple accounts

---

### Strong Password Characteristics

A secure password should:

* Be at least 12–16 characters long
* Include uppercase letters
* Include lowercase letters
* Include numbers
* Include special characters
* Avoid personal information
* Be unique for every account

#### Example

```text
Weak Password:
password123

Strong Password:
T7@r!Q9#Lp2$Mx8
```

---

## Weak File Permissions

### What are File Permissions?

File permissions determine who can:

* Read files
* Modify files
* Execute files

### Principle of Least Privilege

Users should receive only the permissions necessary to perform their tasks.

```text
Minimum Required Access
=
Maximum Security
```

---

### Risks of Weak File Permissions

#### Confidentiality Impact

Unauthorized users may:

* View sensitive documents
* Access confidential data
* Steal personal information

#### Integrity Impact

Unauthorized users may:

* Modify files
* Delete files
* Replace important documents

---

### Example

#### Secure Scenario

```text
HR Salary File
Access:
✓ HR Manager
✓ HR Staff

✗ General Employees
```

#### Insecure Scenario

```text
HR Salary File
Access:
✓ Everyone

Result:
Confidential data exposure
```

---

## Malicious Programs (Malware)

### What is Malware?

Malware is software intentionally designed to damage systems, steal data, or gain unauthorized access.

---

## Common Malware Types

### Trojan Horse

A Trojan disguises itself as legitimate software.

#### Capabilities

* Provides remote access
* Steals information
* Installs additional malware

#### Security Impact

| CIA Component   | Impact |
| --------------- | ------ |
| Confidentiality | High   |
| Integrity       | High   |
| Availability    | Medium |

---

### Ransomware

Ransomware encrypts user files and demands payment for decryption.

#### Attack Process

1. Malware infects system
2. Files become encrypted
3. User loses access
4. Attacker demands ransom
5. Decryption key offered after payment

```text
Original File
      ↓
Encryption
      ↓
Unreadable Data
      ↓
Ransom Demand
```

#### Security Impact

| CIA Component   | Impact   |
| --------------- | -------- |
| Confidentiality | Medium   |
| Integrity       | High     |
| Availability    | Critical |

---

## Advantages of Operating System Security

* Protects sensitive information
* Prevents unauthorized access
* Maintains data integrity
* Ensures service availability
* Reduces malware risks
* Protects personal privacy
* Supports secure business operations
* Enhances system reliability

---

## Key Characteristics

* Operating systems manage hardware and software resources.
* Security is based on the CIA Triad.
* Authentication verifies user identity.
* Weak passwords remain a major attack vector.
* File permissions enforce access control.
* Least privilege minimizes security risks.
* Malware can affect confidentiality, integrity, and availability.
* Ransomware primarily targets availability.
* Security must be implemented at the operating system level.

---

## Example

A company employee stores confidential financial reports on a laptop.

### Secure Environment

```text
Strong Password
+
Proper File Permissions
+
Updated Operating System
+
Anti-Malware Protection
=
Secure Data
```

### Insecure Environment

```text
Weak Password
+
Open File Permissions
+
Malware Infection
=
Data Breach
```

---

## Key Notes

* OS stands for Operating System.
* The OS acts as the bridge between hardware and applications.
* Security revolves around Confidentiality, Integrity, and Availability (CIA).
* Authentication verifies identity before granting access.
* Strong passwords are essential for account security.
* File permissions control access to resources.
* Least privilege reduces attack surfaces.
* Malware can compromise all security objectives.
* Ransomware encrypts files and affects availability.
* Operating system security is the foundation of overall cybersecurity.

---

## Learning Outcome

After completing this section, I understood the role of operating systems in managing hardware and software resources, the importance of the CIA Triad in information security, and how authentication, file permissions, and malware directly impact operating system security. I also learned how weak passwords, excessive permissions, and malicious programs can compromise confidentiality, integrity, and availability, making OS security a critical component of cybersecurity.
