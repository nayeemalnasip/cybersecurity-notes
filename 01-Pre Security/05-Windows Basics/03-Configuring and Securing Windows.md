# Windows Basics

## Configuring and Securing Windows

### Overview

Windows provides a comprehensive set of tools for managing applications, configuring system settings, monitoring performance, and maintaining security. Understanding how to install, update, remove applications, and use built-in administrative and security tools is essential for both everyday users and cybersecurity professionals.

This section explores application management, Windows configuration tools, Task Manager, Windows Security, and Windows Defender Firewall, all of which contribute to maintaining a secure and efficient Windows environment.

---

## Main Concept

### What is Windows Configuration and Security Management?

Windows configuration and security management refers to the processes and tools used to:

* Install and manage software
* Configure operating system settings
* Monitor system resources
* Protect against malware and threats
* Control network access
* Maintain system stability

These functions help ensure that Windows remains secure, up-to-date, and optimized for daily operations.

---

## How It Works

### Step 1: Manage Applications

Users can:

* Install new software
* Update existing applications
* Remove unused programs

### Step 2: Configure System Settings

Windows provides centralized interfaces to manage:

* Devices
* User accounts
* Security
* Network settings
* Personalization

### Step 3: Monitor System Performance

Task Manager tracks:

* Running processes
* CPU usage
* Memory utilization
* Network activity

### Step 4: Apply Security Controls

Windows Security protects the system through:

* Antivirus protection
* Firewall management
* Application control
* Hardware security

### Step 5: Control Network Traffic

Windows Defender Firewall evaluates:

* Incoming traffic
* Outgoing traffic
* Application permissions
* Network profiles

```text
Applications
      ↓
Windows Configuration
      ↓
Task Manager Monitoring
      ↓
Windows Security
      ↓
Firewall Protection
```

---

## Important Components

## Application Management

### Updating Applications

Keeping software updated is critical for:

* Security patching
* Bug fixes
* Performance improvements
* Feature enhancements

---

### Windows Update

Windows includes a built-in update service called Windows Update.

#### Functions

* Updates Windows OS
* Updates security components
* Delivers patches
* Improves stability

Access Path:

```text
Settings
   ↓
Windows Update
```

---

### Application Updates

Application update methods vary depending on installation source.

| Application Type     | Update Method        |
| -------------------- | -------------------- |
| Built-in Apps        | Automatic Updates    |
| Microsoft Store Apps | Store Updates        |
| Third-Party Apps     | Vendor Update System |
| Standalone Software  | Manual Updates       |

---

## Installing Applications

### Microsoft Store

Microsoft Store provides a secure platform for obtaining applications.

Benefits:

* Verified software
* Automatic updates
* Simplified installation

---

### Installing from the Internet

Applications may also be downloaded directly from trusted vendors.

Common installer formats:

```text
.exe
.msi
```

Examples:

```text
Google Chrome Installer.exe
ZoomInstaller.exe
ApplicationSetup.msi
```

---

### Installation Process

Typical workflow:

```text
Download Installer
      ↓
Run Installer
      ↓
Accept Configuration Options
      ↓
Install Files
      ↓
Launch Application
```

---

## Uninstalling Applications

Windows supports multiple removal methods.

### Methods

#### Settings App

```text
Settings
   ↓
Apps
   ↓
Installed Apps
```

#### Control Panel

```text
Control Panel
   ↓
Programs
   ↓
Uninstall a Program
```

#### Microsoft Store

Store-installed applications can be removed directly.

#### Built-in Uninstaller

Many applications include their own uninstall utility.

---

## Windows Configuration Tools

Windows provides two major configuration interfaces.

---

### Windows Settings

The modern configuration platform.

#### Features

* User-friendly interface
* Centralized settings management
* Security controls
* Device management

---

### Common Settings Categories

| Category           | Purpose                 |
| ------------------ | ----------------------- |
| System             | Display, Audio, Storage |
| Devices            | Printers, Bluetooth     |
| Network & Internet | Connectivity Settings   |
| Personalization    | Themes and Appearance   |
| Accounts           | User Management         |
| Privacy & Security | Security Configuration  |

---

### Control Panel

The traditional Windows administration interface.

#### Functions

* Legacy system management
* Advanced configuration
* Administrative tools
* Program management

Common Sections:

```text
System and Security
Network and Internet
Hardware and Sound
Programs
User Accounts
```

---

## Task Manager

### What is Task Manager?

Task Manager is a built-in monitoring and troubleshooting utility.

It provides real-time visibility into system activity.

---

### Processes Tab

Displays:

* Running applications
* Background services
* Resource usage

Example Information:

```text
Application Name
CPU Usage
Memory Usage
Disk Usage
```

---

### Performance Tab

Provides statistics for:

* CPU
* Memory
* Disk
* Ethernet/Wi-Fi

Example Metrics:

