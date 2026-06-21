# Linux CLI Basics

## System Information Gathering and Linux Environment Investigation

### Overview

System information gathering is one of the first tasks performed by system administrators, cybersecurity analysts, and incident responders when accessing a Linux machine. Understanding the operating system, kernel version, storage capacity, user context, and distribution details helps professionals assess the environment, identify potential issues, and prepare for troubleshooting or security investigations.

In this section, you will learn how to collect essential system information using built-in Linux commands and how to investigate operating system details through configuration files stored within the Linux filesystem.

---

## Main Concept

### What is System Information Gathering?

System information gathering is the process of collecting details about a computer system, including:

* Current user information
* Operating system details
* Kernel version
* Hardware architecture
* Disk usage
* Linux distribution information

These details provide a snapshot of the system's configuration and operating environment.

Cybersecurity professionals use this information during:

* Incident response
* System administration
* Vulnerability assessments
* Security audits
* Digital forensics
* Penetration testing

---

## How It Works

### Step 1: Identify the Current User

Determine which account is currently logged in.

```bash
whoami
```

---

### Step 2: Gather Operating System Information

Display kernel and system details.

```bash
uname -a
```

---

### Step 3: Check Disk Usage

Review available storage and filesystem usage.

```bash
df -h
```

---

### Step 4: Navigate to System Configuration Directory

Move to the Linux configuration directory.

```bash
cd /etc
```

---

### Step 5: Read Operating System Information

View Linux distribution details.

```bash
cat os-release
```

---

### Step 6: Locate and Review Required Files

Use:

```bash
find
```

to locate files and:

```bash
cat
```

to read their contents.

---

## Important Components

## User Identification

### whoami Command

The `whoami` command displays the username of the currently logged-in user.

Syntax:

```bash
whoami
```

Example:

```bash
ubuntu@tryhackme:~$ whoami
ubuntu
```

Output:

```text
ubuntu
```

---

### Why It Matters

Cybersecurity professionals use this command to:

* Verify current privileges
* Confirm active accounts
* Identify execution context
* Troubleshoot permission issues

---

## Operating System Information

### uname Command

The `uname` command displays system information.

Basic Syntax:

```bash
uname
```

Example:

```bash
uname
```

Output:

```text
Linux
```

---

### uname -a Command

Displays comprehensive system details.

Syntax:

```bash
uname -a
```

Example:

```text
Linux tryhackme 6.x.x-aws x86_64 GNU/Linux
```

---

### Information Returned

| Component      | Description           |
| -------------- | --------------------- |
| Linux          | Kernel Type           |
| Hostname       | System Name           |
| Kernel Version | Installed Kernel      |
| Architecture   | CPU Architecture      |
| GNU/Linux      | Operating System Type |

---

### Kernel

#### What is a Kernel?

The kernel is the core component of the operating system.

Responsibilities:

* Hardware communication
* Process management
* Memory management
* Device management
* Security enforcement

Architecture Example:

```text
x86_64
```

Meaning:

```text
64-bit Operating System
```

---

## Disk and Storage Information

### df Command

The `df` command displays filesystem disk usage.

Syntax:

```bash
df
```

---

### Human Readable Output

Syntax:

```bash
df -h
```

Example:

```text
Filesystem      Size Used Avail Use%
/dev/root        20G  12G   8G   60%
```

---

### Understanding df Output

| Column     | Meaning         |
| ---------- | --------------- |
| Filesystem | Storage Device  |
| Size       | Total Capacity  |
| Used       | Consumed Space  |
| Avail      | Available Space |
| Use%       | Percentage Used |
| Mounted on | Mount Location  |

---

### Common Filesystems

#### Root Filesystem

```text
/dev/root
```

Main operating system storage.

---

#### tmpfs

```text
tmpfs
```

Temporary memory-based filesystem.

Characteristics:

* Stored in RAM
* Fast access
* Temporary storage
* Cleared on reboot

Examples:

```text
/dev/shm
/run
/run/user
```

---

## Linux Configuration Directory

### /etc Directory

The `/etc` directory stores:

* System configuration files
* Service settings
* User configuration data
* Distribution information

Navigation:

```bash
cd /etc
```

---

### Listing Contents

```bash
ls
```

Example Files:

