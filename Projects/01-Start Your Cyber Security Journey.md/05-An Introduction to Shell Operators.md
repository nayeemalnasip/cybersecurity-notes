# Linux Fundamentals Part 1 — Project Report

## Objective

The objective of this task was to understand Linux shell operators and how they can be used to control command execution, manage output, and improve workflow efficiency in terminal-based environments.

---

## Tasks Completed

### Challenge 1

**Question:**

If we wanted to run a command in the background, what operator would we want to use?

**Answer:**

```text id="h8q1lw"
&
```

---

### Challenge 2

**Question:**

If I wanted to replace the contents of a file named "passwords" with the word "password123", what would my command be?

**Answer:**

```bash id="d9p3ms"
echo password123 > passwords
```

---

### Challenge 3

**Question:**

Now if I wanted to add "tryhackme" to this file named "passwords" but also keep "passwords123", what would my command be?

**Answer:**

```bash id="f1r7kq"
echo tryhackme >> passwords
```

---

## Skills Practiced

* Shell Operator Usage
* Command Chaining
* Output Redirection
* Background Process Execution
* Bash Scripting Fundamentals
* Linux Workflow Optimization

---

## Key Concepts Learned

* `&` runs processes in the background.
* `&&` allows conditional command execution.
* `>` overwrites file contents with new output.
* `>>` appends output without deleting existing data.
* Shell operators are essential for automation and scripting.
* Proper use of operators improves efficiency in Linux environments.

---

## Tools Used

* Linux Terminal
* Bash Shell
* echo
* cat

---

## Conclusion

This task introduced essential Linux shell operators used for controlling command execution and handling output. Understanding these operators is critical for writing efficient scripts, automating tasks, and performing cybersecurity operations such as enumeration, logging, and system analysis.