```text
CPU Utilization
Memory Consumption
Network Activity
```

---

### Users Tab

Displays:

* Logged-in users
* Active sessions
* Resource consumption

---

### Details Tab

Provides advanced process information.

Includes:

```text
Process Name
PID
Status
User Account
```

PID = Process Identifier

---

### Services Tab

Displays Windows services.

States:

```text
Running
Stopped
```

---

### Opening Task Manager

Keyboard Shortcut:

```text
Ctrl + Shift + Esc
```

Alternative Method:

```text
Right Click Taskbar
   ↓
Task Manager
```

---

## Native Windows Security

### What is Windows Security?

Windows Security is Microsoft's centralized security management platform.

It provides protection against:

* Malware
* Unauthorized access
* Unsafe applications
* Network threats

---

### Virus & Threat Protection

Primary antivirus component.

Features:

* Real-time protection
* Threat detection
* Malware removal
* Custom scanning

---

### Scan Types

| Scan Type    | Description                |
| ------------ | -------------------------- |
| Quick Scan   | Common threat locations    |
| Full Scan    | Entire system              |
| Custom Scan  | Specific folder or file    |
| Offline Scan | Advanced malware detection |

Example:

```text
Windows Security
   ↓
Virus & Threat Protection
   ↓
Scan Options
   ↓
Custom Scan
```

---

### Firewall & Network Protection

Manages network traffic and connection security.

Functions:

* Block unauthorized access
* Monitor network traffic
* Apply security policies

---

### App & Browser Control

Protects users from:

* Malicious applications
* Unsafe downloads
* Dangerous websites

---

### Device Security

Provides hardware-level protections.

Examples:

* Secure Boot
* TPM (Trusted Platform Module)
* Hardware Isolation

---

## Windows Defender Firewall

### What is a Firewall?

A firewall is a security mechanism that monitors and controls network traffic according to predefined rules.

---

### Windows Defender Firewall Features

#### Traffic Filtering

Controls:

* Incoming traffic
* Outgoing traffic

#### Rule Management

Rules determine:

```text
Allow Connection
Block Connection
Restrict Connection
```

---

### Network Profiles

Windows Defender Firewall uses different security profiles.

| Profile | Purpose                   |
| ------- | ------------------------- |
| Domain  | Organizational networks   |
| Private | Trusted home/lab networks |
| Public  | Untrusted public networks |

---

### Firewall Rule Components

Advanced Firewall Settings display:

| Component                 | Purpose                       |
| ------------------------- | ----------------------------- |
| Inbound Rules             | Incoming traffic controls     |
| Outbound Rules            | Outgoing traffic controls     |
| Connection Security Rules | Secure communication policies |
| Monitoring                | Active firewall activity      |

---

### Example Firewall Rule

```text
Application: Web Browser
Action: Allow
Direction: Outbound
Profile: Private
```

---

## Advantages / Benefits

* Centralized application management
* Improved system stability
* Automated security updates
* Real-time performance monitoring
* Malware protection
* Network security enforcement
* Hardware-level security integration
* Simplified administration
* Enhanced system visibility
* Reduced attack surface

---

## Key Characteristics

* Windows Update keeps the operating system secure and current.
* Applications may update automatically or manually.
* Software can be installed through Microsoft Store or external installers.
* Windows Settings provides centralized configuration management.
* Control Panel supports advanced administrative tasks.
* Task Manager monitors system performance and processes.
* Windows Security offers built-in malware protection.
* Windows Defender Firewall controls network communications.
* Security tools are enabled by default in Windows.
* Multiple network profiles support different security requirements.

---

## Example

A system administrator wants to verify a newly downloaded file.

### Workflow

```text
1. Download file
2. Open Windows Security
3. Navigate to Virus & Threat Protection
4. Select Custom Scan
5. Scan target folder
6. Review scan results
7. Verify file safety
```

If a threat is detected, Windows Security can quarantine or remove the malicious file automatically.

---

## Key Notes

* Regular updates are essential for security and stability.
* Windows Update manages operating system updates.
* Common installer formats include `.exe` and `.msi`.
* Applications can be removed through Settings, Control Panel, or built-in uninstallers.
* Windows Settings is the modern management interface.
* Control Panel remains important for legacy administration.
* Task Manager provides real-time system monitoring.
* PID stands for Process Identifier.
* Windows Security acts as the central protection dashboard.
* Windows Defender Firewall controls network access using security rules and profiles.

---

## Learning Outcome

After completing this section, I understood how Windows manages application installation, updating, and removal. I learned how to configure operating system settings using both Windows Settings and Control Panel, monitor system performance using Task Manager, and utilize Windows Security features such as Virus & Threat Protection, App & Browser Control, Device Security, and Windows Defender Firewall. I also gained practical knowledge of security scanning, firewall profiles, and system monitoring, which are fundamental skills for Windows administration and cybersecurity operations.
