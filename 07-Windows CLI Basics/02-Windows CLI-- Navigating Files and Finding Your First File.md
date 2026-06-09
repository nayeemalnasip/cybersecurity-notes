# Windows CLI Basics

## Windows CLI Navigation, File Discovery, and File Reading

### Overview

Navigating the Windows filesystem through the Command-Line Interface (CLI) is a fundamental skill for IT professionals, system administrators, and cybersecurity practitioners. While the Graphical User Interface (GUI) provides a user-friendly way to access files and folders, the Command Prompt offers faster navigation, efficient file searching, and direct interaction with the operating system.

In this section, you will learn how to identify your current location, explore directories, reveal hidden files, navigate the filesystem, search for files recursively, and read file contents using native Windows CLI commands.

---

## Main Concept

### What is Windows Filesystem Navigation?

Windows filesystem navigation is the process of moving through directories, locating files, and interacting with stored data using command-line commands.

These skills are essential for:

* System administration
* Troubleshooting
* Incident response
* Digital forensics
* Malware analysis
* Cybersecurity investigations

Instead of manually browsing folders, users can quickly search and access information using commands.

---

## How It Works

### Step 1: Determine Current Location

Display the current working directory.

```cmd
cd
```

---

### Step 2: View Directory Contents

List files and folders within the current directory.

```cmd
dir
```

---

### Step 3: Display Hidden Files

Show all files and folders, including hidden items.

```cmd
dir /a
```

---

### Step 4: Navigate Through Directories

Move between folders using the `cd` command.

```cmd
cd Documents
```

Move back one directory level:

```cmd
cd ..
```

---

### Step 5: Search for a File

Locate a file recursively within subdirectories.

```cmd
dir /s task_brief.txt
```

---

### Step 6: Navigate to File Location

Move to the directory containing the target file.

```cmd
cd <file_path>
```

---

### Step 7: Read File Contents

Display the contents of a text file.

```cmd
type task_brief.txt
```

---

## Important Components

## Current Working Directory

### cd Command

The `cd` command displays the current directory and is also used to change directories.

Display Current Directory:

```cmd
cd
```

Example Output:

```text
C:\Users\Administrator
```

---

### Change Directory

Move into a folder:

```cmd
cd Documents
```

Example:

```text
C:\Users\Administrator\Documents
```

---

### Move Back One Level

```cmd
cd ..
```

Example:

```text
C:\Users\Administrator
```

---

## Directory Listing

### dir Command

Displays files and folders in the current directory.

Syntax:

```cmd
dir
```

Example Output:

```text
Directory of C:\Users\Administrator

Desktop
Documents
Downloads
Pictures
Videos
```

---

### Information Displayed

| Field | Description                |
| ----- | -------------------------- |
| Date  | Creation/Modification Date |
| Time  | File Timestamp             |
| Type  | File or Directory          |
| Name  | Item Name                  |
| Size  | File Size                  |

---

## Hidden Files and Folders

### dir /a Command

Displays all files, including hidden and system files.

Syntax:

```cmd
dir /a
```

Example:

```text
desktop.ini
AppData
NTUSER.DAT
```

---

### Why Hidden Files Exist

Windows hides certain files to:

* Protect system configurations
* Prevent accidental modification
* Store application settings
* Maintain operating system stability

---

### Common Hidden Items

```text
AppData
desktop.ini
NTUSER.DAT
```

---

## Windows Filesystem Structure

Windows organizes files using a hierarchical directory structure.

Example:

```text
C:\
└── Users
    └── Administrator
        ├── Desktop
        ├── Documents
        ├── Downloads
        ├── Pictures
        └── Videos
```

---

## File Discovery

### Recursive Search

Searching manually through directories can be time-consuming. Windows provides recursive search functionality.

Syntax:

```cmd
dir /s filename
```

Example:

```cmd
dir /s task_brief.txt
```

---

### Understanding the `/s` Switch

```text
/s
```

Meaning:

```text
Search all subdirectories recursively
```

---

### Search Process

```text
Current Directory
        ↓
Subdirectory 1
        ↓
Subdirectory 2
        ↓
Subdirectory N
        ↓
Target File Found
```

---

## Reading File Contents

### type Command

The `type` command displays the contents of text files directly within the Command Prompt.

Syntax:

```cmd
type filename
```

Example:

```cmd
type task_brief.txt
```

---

### Common Uses

* Read notes
* View logs
* Examine configuration files
* Inspect reports
* Review scripts

Examples:

```cmd
type report.txt
type notes.txt
type config.txt
```

---

## File Investigation Workflow

### Practical Process

```text
Open Command Prompt
        ↓
Identify Current Location
        ↓
List Directory Contents
        ↓
Reveal Hidden Files
        ↓
Search Target File
        ↓
Navigate to Location
        ↓
Read File Contents
        ↓
Collect Information
```

---

## Advantages / Benefits

* Faster file discovery
* Efficient directory navigation
* No dependency on GUI tools
* Useful for remote administration
* Essential for cybersecurity investigations
* Supports large-scale file searches
* Provides direct access to hidden files
* Improves troubleshooting efficiency

---

## Key Characteristics

* Windows CLI uses drive-letter-based paths.
* `cd` displays and changes directories.
* `dir` lists files and folders.
* `dir /a` reveals hidden files.
* `dir /s` performs recursive searches.
* `type` displays file contents.
* Hidden files are protected by default.
* Windows uses a hierarchical filesystem structure.
* Command-line navigation is often faster than GUI navigation.
* File searching is a common cybersecurity investigation technique.

---

## Example

A security analyst receives a file name but does not know its location.

### Check Current Directory

```cmd
cd
```

Output:

```text
C:\Users\Administrator
```

---

### Search for the File

```cmd
dir /s task_brief.txt
```

Output:

```text
C:\Users\Administrator\Documents\Investigations\task_brief.txt
```

---

### Navigate to the Folder

```cmd
cd Documents\Investigations
```

---

### Confirm File Exists

```cmd
dir
```

Output:

```text
task_brief.txt
```

---

### Read the File

```cmd
type task_brief.txt
```

The analyst successfully locates and reviews the file using only Windows command-line tools.

---

## Key Notes

| Command           | Purpose                             |
| ----------------- | ----------------------------------- |
| `cd`              | Display or change current directory |
| `cd ..`           | Move to parent directory            |
| `dir`             | List directory contents             |
| `dir /a`          | Show hidden files and folders       |
| `dir /s filename` | Search recursively for a file       |
| `type filename`   | Display file contents               |

### Important Windows Paths

```text
C:\Users
C:\Users\Administrator
C:\Users\Administrator\Desktop
C:\Users\Administrator\Documents
```

### Important Concepts

```text
Working Directory
Filesystem
Directory
Path
Recursive Search
Hidden Files
File Investigation
```

---

## Learning Outcome

After completing this section, I learned how to navigate the Windows filesystem using the Command Prompt. I gained practical experience identifying my current location, listing directory contents, viewing hidden files, moving between directories, searching for files recursively, and reading text file contents directly from the command line. These skills provide a strong foundation for Windows administration, troubleshooting, incident response, digital forensics, and cybersecurity investigations where efficient file discovery and system navigation are essential.
