# Linux Fundamentals Part 1

## Main Concepts

### Running Your First Linux Commands

#### What is it?

The Linux Terminal is a command-line interface (CLI) that allows users to interact directly with the operating system using text-based commands. Unlike Windows or macOS, many Linux systems—especially servers—operate without a graphical user interface (GUI), making terminal proficiency an essential skill.

In cybersecurity, the terminal is one of the most important tools because most security assessments, server administration tasks, and automation processes are performed through command-line interactions.

---

#### How It Works

1. Open a terminal session.
2. Enter a command.
3. The shell interprets the command.
4. Linux executes the requested action.
5. The output is displayed in the terminal.

Example terminal prompt:

```bash
tryhackme@linux1:~$
```

Prompt Breakdown:

| Component | Description                        |
| --------- | ---------------------------------- |
| tryhackme | Username                           |
| linux1    | Hostname (machine name)            |
| ~         | Current directory (Home Directory) |
| $         | Standard user prompt               |

---

### The `echo` Command

#### What is it?

The `echo` command displays text directly in the terminal.

#### Syntax

```bash
echo <text>
```

#### Examples

Single Word:

```bash
echo Hello
```

Output:

```text
Hello
```

Multiple Words:

```bash
echo "Hello Friend!"
```

Output:

```text
Hello Friend!
```

#### Important Notes

* Quotes are optional for a single word.
* Quotes are recommended when spaces exist in the text.
* Frequently used in shell scripting for displaying messages and debugging.

---

### The `whoami` Command

#### What is it?

The `whoami` command displays the username of the currently logged-in user.

#### Syntax

```bash
whoami
```

#### Example

```bash
whoami
```

Output:

```text
tryhackme
```

#### Cyber Security Relevance

The `whoami` command is commonly used during:

* Privilege Escalation
* Enumeration
* System Auditing
* Incident Response
* Penetration Testing

Security professionals often verify which account they currently control before performing actions on a system.

---

## Advantages / Benefits

* Fast interaction with the operating system.
* Requires minimal system resources.
* Enables automation through scripting.
* Provides direct access to system functions.
* Essential for server administration and cybersecurity operations.

---

## Key Characteristics

* Text-based interface.
* Case-sensitive commands.
* Efficient for remote administration.
* Supports automation and scripting.
* Widely used across Linux distributions.

---

## Real-World Example

During a penetration test, an attacker gains access to a Linux server through a compromised account. One of the first commands executed is:

```bash
whoami
```

This identifies the current user account and helps determine available privileges before continuing enumeration.

Similarly, the `echo` command is often used within Bash scripts to display progress messages and log information during automated security assessments.

---

## Key Notes

* The terminal is the primary interface for Linux administration.
* `echo` outputs text to the terminal.
* `whoami` displays the current logged-in user.
* Command-line skills are fundamental for cybersecurity professionals.
* Most Linux servers operate primarily through terminal access.

---

## Learning Outcome

After completing this section, I understood how to interact with a Linux system through the terminal, how to display text using the `echo` command, how to identify the current user using the `whoami` command, and why command-line proficiency is a foundational skill in cybersecurity and Linux administration.
