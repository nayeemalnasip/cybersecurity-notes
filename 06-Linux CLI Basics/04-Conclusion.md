# Linux CLI Basics

## Linux Command-Line Fundamentals Review and Conclusion

### Overview

The Linux Command-Line Interface (CLI) is one of the most important skills for system administrators, cybersecurity analysts, penetration testers, and IT professionals. Unlike graphical interfaces, the CLI allows direct interaction with the operating system through commands, providing greater control, efficiency, and visibility into system operations.

Throughout this room, you explored the fundamentals of Linux navigation, file management, system information gathering, and terminal interaction. These foundational skills form the basis for more advanced Linux administration, cybersecurity investigations, incident response, and security tooling.

---

## Main Concept

### What Did We Learn?

This room introduced the essential concepts required to work effectively within a Linux environment using the command line.

Key learning areas included:

* Understanding the Linux terminal
* Navigating the filesystem
* Exploring files and directories
* Working with hidden files
* Searching for files
* Reading file contents
* Gathering system information
* Investigating operating system details

These skills represent the foundation of daily Linux operations and cybersecurity workflows.

---

## How Linux CLI Operations Work

### Step 1: Open a Terminal

The terminal provides access to the Linux command-line environment.

### Step 2: Navigate the Filesystem

Use navigation commands to move between directories.

### Step 3: Explore System Resources

View files, folders, and system information.

### Step 4: Locate Required Data

Search for files and directories using command-line tools.

### Step 5: Read and Analyze Information

Inspect files and configuration data.

```text
User
   ↓
Terminal
   ↓
Linux Shell
   ↓
Filesystem Navigation
   ↓
System Investigation
   ↓
Information Collection
```

---

## Important Components

## Terminal

### What is the Terminal?

The terminal is a text-based interface used to communicate directly with the Linux operating system.

Functions:

* Execute commands
* Manage files
* Run programs
* Configure systems
* Perform administrative tasks

Example Prompt:

```bash
ubuntu@tryhackme:~$
```

---

## Shell

### What is a Shell?

The shell acts as an interpreter between the user and the Linux operating system.

Responsibilities:

* Process commands
* Launch applications
* Execute scripts
* Manage processes

Common Shells:

| Shell | Description                |
| ----- | -------------------------- |
| Bash  | Most common Linux shell    |
| Zsh   | Advanced interactive shell |
| Sh    | Traditional Unix shell     |
| Fish  | User-friendly shell        |

---

## Linux Filesystem Navigation

### Current Working Directory

The current location within the filesystem.

Command:

```bash
pwd
```

Example:

```text
/home/ubuntu
```

---

### Viewing Directory Contents

Basic Listing:

```bash
ls
```

Detailed Listing:

```bash
ls -l
```

Show Hidden Files:

```bash
ls -al
```

---

### Hidden Files

Hidden files begin with a period (`.`).

Examples:

```text
.bashrc
.profile
.gitconfig
.Xauthority
```

These files commonly store:

* User preferences
* Shell settings
* Configuration information

---

## Directory Navigation

### Change Directory

Move into a directory:

```bash
cd Documents
```

Move back one level:

```bash
cd ..
```

Return to home directory:

```bash
cd ~
```

---

### Important Navigation Symbols

| Symbol | Meaning           |
| ------ | ----------------- |
| `.`    | Current Directory |
| `..`   | Parent Directory  |
| `~`    | Home Directory    |
| `/`    | Root Directory    |

---

## File Discovery

### find Command

The `find` utility searches for files and directories.

Syntax:

```bash
find <location> -name <filename>
```

Example:

```bash
find ~ -name mission_brief.txt
```

Common Cybersecurity Uses:

* Locate logs
* Find configuration files
* Search evidence during investigations
* Discover sensitive files

---

## Reading Files

### cat Command

Displays file contents directly in the terminal.

Syntax:

```bash
cat filename
```

Examples:

```bash
cat mission_brief.txt
cat day1_report.txt
cat /etc/os-release
```

---

## System Information Gathering

### Current User

Command:

```bash
whoami
```

Example Output:

```text
ubuntu
```

