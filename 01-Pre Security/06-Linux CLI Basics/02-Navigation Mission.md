# Linux CLI Basics

## Linux Filesystem Navigation and File Discovery

### Overview

Efficient navigation of the Linux filesystem is a fundamental skill for system administrators, cybersecurity analysts, and IT professionals. Most cybersecurity activities, including log analysis, incident response, system administration, and penetration testing, require working within the Linux terminal.

This section introduces essential Linux navigation commands used to locate files, explore directories, view file information, and read file contents. Through a practical mission scenario, you will learn how to move through the filesystem, discover files, and retrieve information directly from the command line.

---

## Main Concept

### What is Filesystem Navigation?

Filesystem navigation refers to the process of moving through directories, locating files, and accessing information stored within a Linux system.

Linux uses a hierarchical directory structure where files and folders are organized under a single root directory (`/`).

Using terminal commands, users can:

* Determine their current location
* View directory contents
* Move between folders
* Locate files
* Read file contents
* Investigate system resources

These operations form the foundation of daily Linux administration and cybersecurity work.

---

## How It Works

### Step 1: Determine Current Location

Use the `pwd` command to identify the current working directory.

```bash
pwd
```

Example:

```text
/home/ubuntu
```

---

### Step 2: View Available Files and Directories

Use the `ls` command to display directory contents.

```bash
ls
```

---

### Step 3: Obtain Detailed Information

Use the long listing option.

```bash
ls -l
```

This displays:

* Permissions
* Owner
* Group
* File size
* Modification date
* File name

---

### Step 4: Display Hidden Files

Use:

```bash
ls -al
```

This reveals hidden files and directories.

---

### Step 5: Change Directory

Navigate into a directory.

```bash
cd Documents
```

Move back one level.

```bash
cd ..
```

---

### Step 6: Locate Files

Search for files using the `find` command.

```bash
find ~ -name mission_brief.txt
```

---

### Step 7: Read File Contents

Display file contents.

```bash
cat mission_brief.txt
```

---

## Important Components

## Terminal

### What is a Terminal?

A terminal is a text-based interface that allows users to interact directly with the Linux operating system.

Functions:

* Execute commands
* Manage files
* Run programs
* Configure systems
* Perform security tasks

Example Prompt:

```bash
ubuntu@tryhackme:~$
```

---

## Current Working Directory

### pwd Command

The `pwd` command displays the current directory.

Syntax:

```bash
pwd
```

Example:

```bash
ubuntu@tryhackme:~$ pwd
/home/ubuntu
```

Meaning:

```text
Current Location:
/home/ubuntu
```

---

## Listing Directory Contents

### ls Command

Displays files and directories.

Syntax:

```bash
ls
```

Example:

```text
Desktop
Documents
Downloads
Music
Pictures
```

---

### ls -l Command

Provides detailed information.

Syntax:

```bash
ls -l
```

Example Output:

```text
drwxr-xr-x 2 ubuntu ubuntu 4096 Desktop
-rw-r--r-- 1 ubuntu ubuntu 120 report.txt
```

---

### Understanding File Permissions

Example:

```text
drwxr-xr-x
```

Breakdown:

| Section | Meaning            |
| ------- | ------------------ |
| d       | Directory          |
| rwx     | Owner Permissions  |
| r-x     | Group Permissions  |
| r-x     | Others Permissions |

Permission Types:

| Symbol | Meaning |
| ------ | ------- |
| r      | Read    |
| w      | Write   |
| x      | Execute |

---

## Hidden Files

### What are Hidden Files?

Hidden files begin with a period (`.`).

Examples:

```text
.bashrc
.profile
.gitconfig
```

These files are typically used for:

* Configuration
* Preferences
* Environment settings

---

### Viewing Hidden Files

Syntax:

```bash
ls -al
```

Example:

```text
.bashrc
.profile
.Xauthority
```

---

## Directory Navigation

### cd Command

Changes the current directory.

Syntax:

```bash
cd <directory>
```

Example:

