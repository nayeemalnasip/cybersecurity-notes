# Python Basics

## Conditional Statements

### Overview

Conditional statements are one of the most important concepts in programming. They allow a program to make decisions based on specific conditions and execute different code paths depending on the outcome.

In the **Guess the Number** game, conditional statements enable the program to compare the user's guess against the secret number and provide appropriate feedback. Without conditional logic, the program would not be able to determine whether a guess is correct, too low, too high, or outside the allowed range.

Conditional statements form the foundation of:

* Decision-making systems
* Authentication mechanisms
* Security controls
* Input validation
* Access control systems
* Automated cybersecurity scripts

---

## Main Concept

### What are Conditional Statements?

A conditional statement evaluates whether a condition is **True** or **False** and executes specific code based on the result.

Think of it as asking a question:

```text
Is the user authenticated?
```

If the answer is:

```text
True
```

Grant access.

Otherwise:

```text
False
```

Deny access.

This same logic is used in Python through:

```python
if
elif
else
```

statements.

---

## How Conditional Statements Work

### Decision Flow

A Python program evaluates conditions from top to bottom.

```text
IF Condition 1 is True
        │
        ▼
 Execute Block 1

Otherwise
        │
        ▼

ELIF Condition 2 is True
        │
        ▼
 Execute Block 2

Otherwise
        │
        ▼

ELSE
        │
        ▼
 Execute Default Block
```

Only one matching block executes.

---

## Conditional Logic in the Guessing Game

The game evaluates the user's guess using four possible scenarios.

### Scenario 1: Guess is Outside Allowed Range

Condition:

```python
guess < 1 or guess > 20
```

Example:

```python
guess = 25
```

Evaluation:

```python
25 > 20
```

Result:

```text
That number is out of range. Try again.
```

---

### Scenario 2: Guess is Too Low

Condition:

```python
guess < secret
```

Example:

```python
secret = 10
guess = 5
```

Evaluation:

```python
5 < 10
```

Result:

```text
Too low, try again.
```

---

### Scenario 3: Guess is Too High

Condition:

```python
guess > secret
```

Example:

```python
secret = 10
guess = 15
```

Evaluation:

```python
15 > 10
```

Result:

```text
Too high, try again.
```

---

### Scenario 4: Correct Guess

Condition:

```python
guess == secret
```

Example:

```python
secret = 10
guess = 10
```

Result:

```text
You got it in 1 tries!
```

---

## Python Conditional Syntax

### if Statement

Executes code when a condition is true.

Syntax:

```python
if condition:
    statement
```

Example:

```python
age = 18

if age >= 18:
    print("Adult")
```

Output:

```text
Adult
```

---

### elif Statement

Checks an additional condition when the previous condition is false.

Syntax:

```python
if condition1:
    statement

elif condition2:
    statement
```

Example:

```python
score = 80

if score >= 90:
    print("A")

elif score >= 80:
    print("B")
```

Output:

```text
B
```

---

### else Statement

Executes when all previous conditions are false.

Syntax:

```python
if condition:
    statement

else:
    statement
```

Example:

```python
age = 15

if age >= 18:
    print("Adult")

else:
    print("Minor")
```

Output:

```text
Minor
```

---

## Important Components

### Comparison Operators

Comparison operators compare two values and return either:

```text
True
```

or

```text
False
```

| Operator | Meaning               | Example         |
| -------- | --------------------- | --------------- |
| ==       | Equal To              | guess == secret |
| !=       | Not Equal To          | guess != secret |
| <        | Less Than             | guess < secret  |
| >        | Greater Than          | guess > secret  |
| <=       | Less Than or Equal    | guess <= 20     |
| >=       | Greater Than or Equal | guess >= 1      |

---

### Logical Operators

Logical operators combine multiple conditions.

---

### OR Operator

Syntax:

```python
condition1 or condition2
```

Returns True if at least one condition is True.

Example:

```python
guess < 1 or guess > 20
```

Meaning:

```text
Is the guess less than 1?
OR
Is the guess greater than 20?
```

If either condition is true:

```text
Out of Range
```

---

### AND Operator

