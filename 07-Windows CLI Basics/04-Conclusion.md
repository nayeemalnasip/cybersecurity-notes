# Windows CLI Basics

## Windows Command-Line Fundamentals and System Interaction

### Overview

The Windows Command Prompt (CMD) provides a powerful text-based interface for interacting directly with the Windows operating system. While graphical tools remain useful for everyday tasks, command-line utilities offer faster access to files, system information, and administrative functions. Mastering basic Windows CLI commands is an essential skill for IT professionals, system administrators, and cybersecurity practitioners.

Throughout this room, you explored how to navigate the Windows filesystem, locate files, inspect hidden content, read files directly from the terminal, and gather important system and network information.

---

## Main Concept

### What is the Windows Command Line?

The Windows Command Line, commonly referred to as Command Prompt (CMD), is a command-driven interface that allows users to interact with the operating system through text commands instead of graphical menus and windows.

CMD enables users to:

* Navigate the filesystem
* Manage files and folders
* Retrieve system information
* Troubleshoot issues
* Automate administrative tasks
* Perform security investigations

It provides greater control, speed, and flexibility compared to relying solely on the graphical interface.

---

## How It Works

### File and Directory Navigation

Users can move through folders and explore the filesystem using commands such as:

```cmd
cd
dir
cd ..
```

---

### File Discovery

Windows can recursively search directories to locate files without manually browsing folders.

```cmd
dir /s filename.txt
```

---

### Hidden File Inspection

System and hidden files can be revealed using:

```cmd
dir /a
```

---

### File Reading

Text files can be viewed directly within the terminal.

```cmd
type filename.txt
```

---

### System Information Collection

Built-in commands provide information about:

* Current user
* Computer name
* Operating system
* Network configuration

```cmd
whoami
hostname
systeminfo
ipconfig
```

---

## Important Components

## Command Prompt (CMD)

A built-in Windows application that interprets and executes text-based commands.

Purpose:

* System administration
* Troubleshooting
* File management
* Security analysis

---

## File Navigation Commands

### Display Current Directory

```cmd
cd
```

---

### List Directory Contents

```cmd
dir
```

---

### Show Hidden Files

```cmd
dir /a
```

---

### Change Directory

```cmd
cd FolderName
```

---

### Move to Parent Directory

```cmd
cd ..
```

---

## File Discovery Tools

### Recursive File Search

```cmd
dir /s task_brief.txt
```

Purpose:

* Locate files anywhere within a directory structure
* Support investigations and troubleshooting
* Quickly identify file locations

---

## File Viewing

### Display File Content

```cmd
type task_brief.txt
```

Purpose:

* Read text files
* Review logs
* Inspect configuration files
* Access instructions and reports

---

## System Identification Commands

### Current User

```cmd
whoami
```

Displays:

```text
Current Logged-in User
```

---

### Computer Name

```cmd
hostname
```

Displays:

```text
System Hostname
```

---

### Operating System Information

```cmd
systeminfo
```

Provides:

* OS Name
* OS Version
* System Type
* Memory Information
* Hostname

---

## Network Information

### View Network Configuration

```cmd
ipconfig
```

Displays:

* IPv4 Address
* Subnet Mask
* Default Gateway
* Network Adapter Information

---

### Example Output

```text
IPv4 Address : 192.168.1.10
Default Gateway : 192.168.1.1
```

---

## Important Concepts

| Concept                      | Description                                      |
| ---------------------------- | ------------------------------------------------ |
| Command-Line Interface (CLI) | Text-based interaction with the operating system |
| Filesystem Navigation        | Moving between folders and directories           |
| Recursive Search             | Searching through all subdirectories             |
| Hidden Files                 | Files concealed from normal directory listings   |
| Hostname                     | Unique system identifier on a network            |
| IPv4 Address                 | Network address assigned to a device             |
| Default Gateway              | Router used to access external networks          |
| System Information           | Hardware and OS configuration details            |

---

## Advantages / Benefits

* Faster than navigating through graphical menus
* Provides precise control over system operations
* Useful for remote administration
* Essential for automation and scripting
* Supports incident response and investigations
* Allows access to hidden files and system information
* Commonly used across IT and cybersecurity environments
* Requires minimal system resources

---

## Key Characteristics

* Built into all modern Windows operating systems.
* Supports file and directory management.
* Enables rapid information gathering.
* Useful in local and remote environments.
* Often required for cybersecurity investigations.
* Provides direct access to operating system functions.
* Frequently used by administrators and security analysts.
* Forms the foundation for advanced Windows administration.

---

## Example

A cybersecurity analyst receives an alert regarding suspicious activity on a workstation.

### Identify Current User

```cmd
whoami
```

Output:

```text
administrator
```

---

### Verify Hostname

```cmd
hostname
```

Output:

```text
WORKSTATION-01
```

---

### Review Operating System Details

```cmd
systeminfo
```

Output:

```text
OS Name: Microsoft Windows Server 2019
System Type: x64-based PC
```

---

### Check Network Configuration

```cmd
ipconfig
```

Output:

```text
IPv4 Address : 10.10.10.15
Default Gateway : 10.10.10.1
```

---

### Result

The analyst quickly identifies the system, verifies the user account, confirms the operating system version, and gathers network details required for further investigation.

---

## Key Notes

### Essential Navigation Commands

```cmd
cd
dir
dir /a
cd ..
```

---

### Essential File Operations

```cmd
dir /s filename
type filename
```

---

### Essential System Information Commands

```cmd
whoami
hostname
systeminfo
ipconfig
```

---

### Common Cybersecurity Applications

* Incident Response
* Threat Hunting
* Digital Forensics
* Asset Discovery
* System Auditing
* Troubleshooting
* Security Monitoring

---

## Learning Outcome

After completing this room, I developed a solid understanding of how to interact with Windows systems using the Command Prompt. I learned how to navigate directories, locate files, reveal hidden content, read files directly from the terminal, and gather critical system and network information. These foundational command-line skills are essential for Windows administration, troubleshooting, cybersecurity investigations, incident response activities, and advanced security operations in enterprise environments.