```bash
cd Documents
```

Result:

```text
/home/ubuntu/Documents
```

---

### Moving Back One Directory

Syntax:

```bash
cd ..
```

Example:

```text
/home/ubuntu/Documents
      ↓
/home/ubuntu
```

---

### Navigation Symbols

| Symbol | Meaning           |
| ------ | ----------------- |
| `.`    | Current Directory |
| `..`   | Parent Directory  |
| `~`    | Home Directory    |
| `/`    | Root Directory    |

Examples:

```bash
cd ~
cd ..
cd /
```

---

## File Searching

### find Command

The `find` utility searches for files and directories.

Syntax:

```bash
find <starting_location> -name <filename>
```

Example:

```bash
find ~ -name mission_brief.txt
```

Output:

```text
/home/ubuntu/projects/reports/mission_brief.txt
```

---

### Why Cybersecurity Professionals Use find

Common uses:

* Locate log files
* Find configuration files
* Search for malware indicators
* Discover sensitive files
* Investigate incidents

Examples:

```bash
find /var/log -name "*.log"
find /home -name "*.txt"
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
cat mission_brief.txt
```

Output:

```text
Great job finding your way around the terminal.

Your next assignment is to collect a small system report...
```

---

### Common Uses of cat

* Read configuration files
* View logs
* Examine scripts
* Review reports

Examples:

```bash
cat /etc/os-release
cat report.txt
cat script.sh
```

---

## Linux Navigation Workflow

### Typical Investigation Process

```text
Open Terminal
      ↓
pwd
      ↓
ls
      ↓
cd Directory
      ↓
find File
      ↓
cat File
      ↓
Gather Information
```

---

## Advantages / Benefits

* Fast filesystem navigation
* Efficient file discovery
* Complete system visibility
* Works on GUI and non-GUI systems
* Essential for remote administration
* Useful for security investigations
* Supports automation and scripting
* Low resource consumption
* Powerful file management capabilities
* Core skill for Linux professionals

---

## Key Characteristics

* Linux navigation is command-line driven.
* `pwd` displays the current location.
* `ls` lists files and directories.
* `ls -l` displays detailed file information.
* `ls -al` reveals hidden files.
* `cd` changes directories.
* `cd ..` moves to the parent directory.
* `find` searches for files and directories.
* `cat` displays file contents.
* Hidden files begin with a period (`.`).

---

## Example

A cybersecurity analyst needs to locate a report file.

### Step 1: Verify Current Location

```bash
pwd
```

Output:

```text
/home/ubuntu
```

### Step 2: Search for the File

```bash
find ~ -name report.txt
```

Output:

```text
/home/ubuntu/Documents/report.txt
```

### Step 3: Navigate to the Directory

```bash
cd Documents
```

### Step 4: Read the File

```bash
cat report.txt
```

The analyst successfully locates and reviews the report using Linux CLI commands.

---

## Key Notes

| Command  | Purpose                               |
| -------- | ------------------------------------- |
| `pwd`    | Display current directory             |
| `ls`     | List directory contents               |
| `ls -l`  | Detailed directory listing            |
| `ls -al` | Show all files including hidden files |
| `cd`     | Change directory                      |
| `cd ..`  | Move to parent directory              |
| `find`   | Search for files and directories      |
| `cat`    | Display file contents                 |
| `~`      | Home directory                        |
| `/`      | Root directory                        |

### Important Hidden File Examples

```text
.bashrc
.profile
.gitconfig
.Xauthority
```

### Important Navigation Symbols

```text
.   = Current Directory
..  = Parent Directory
~   = Home Directory
/   = Root Directory
```

---

## Learning Outcome

After completing this section, I learned how to navigate the Linux filesystem using the command-line interface. I gained practical experience using commands such as `pwd`, `ls`, `cd`, `find`, and `cat` to identify my location, explore directories, locate files, and read their contents. I also learned how Linux handles hidden files and directory structures, providing essential skills for system administration, troubleshooting, digital investigations, and cybersecurity operations.
