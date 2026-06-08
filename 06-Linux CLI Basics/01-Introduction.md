# Linux CLI Basics

## Introduction to the Linux Command-Line Interface (CLI)

### Overview

Linux is one of the most important operating systems in cybersecurity, powering web servers, cloud infrastructure, networking devices, embedded systems, and security-focused environments. While many operating systems provide graphical interfaces, cybersecurity professionals frequently rely on the Linux Command-Line Interface (CLI) to perform administration, troubleshooting, automation, forensic analysis, and security testing tasks.

This room introduces the fundamentals of the Linux CLI through a practical, hands-on scenario. As a new IT Support Engineer in a Cyber Operations Support Team, you will learn how to interact with a Linux system using terminal commands, navigate the filesystem, and gather information directly from the operating system.

---

## Main Concept

### What is the Linux Command-Line Interface (CLI)?

The Command-Line Interface (CLI) is a text-based method of interacting with an operating system by entering commands through a terminal.

Instead of clicking icons and menus like a Graphical User Interface (GUI), users type commands that the operating system interprets and executes.

The CLI provides:

* Direct system interaction
* Faster administration
* Automation capabilities
* Greater control over system resources
* Remote system management

In Linux environments, the CLI is often the preferred method for managing systems, especially servers and cybersecurity tools.

---

## How It Works

### Step 1: Open a Terminal

A terminal application provides access to the Linux command-line environment.

### Step 2: Enter Commands

Users type commands into the terminal.

Example:

```bash
pwd
```

### Step 3: Shell Processes the Command

The shell interprets the command and communicates with the operating system.

### Step 4: Operating System Executes the Request

Linux performs the requested action.

Examples:

* Display information
* Navigate directories
* Create files
* Manage users
* Execute programs

### Step 5: Output is Returned

The terminal displays the result.

```text
User
   ↓
Terminal
   ↓
Shell
   ↓
Linux Kernel
   ↓
System Resources
```

---

## Important Components

## Linux Operating System

### What is Linux?

Linux is an open-source operating system widely used in:

* Servers
* Cloud environments
* Embedded systems
* Cybersecurity laboratories
* Network infrastructure

Popular Linux Distributions:

| Distribution             | Common Usage        |
| ------------------------ | ------------------- |
| Ubuntu                   | Desktop & Server    |
| Debian                   | Servers             |
| Kali Linux               | Penetration Testing |
| Fedora                   | Development         |
| Red Hat Enterprise Linux | Enterprise Systems  |

---

## Terminal

### What is a Terminal?

A terminal is a program that provides access to the command-line interface.

It allows users to:

* Execute commands
* Run applications
* Manage files
* Interact with the operating system

Example Terminal Prompt:

```bash
user@linux:~$
```

---

## Shell

### What is a Shell?

The shell is a command interpreter that sits between the user and the operating system.

Responsibilities:

* Interpret commands
* Execute programs
* Manage scripts
* Control processes

Common Linux Shells:

| Shell | Description                |
| ----- | -------------------------- |
| Bash  | Most common Linux shell    |
| Zsh   | Enhanced interactive shell |
| Sh    | Original Unix shell        |
| Fish  | User-friendly shell        |

Example:

```bash
echo "Hello Linux"
```

---

## Linux Filesystem

### What is the Linux Filesystem?

Linux organizes files using a hierarchical directory structure that begins from a single root directory.

Unlike Windows:

```text
Windows:
C:\Users\Admin\Documents
```

Linux uses:

```text
/home/user/Documents
```

---

### Root Directory

The root directory is represented by:

```bash
/
```

It serves as the starting point for the entire filesystem.

Example Structure:

```text
/
├── bin
├── boot
├── dev
├── etc
├── home
├── opt
├── tmp
├── usr
└── var
```

---

## Home Directory

Each user typically has a personal workspace known as the home directory.

Example:

```bash
/home/intern
```

Shortcut:

```bash
~
```

Examples:

```bash
cd ~
cd /home/intern
```

---

## Why Cybersecurity Professionals Use the CLI

The Linux CLI is widely used because it allows:

### Faster Operations

Tasks can be completed quickly through commands.

Example:

```bash
ls
```

---

### Automation

Scripts can automate repetitive work.

Example:

```bash
#!/bin/bash
echo "System Check Complete"
```

---

### Remote Administration

Many servers operate without graphical interfaces.

Administrators connect remotely using:

```bash
ssh username@server
```

---

### Security Analysis

The CLI provides access to:

* Logs
* Processes
* Network information
* Security tools

Examples:

```bash
ps
netstat
journalctl
```

---

## Basic Navigation Concepts

### Current Working Directory

The current location inside the filesystem.

Command:

```bash
pwd
```

Example Output:

```text
/home/intern
```

---

### Viewing Files and Directories

Command:

```bash
ls
```

Example Output:

```text
Documents
Downloads
Projects
```

---

### Changing Directories

Command:

```bash
cd
```

Example:

```bash
cd Documents
```

---

### Returning to Home Directory

Command:

```bash
cd ~
```

or

```bash
cd
```

---

## Common Beginner Commands

| Command | Purpose                   |
| ------- | ------------------------- |
| pwd     | Display current directory |
| ls      | List files and folders    |
| cd      | Change directory          |
| clear   | Clear terminal screen     |
| whoami  | Display current user      |
| echo    | Print text                |
| mkdir   | Create directory          |
| touch   | Create file               |

Examples:

```bash
pwd
ls
whoami
```

---

## Advantages / Benefits

* Direct interaction with Linux systems
* Faster than GUI for many tasks
* Ideal for remote administration
* Essential for cybersecurity operations
* Supports scripting and automation
* Provides detailed system visibility
* Uses minimal system resources
* Widely supported across Linux distributions

---

## Key Characteristics

* The CLI is text-based.
* Commands are entered through a terminal.
* The shell interprets user commands.
* Linux uses a hierarchical filesystem.
* The root directory (`/`) is the top-level directory.
* User files are commonly stored in `/home`.
* CLI skills are fundamental for cybersecurity professionals.
* Most Linux servers are administered through the command line.
* Many security tools operate primarily through the terminal.
* Command-line knowledge improves troubleshooting and automation capabilities.

---

## Example

A cybersecurity intern needs to determine their current location in the filesystem.

### Workflow

```bash
pwd
```

Output:

```text
/home/intern
```

Next, they view available files:

```bash
ls
```

Output:

```text
Documents
Downloads
Projects
```

Finally, they navigate into the Documents folder:

```bash
cd Documents
```

This demonstrates the basic process of filesystem navigation using the Linux CLI.

---

## Key Notes

| Term                 | Definition                       |
| -------------------- | -------------------------------- |
| Linux                | Open-source operating system     |
| CLI                  | Command-Line Interface           |
| Terminal             | Program used to access the CLI   |
| Shell                | Command interpreter              |
| Filesystem           | Structure used to organize files |
| Root Directory (`/`) | Top-level Linux directory        |
| Home Directory (`~`) | User's personal workspace        |
| `pwd`                | Show current directory           |
| `ls`                 | List directory contents          |
| `cd`                 | Change directory                 |

---

## Learning Outcome

After completing this section, I understood the purpose and importance of the Linux Command-Line Interface (CLI) and how it differs from graphical interfaces. I learned the role of the terminal and shell, became familiar with the Linux filesystem structure, and gained foundational knowledge of command-line navigation. These concepts provide the essential skills required for Linux administration, cybersecurity operations, troubleshooting, automation, and future hands-on work within Linux-based environments.
