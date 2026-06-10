# Operating System Security

## Introduction to Operating System Security

### Overview

Operating systems (OS) are the foundation of modern computing devices, including desktops, laptops, servers, smartphones, and tablets. They act as an intermediary layer between computer hardware and software applications, enabling programs to interact with system resources efficiently and securely.

Because operating systems manage access to hardware, user data, applications, memory, storage, and network resources, they play a critical role in maintaining the security of a computing environment. Protecting an operating system is essential to safeguarding sensitive information, ensuring system reliability, and preventing unauthorized access.

---

## Main Concept

### What is Operating System Security?

Operating System Security refers to the collection of mechanisms, controls, and practices used to protect an operating system and the resources it manages from unauthorized access, misuse, modification, disruption, or destruction.

The operating system serves as the security foundation of a device by controlling:

* User authentication
* Access permissions
* File protection
* Application execution
* Hardware resource management
* Network communication

A secure operating system helps protect both the device and the data stored on it.

---

## How It Works

### Step 1: Hardware Components

A computer consists of physical components known as hardware.

Examples include:

* CPU (Central Processing Unit)
* RAM (Random Access Memory)
* Hard Disk Drive (HDD)
* Solid State Drive (SSD)
* Keyboard
* Mouse
* Monitor
* Printer
* USB Devices

Hardware alone cannot perform useful tasks without software.

---

### Step 2: Operating System Layer

The operating system sits directly above the hardware and controls access to system resources.

Functions include:

* Managing memory
* Managing storage
* Handling hardware devices
* Running applications
* Enforcing security controls

---

### Step 3: Applications Run on the OS

Applications do not interact directly with hardware.

Instead:

```text
Application
      ↓
Operating System
      ↓
Hardware
```

Examples:

* Google Chrome
* Mozilla Firefox
* Microsoft Outlook
* WhatsApp
* Telegram
* Signal

The operating system acts as a secure intermediary between applications and hardware.

---

### Step 4: Security Enforcement

The operating system enforces rules that determine:

* Who can access data
* Which applications can run
* What resources can be used
* How files are protected

These controls help prevent unauthorized activities.

---

## Important Components

## Computer Hardware

Computer hardware refers to the physical components of a computer system.

### Common Hardware Components

| Component | Function                                 |
| --------- | ---------------------------------------- |
| CPU       | Executes instructions and processes data |
| RAM       | Temporary storage for active processes   |
| HDD/SSD   | Permanent data storage                   |
| Keyboard  | User input device                        |
| Mouse     | Navigation and input device              |
| Monitor   | Displays visual output                   |
| Printer   | Produces physical documents              |

---

## Operating System (OS)

An Operating System is system software that manages hardware resources and provides services to applications.

### Core Responsibilities

* Process Management
* Memory Management
* Storage Management
* Device Management
* User Management
* Security Enforcement

---

### Examples of Operating Systems

#### Desktop Operating Systems

| Operating System | Use Case                   |
| ---------------- | -------------------------- |
| Windows 11       | Personal Computers         |
| macOS            | Apple Computers            |
| Linux            | Desktop and Server Systems |

---

#### Mobile Operating Systems

| Operating System | Use Case                |
| ---------------- | ----------------------- |
| Android          | Smartphones and Tablets |
| iOS              | Apple Mobile Devices    |

---

#### Server Operating Systems

| Operating System    | Use Case                             |
| ------------------- | ------------------------------------ |
| Windows Server 2022 | Enterprise Servers                   |
| Linux               | Web Servers and Cloud Infrastructure |
| IBM AIX             | Enterprise Computing                 |
| Oracle Solaris      | Large-Scale Business Systems         |

---

## Why Operating System Security Matters

Modern operating systems store and manage highly sensitive information.

### Examples of Sensitive Data

#### Personal Devices

* Private conversations
* Family photos
* Social media accounts
* Saved passwords
* Banking applications
* Email accounts

#### Business Devices

* Company documents
* Customer information
* Research data
* Internal communications
* Financial records
* Authentication credentials

Unauthorized access to these resources can result in data theft, privacy violations, and financial losses.

---

## The CIA Triad

The foundation of information security is based on three core principles known as the CIA Triad.

---

### Confidentiality

Ensures information is accessible only to authorized individuals.

#### Goal

Prevent unauthorized disclosure of sensitive information.

#### Examples

* Password protection
* Encryption
* Access controls
* Multi-Factor Authentication (MFA)

---

### Integrity

Ensures information remains accurate, complete, and unaltered.

#### Goal

Prevent unauthorized modification of data.

#### Examples

* File integrity monitoring
* Digital signatures
* Hash verification
* Access controls

---

### Availability

Ensures systems and information remain accessible when needed.

#### Goal

Prevent service interruptions and downtime.

#### Examples

* System backups
* Redundant servers
* Disaster recovery plans
* Load balancing

---

## CIA Triad Overview

```text
        Security
            │
 ┌──────────┼──────────┐
 │          │          │
Confidentiality Integrity Availability
```

---

## Operating System Security Functions

### Authentication

Verifies the identity of users attempting to access the system.

Examples:

* Passwords
* PINs
* Biometrics
* Smart Cards

---

### Authorization

Determines what authenticated users are allowed to do.

Examples:

* Read files
* Modify documents
* Install applications
* Access administrative tools

---

### Access Control

Restricts access to resources based on permissions.

Examples:

```text
Read
Write
Execute
Modify
Delete
```

---

### Process Isolation

Prevents applications from interfering with each other.

Benefits:

* Increased stability
* Improved security
* Reduced risk of system compromise

---

### Data Protection

Protects sensitive information stored on the system.

Methods:

* Encryption
* Backups
* File Permissions
* Secure Storage

---

## Advantages / Benefits

* Protects sensitive information
* Prevents unauthorized access
* Maintains data accuracy
* Ensures system availability
* Reduces security risks
* Supports compliance requirements
* Enhances system reliability
* Protects personal and business assets

---

## Key Characteristics

* Operating systems manage all hardware resources.
* Applications rely on the OS to access hardware.
* Security begins at the operating system layer.
* Operating systems enforce access controls.
* The CIA Triad forms the foundation of security.
* Authentication verifies user identity.
* Authorization controls user actions.
* Availability ensures uninterrupted access to services.
* Confidentiality protects sensitive information.
* Integrity prevents unauthorized data modification.

---

## Example

A user stores important banking information and personal documents on a laptop.

### Confidentiality

Only the authorized user can access the files using a password-protected account.

### Integrity

Files are protected from unauthorized modification using access permissions and integrity controls.

### Availability

The laptop remains operational and backups are available if hardware failure occurs.

As a result, the user's information remains secure, accurate, and accessible when needed.

---

## Key Notes

### Security Goals

```text
Confidentiality
Integrity
Availability
```

---

### Common Operating Systems

```text
Windows
Linux
macOS
Android
iOS
```

---

### Core OS Responsibilities

```text
Process Management
Memory Management
Storage Management
Device Management
User Management
Security Management
```

---

### Important Security Controls

```text
Authentication
Authorization
Access Control
Encryption
Backups
Process Isolation
```

---

## Learning Outcome

After completing this section, I understood the role of operating systems as the critical layer between hardware and software applications. I learned how operating systems manage system resources, control application access, and enforce security mechanisms to protect sensitive information. I also gained an understanding of the CIA Triad—Confidentiality, Integrity, and Availability—which serves as the foundation of information security and guides the protection of data and computing systems.