Purpose:

* Verify current account
* Confirm permissions
* Understand execution context

---

### Operating System Information

Basic OS Information:

```bash
uname
```

Detailed Information:

```bash
uname -a
```

Provides:

* Kernel type
* Hostname
* Kernel version
* Architecture
* Operating system information

---

### Disk Usage

Command:

```bash
df -h
```

Displays:

* Total storage
* Used space
* Available space
* Usage percentage

Example:

```text
Filesystem      Size Used Avail Use%
/dev/root        20G  12G   8G   60%
```

---

## Linux Configuration Files

### /etc Directory

The primary Linux configuration directory.

Location:

```bash
/etc
```

Contains:

* System settings
* Service configurations
* User configuration files
* Distribution information

Examples:

```text
fstab
hosts
resolv.conf
os-release
```

---

### os-release File

Provides Linux distribution information.

Location:

```bash
/etc/os-release
```

View Contents:

```bash
cat /etc/os-release
```

Example Information:

```text
NAME="Ubuntu"
VERSION_ID="24.04"
PRETTY_NAME="Ubuntu 24.04.1 LTS"
```

---

## Linux Investigation Workflow

### Typical Process

```text
Open Terminal
      ↓
Check Current Location
      ↓
Explore Directories
      ↓
Search for Files
      ↓
Read File Contents
      ↓
Gather System Information
      ↓
Analyze Results
```

---

## Advantages / Benefits

* Fast system navigation
* Efficient file management
* Direct operating system interaction
* Remote administration capability
* Strong troubleshooting support
* Essential for cybersecurity operations
* Low resource consumption
* Powerful automation potential
* Enhanced visibility into system internals
* Industry-standard administration method

---

## Key Characteristics

* Linux CLI is text-based.
* Commands are executed through a terminal.
* The shell interprets user commands.
* Linux uses a hierarchical filesystem structure.
* Hidden files begin with a period (`.`).
* `pwd` displays the current directory.
* `ls` lists files and directories.
* `cd` changes directories.
* `find` locates files within the filesystem.
* `cat` displays file contents.
* `whoami` identifies the current user.
* `uname -a` provides system information.
* `df -h` displays storage information.
* `/etc` contains important system configuration files.

---

## Example

A cybersecurity analyst gains access to a Linux server and needs to understand the environment.

### Step 1: Identify Current User

```bash
whoami
```

Output:

```text
ubuntu
```

### Step 2: Check Current Directory

```bash
pwd
```

Output:

```text
/var/log
```

### Step 3: Locate a Report File

```bash
find ~ -name report.txt
```

### Step 4: Read the File

```bash
cat report.txt
```

### Step 5: Identify Operating System

```bash
cat /etc/os-release
```

The analyst successfully gathers the information needed to begin further investigation.

---

## Key Notes

| Command               | Purpose                               |
| --------------------- | ------------------------------------- |
| `pwd`                 | Show current directory                |
| `ls`                  | List files and folders                |
| `ls -l`               | Detailed file listing                 |
| `ls -al`              | Show all files including hidden files |
| `cd`                  | Change directory                      |
| `cd ..`               | Move to parent directory              |
| `find`                | Search for files                      |
| `cat`                 | Display file contents                 |
| `whoami`              | Show current user                     |
| `uname -a`            | Show system information               |
| `df -h`               | Show disk usage                       |
| `cat /etc/os-release` | Show Linux distribution information   |

### Important Directories

```text
/
├── home
├── etc
├── var
├── tmp
├── usr
└── dev
```

### Important Files

```text
/etc/os-release
mission_brief.txt
day1_report.txt
.bashrc
.profile
```

---

## Learning Outcome

After completing this room, I developed a foundational understanding of the Linux Command-Line Interface and learned how to interact with a Linux system using essential terminal commands. I gained practical experience navigating the filesystem, exploring directories, locating files, reading file contents, gathering system information, and investigating operating system details through configuration files. These skills establish a strong foundation for Linux administration, cybersecurity operations, incident response, digital forensics, and advanced security tooling that will be explored in future Linux and cybersecurity training.
