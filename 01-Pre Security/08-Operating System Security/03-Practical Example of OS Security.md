## Practical Example of OS Security

### Overview

Operating system security is not only about understanding concepts such as confidentiality, integrity, and availability; it also involves recognizing how attackers exploit weak security practices in real environments. One of the most common attack methods is gaining unauthorized access through weak passwords and poor account security.

In this practical scenario, a security assessment demonstrates how attackers can leverage weak credentials to access Linux systems, enumerate files, gather information, and potentially escalate privileges.

---

## Authentication Attacks and Unauthorized Access

### What is Authentication?

Authentication is the process of verifying a user's identity before granting access to a system.

Common authentication methods include:

* Username and Password
* PIN Codes
* Biometrics
* Security Tokens
* Multi-Factor Authentication (MFA)

If authentication is weak, attackers may gain unauthorized access to systems and sensitive data.

---

## Attack Scenario

### Security Assessment Overview

A cybersecurity team was hired to assess the security posture of a company.

During a physical inspection, investigators discovered a sticky note containing:

```text
Username: sammie
Password: dragon
```

This represents a common security mistake where users write passwords in visible locations.

The objective was to determine whether the discovered password could be used to gain access to a Linux system.

---

## Secure Shell (SSH)

### What is SSH?

SSH (Secure Shell) is a secure network protocol used to remotely access and manage systems.

### Key Features

* Encrypted communication
* Remote system administration
* Secure file transfers
* Authentication support

### SSH Connection Syntax

```bash
ssh username@target_ip
```

Example:

```bash
ssh sammie@192.168.1.10
```

---

## Linux User Accounts and Privileges

### Standard User Accounts

Regular users have limited permissions.

Examples:

```text
sammie
johnny
linda
```

These users can:

* Access personal files
* Run applications
* Perform basic tasks

They cannot:

* Modify critical system files
* Install system-wide software without permission
* Manage other user accounts

---

### Administrative Accounts

Administrative accounts possess unrestricted access.

| Operating System | Administrator Account |
| ---------------- | --------------------- |
| Linux            | root                  |
| Android          | root                  |
| macOS            | root                  |
| Windows          | administrator         |

### Root Account Characteristics

* Full system access
* Can modify all files
* Can create or delete users
* Can install software
* Can change system configurations

```text
Highest Privilege Level
        │
        ▼
      root
```

---

## Linux Commands Used During Investigation

### whoami Command

#### Purpose

Displays the currently logged-in user.

#### Syntax

```bash
whoami
```

#### Example

```bash
sammie@machine:~$ whoami
sammie
```

#### Use Cases

* Verify account identity
* Confirm privilege level
* Audit active sessions

---

### ls Command

#### Purpose

Lists files and directories in the current location.

#### Syntax

```bash
ls
```

#### Example

```bash
ls
```

Output:

```text
country.txt
draft.md
icon.png
password.txt
profile.jpg
```

---

### cat Command

#### Purpose

Displays file contents directly in the terminal.

#### Syntax

```bash
cat filename
```

#### Example

```bash
cat draft.md
```

Output:

```text
# Operating System Security

Reusing passwords means that your password
for other sites becomes exposed if one
service is hacked.
```

---

### history Command

#### Purpose

Displays previously executed commands.

#### Syntax

```bash
history
```

#### Example

```bash
history
```

Output:

```text
1 whoami
2 ls
3 cat draft.md
4 history
```

---

## User Enumeration

### What is User Enumeration?

User enumeration is the process of identifying valid usernames on a system.

In this scenario, known users included:

```text
sammie
johnny
linda
```

Attackers often collect usernames before attempting password attacks.

---

## Password Guessing Attacks

### What is Password Guessing?

Password guessing involves trying likely passwords based on:

* Common passwords
* Personal information
* Company information
* Password reuse patterns

### Example

```text
Username: sammie
Password: dragon
```

Because "dragon" is a common password, it represents poor password hygiene.

---

## Switching Users with su

### What is su?

The `su` (Substitute User) command allows switching from one user account to another.

### Syntax

```bash
su - username
```

### Example

```bash
su - johnny
```

The system then requests the target user's password.

---

## Security Weaknesses Demonstrated

### 1. Password Exposure

#### Problem

Credentials written on sticky notes.

#### Risk

Anyone nearby can view and use them.

#### Impact

* Confidentiality compromised
* Unauthorized access granted

---

### 2. Weak Password Selection

#### Problem

Using predictable passwords.

Example:

```text
dragon
password
123456
```

#### Risk

Easy to guess or crack.

#### Impact

* Account compromise
* Data theft
* Unauthorized system access

---

### 3. Password Reuse

#### Problem

Using identical passwords across multiple accounts.

#### Risk

Compromise of one account can lead to compromise of many others.

#### Impact

* Credential stuffing attacks
* Account takeover

---

## Security Best Practices

### Strong Password Policies

Use passwords that:

* Are at least 12–16 characters
* Include uppercase letters
* Include lowercase letters
* Include numbers
* Include special characters

Example:

```text
T#9uV@4rL!2pX$7n
```

---

### Multi-Factor Authentication (MFA)

Combine:

```text
Something You Know
+
Something You Have
=
Stronger Security
```

Example:

* Password
* Mobile Authentication App

---

### Credential Protection

Never:

```text
✗ Write passwords on sticky notes
✗ Share passwords
✗ Reuse passwords
✗ Store passwords in plain text
```

Always:

```text
✓ Use a password manager
✓ Enable MFA
✓ Use unique passwords
✓ Change compromised credentials
```

---

## Advantages of Proper OS Security

* Prevents unauthorized access
* Protects sensitive information
* Reduces credential theft risks
* Strengthens authentication controls
* Supports regulatory compliance
* Protects organizational assets
* Improves overall cybersecurity posture

---

## Key Characteristics

* SSH provides secure remote access.
* Authentication verifies user identity.
* Linux uses user privilege separation.
* Root accounts have unrestricted access.
* Weak passwords are a major attack vector.
* Password reuse significantly increases risk.
* User enumeration often precedes password attacks.
* Commands such as `whoami`, `ls`, `cat`, and `history` assist in system investigation.
* Administrative accounts require stronger protection than standard accounts.

---

## Example

### Vulnerable Environment

```text
Username: sammie
Password: dragon

Sticky Note Attached To Monitor
```

Result:

```text
Attacker Finds Credentials
        ↓
SSH Login Successful
        ↓
Access Granted
        ↓
Potential Data Exposure
```

---

### Secure Environment

```text
Username: sammie
Password: Unique & Complex

MFA Enabled
No Visible Credentials
```

Result:

```text
Unauthorized Login Attempt
        ↓
Authentication Failure
        ↓
System Remains Secure
```

---

## Key Notes

* SSH is used for secure remote system access.
* `whoami` identifies the current user.
* `ls` lists files and directories.
* `cat` displays file contents.
* `history` shows previously executed commands.
* Linux administrative accounts use the `root` user.
* Weak passwords are one of the most common causes of system compromise.
* Password reuse increases attack success rates.
* Credential exposure can lead to unauthorized system access.
* Strong authentication practices are critical for OS security.

---

## Learning Outcome

After completing this section, I understood how weak authentication practices can lead to unauthorized access in Linux environments. I learned how attackers exploit exposed credentials, how SSH is used for remote system access, and how common Linux commands such as `whoami`, `ls`, `cat`, and `history` help users investigate systems. I also gained practical insight into user privilege levels, password security risks, and the importance of following strong authentication and credential management practices to secure operating systems.
