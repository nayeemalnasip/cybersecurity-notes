# Windows CLI Basics

## Gathering System Information on Windows

### Overview

Before troubleshooting a system, investigating security incidents, or performing administrative tasks, IT and cybersecurity professionals first gather information about the environment they are working in. System information helps identify the current user, computer name, operating system version, hardware architecture, and network configuration.

Windows provides several built-in Command Prompt utilities that allow administrators and security analysts to quickly collect this information without using graphical tools. Understanding these commands is a fundamental skill for system administration, incident response, and cybersecurity investigations.

---

## Main Concept

### What is System Information Gathering?

System information gathering is the process of collecting details about a computer's operating system, user accounts, hardware, and network configuration.

This process helps administrators and security professionals:

* Identify system ownership
* Verify user permissions
* Determine operating system versions
* Understand network connectivity
* Troubleshoot issues
* Support incident investigations
* Document system environments

---

## How It Works

### Step 1: Identify Current User

Determine which account is currently logged into the system.

```cmd
whoami
```

---

### Step 2: Identify Computer Name

Display the hostname of the machine.

```cmd
hostname
```

---

### Step 3: Retrieve Operating System Information

Collect detailed operating system and hardware information.

```cmd
systeminfo
```

---

### Step 4: Check Network Configuration

Display network adapter information and IP settings.

```cmd
ipconfig
```

---

### Step 5: Analyze Collected Information

Review:

* Current user
* Hostname
* OS version
* System architecture
* IP address
* Default gateway

These details provide a basic profile of the machine.

---

## Important Components

## User Identification

### whoami Command

The `whoami` command displays the username of the currently logged-in account.

Syntax:

```cmd
whoami
```

Example:

```cmd
C:\Users\Administrator> whoami
```

Output:

```text
administrator
```

---

### Why It Matters

Cybersecurity professionals use this command to:

* Verify account permissions
* Confirm active user sessions
* Identify privilege levels
* Troubleshoot access issues

---

## Computer Identification

### hostname Command

The `hostname` command displays the computer's name.

Syntax:

```cmd
hostname
```

Example:

```cmd
C:\Users\Administrator> hostname
```

Output:

```text
WIN-SERVER01
```

---

### Why Hostnames Matter

Hostnames help:

* Identify systems on a network
* Manage enterprise environments
* Track devices during investigations
* Locate systems in security logs

---

## Operating System Information

### systeminfo Command

The `systeminfo` command provides detailed information about the operating system, hardware, and configuration.

Syntax:

```cmd
systeminfo
```

---

### Example Output

```text
Host Name:                 WIN-SERVER01
OS Name:                   Microsoft Windows Server 2019
OS Version:                10.0.17763
System Type:               x64-based PC
```

---

### Important Fields

| Field                 | Description               |
| --------------------- | ------------------------- |
| Host Name             | Computer name             |
| OS Name               | Windows edition           |
| OS Version            | Installed version/build   |
| System Type           | Hardware architecture     |
| Total Physical Memory | Installed RAM             |
| Domain                | Network domain membership |
| Boot Time             | Last system startup       |

---

### System Architecture

Common values:

```text
x64-based PC
```

Meaning:

```text
64-bit Operating System
```

Older systems may display:

```text
x86-based PC
```

Meaning:

```text
32-bit Operating System
```

---

## Network Information

### ipconfig Command

Displays network adapter configuration and IP settings.

Syntax:

```cmd
ipconfig
```

---

### Example Output

```text
Ethernet adapter Ethernet:

IPv4 Address . . . . . : 10.10.10.25
Subnet Mask . . . . . : 255.255.255.0
Default Gateway . . . : 10.10.10.1
```

---

### Key Fields

| Field           | Description                            |
| --------------- | -------------------------------------- |
| IPv4 Address    | Device IP address                      |
| Subnet Mask     | Defines network size                   |
| Default Gateway | Router used to reach external networks |
| DNS Server      | Resolves domain names to IP addresses  |

---

## IPv4 Address

Example:

```text
192.168.1.50
```

Purpose:

* Identifies the device on a network
* Enables communication between systems

---

## Default Gateway

Example:

```text
192.168.1.1
```

Purpose:

* Acts as the network's router
* Sends traffic outside the local network
* Provides internet connectivity

---

## Information Gathering Workflow

```text
Open Command Prompt
          ↓
Check Current User
          ↓
Identify Hostname
          ↓
Collect OS Information
          ↓
Review System Architecture
          ↓
Check Network Configuration
          ↓
Document Findings
```

---

## Advantages / Benefits

* Quickly identifies system details
* Assists with troubleshooting
* Helps verify user permissions
* Supports incident response activities
* Provides network visibility
* Useful for inventory management
* Enables faster system diagnostics
* Requires no additional software

---

## Key Characteristics

* Uses built-in Windows commands.
* Requires minimal system resources.
* Works on most Windows versions.
* Provides real-time system information.
* Supports security investigations.
* Useful in both local and remote administration.
* Frequently used by IT support teams.
* Essential during system audits.

---

## Example

A cybersecurity analyst receives an alert from a workstation.

### Verify Current User

```cmd
whoami
```

Output:

```text
administrator
```

---

### Check Computer Name

```cmd
hostname
```

Output:

```text
CORP-WKS-07
```

---

### Gather Operating System Information

```cmd
systeminfo
```

Relevant Output:

```text
OS Name: Microsoft Windows Server 2019
OS Version: 10.0.17763
System Type: x64-based PC
```

---

### Review Network Information

```cmd
ipconfig
```

Relevant Output:

```text
IPv4 Address : 10.10.10.25
Default Gateway : 10.10.10.1
```

---

### Investigation Result

The analyst successfully identifies:

* Logged-in user
* Computer hostname
* Windows version
* System architecture
* Network configuration

These details provide a baseline understanding of the system before deeper analysis begins.

---

## Key Notes

| Command      | Purpose                           |
| ------------ | --------------------------------- |
| `whoami`     | Display current username          |
| `hostname`   | Display computer name             |
| `systeminfo` | View operating system information |
| `ipconfig`   | View network configuration        |

---

### Important Information Collected

```text
Username
Hostname
Operating System
OS Version
System Type
IPv4 Address
Default Gateway
```

---

### Common Cybersecurity Uses

```text
Incident Response
System Auditing
Asset Identification
Network Troubleshooting
Security Investigations
Access Verification
```

---

## Learning Outcome

After completing this section, I learned how to gather essential system information using Windows Command Prompt. I practiced identifying the currently logged-in user, determining the computer hostname, reviewing operating system details and system architecture, and examining network configuration information such as IPv4 addresses and default gateways. These foundational skills are widely used in IT support, system administration, cybersecurity investigations, incident response, and troubleshooting activities across Windows environments.