```text
fstab
hosts
resolv.conf
os-release
systemd
```

---

## Operating System Release Information

### os-release File

The `os-release` file contains Linux distribution information.

Location:

```text
/etc/os-release
```

---

### Reading the File

```bash
cat /etc/os-release
```

Example:

```text
PRETTY_NAME="Ubuntu 24.04.1 LTS"
NAME="Ubuntu"
VERSION_ID="24.04"
VERSION_CODENAME=noble
```

---

### Important Fields

| Field            | Description                |
| ---------------- | -------------------------- |
| PRETTY_NAME      | Full Distribution Name     |
| NAME             | Distribution Name          |
| VERSION_ID       | Distribution Version       |
| VERSION_CODENAME | Release Codename           |
| ID               | Distribution Identifier    |
| ID_LIKE          | Parent Distribution Family |

---

### Example Distribution Information

```text
Ubuntu 24.04.1 LTS
```

Codename:

```text
Noble Numbat
```

---

## File Searching and Investigation

### find Command

Searches for files and directories.

Syntax:

```bash
find <location> -name <filename>
```

Example:

```bash
find ~ -name day1_report.txt
```

---

### Investigation Workflow

```text
Search File
     ↓
Locate Path
     ↓
Navigate Directory
     ↓
Read Contents
     ↓
Collect Information
```

---

## Reading Files

### cat Command

Displays file contents directly in the terminal.

Syntax:

```bash
cat filename
```

Example:

```bash
cat day1_report.txt
```

---

### Common Uses

* View reports
* Read logs
* Inspect configuration files
* Review scripts

Examples:

```bash
cat os-release
cat report.txt
cat notes.txt
```

---

## Advantages / Benefits

* Quickly identifies system configuration
* Verifies operating environment
* Assists troubleshooting
* Supports security investigations
* Helps detect unsupported systems
* Provides storage visibility
* Confirms user permissions
* Enables efficient incident response
* Works on remote systems
* Requires minimal resources

---

## Key Characteristics

* `whoami` identifies the current user.
* `uname -a` displays detailed system information.
* `df -h` shows human-readable disk usage.
* Linux stores system configuration files in `/etc`.
* `os-release` contains distribution information.
* `find` locates files within the filesystem.
* `cat` displays file contents.
* `tmpfs` filesystems are stored in memory.
* The kernel manages hardware and system resources.
* System information gathering is a critical cybersecurity skill.

---

## Example

A cybersecurity analyst receives access to a Linux server and needs to determine the environment.

### Identify Current User

```bash
whoami
```

Output:

```text
ubuntu
```

### View Kernel Information

```bash
uname -a
```

Output:

```text
Linux tryhackme x86_64 GNU/Linux
```

### Check Available Storage

```bash
df -h
```

Output:

```text
Filesystem      Size Used Avail Use%
/dev/root        20G  12G   8G   60%
```

### Determine Linux Distribution

```bash
cat /etc/os-release
```

Output:

```text
Ubuntu 24.04.1 LTS
```

The analyst now has enough information to understand the operating environment and begin further investigation.

---

## Key Notes

| Command          | Purpose                                  |
| ---------------- | ---------------------------------------- |
| `whoami`         | Display current username                 |
| `uname`          | Display operating system name            |
| `uname -a`       | Display detailed system information      |
| `df -h`          | Show disk usage in human-readable format |
| `cd /etc`        | Navigate to configuration directory      |
| `ls`             | List files and directories               |
| `cat os-release` | Display distribution information         |
| `find`           | Search for files                         |
| `cat`            | Read file contents                       |

### Important Locations

```text
/etc
/etc/os-release
/dev/root
/dev/shm
/run
```

### Important Concepts

```text
Kernel
Filesystem
Distribution
Architecture
Hostname
Storage Utilization
```

---

## Learning Outcome

After completing this section, I learned how to gather essential system information within a Linux environment using the command-line interface. I gained hands-on experience identifying the current user, examining kernel and operating system details, checking storage utilization, navigating configuration directories, and reading system files such as `/etc/os-release`. I also strengthened my file discovery and investigation skills using the `find` and `cat` commands, providing a solid foundation for Linux administration, troubleshooting, cybersecurity operations, and incident response activities.