Syntax:

```python
condition1 and condition2
```

Returns True only when both conditions are True.

Example:

```python
age >= 18 and age <= 65
```

---

### NOT Operator

Syntax:

```python
not condition
```

Example:

```python
not authenticated
```

Meaning:

```text
User is NOT authenticated
```

---

## Complete Conditional Logic

```python
# Give a hint using if / elif / else.

if guess < 1 or guess > 20:
    print("That number is out of range. Try again.")

elif guess < secret:
    print("Too low, try again.")

elif guess > secret:
    print("Too high, try again.")

else:
    print("You got it in", tries, "tries!")
```

---

## Code Execution Flow

### Example 1

```python
secret = 10
guess = 30
```

Evaluation:

```python
guess > 20
```

Result:

```text
That number is out of range. Try again.
```

---

### Example 2

```python
secret = 10
guess = 5
```

Evaluation:

```python
5 < 10
```

Result:

```text
Too low, try again.
```

---

### Example 3

```python
secret = 10
guess = 15
```

Evaluation:

```python
15 > 10
```

Result:

```text
Too high, try again.
```

---

### Example 4

```python
secret = 10
guess = 10
```

Evaluation:

```python
guess == secret
```

Result:

```text
You got it in 1 tries!
```

---

## Program Structure (Version 2)

```python
import random

secret = random.randint(1, 20)
tries = 0
guess = 0

print("I'm thinking of a number between 1 and 20")

text = input("Take a guess: ")
guess = int(text)

tries = tries + 1

if guess < 1 or guess > 20:
    print("That number is out of range. Try again.")

elif guess < secret:
    print("Too low, try again.")

elif guess > secret:
    print("Too high, try again.")

else:
    print("You got it in", tries, "tries!")
```

---

## Cybersecurity Relevance

Conditional statements are heavily used in cybersecurity.

### Authentication Systems

```python
if password == stored_password:
    grant_access()
else:
    deny_access()
```

---

### Firewall Rules

```python
if source_ip in blocked_list:
    block_connection()
else:
    allow_connection()
```

---

### Login Monitoring

```python
if failed_attempts > 5:
    lock_account()
```

---

### Malware Detection

```python
if file_hash in malicious_hashes:
    quarantine_file()
```

---

## Advantages / Benefits

* Enables intelligent decision-making.
* Supports input validation.
* Prevents invalid program behavior.
* Allows dynamic program execution.
* Essential for automation.
* Improves application security.
* Forms the basis of access control and authentication systems.

---

## Key Characteristics

* Conditions evaluate to True or False.
* Python uses if, elif, and else for branching logic.
* Comparison operators compare values.
* Logical operators combine conditions.
* Conditions are evaluated sequentially.
* Only the first matching block executes.
* Indentation determines code blocks in Python.
* Conditional statements are fundamental to software and cybersecurity development.

---

## Example

### Login Verification System

```python
username = input("Username: ")
password = input("Password: ")

if username == "admin" and password == "Cyber123":
    print("Access Granted")

else:
    print("Access Denied")
```

Output:

```text
Access Granted
```

or

```text
Access Denied
```

This demonstrates the same decision-making logic used in the Guess the Number game.

---

## Key Notes

* Conditional statements control program flow.
* if executes when a condition is True.
* elif checks additional conditions.
* else executes when no conditions are True.
* Comparison operators return Boolean values.
* Logical operators combine multiple conditions.
* Conditions are evaluated from top to bottom.
* Input validation often relies on conditional logic.
* Cybersecurity tools heavily depend on decision-making structures.
* Mastering conditional statements is essential before learning loops and advanced automation.

---

## Learning Outcome

After completing this section, I gained a strong understanding of Python conditional statements and how programs make decisions using logical conditions. I learned how to use `if`, `elif`, and `else` statements to control program execution, validate user input, and compare values using comparison and logical operators. Through the Guess the Number game, I understood how branching logic provides dynamic user feedback and forms the foundation of real-world applications such as authentication systems, firewall rules, intrusion detection mechanisms, security automation scripts, and access control systems used throughout cybersecurity and software development.
