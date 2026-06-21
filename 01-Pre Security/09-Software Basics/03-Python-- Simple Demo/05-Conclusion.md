# Python Basics

## Conclusion

### Overview

This room introduced the fundamental building blocks of programming using Python through the development of a simple interactive application called **Guess the Number**. Rather than focusing solely on theory, the room demonstrated how core programming concepts work together to create a complete program that accepts user input, makes decisions, and repeatedly executes actions until a goal is achieved.

The concepts learned in this room form the foundation of nearly every modern software application, automation script, cybersecurity tool, and system administration task.

---

## Main Concepts Covered

Throughout the room, three fundamental programming concepts were explored:

### 1. Variables

Variables are containers used to store and manage data during program execution.

Examples used in the project:

```python
secret = random.randint(1, 20)
guess = 0
tries = 0
```

Purpose of each variable:

| Variable | Purpose                              |
| -------- | ------------------------------------ |
| `secret` | Stores the randomly generated number |
| `guess`  | Stores the user's current guess      |
| `tries`  | Tracks the total number of attempts  |

Variables allow programs to remember information and update values dynamically while running.

---

### 2. Conditional Statements

Conditional statements enable programs to make decisions based on specific conditions.

Python uses:

```python
if
elif
else
```

Example:

```python
if guess < secret:
    print("Too low")

elif guess > secret:
    print("Too high")

else:
    print("Correct")
```

Conditional logic allows software to:

* Validate input
* Make decisions
* Enforce security policies
* Control program flow
* Respond differently to different situations

---

### 3. Iterations (Loops)

Loops allow a program to execute code repeatedly until a condition becomes false.

Example:

```python
while guess != secret:
```

This loop continues asking for guesses until the user finds the correct number.

Loops are essential because they:

* Reduce repetitive code
* Improve efficiency
* Enable automation
* Process large amounts of data
* Support continuous interaction

---

## How the Complete Program Works

The final version of the Guess the Number game combines all concepts learned throughout the room.

### Step 1: Import Required Library

```python
import random
```

Provides access to Python's random number generator.

---

### Step 2: Create Variables

```python
secret = random.randint(1, 20)
guess = 0
tries = 0
```

Stores game information.

---

### Step 3: Display Information

```python
print("I'm thinking of a number between 1 and 20")
```

Notifies the user that the game has started.

---

### Step 4: Enter Loop

```python
while guess != secret:
```

Keeps the game running until the correct answer is found.

---

### Step 5: Accept User Input

```python
text = input("Take a guess: ")
guess = int(text)
```

Receives and converts the user's input.

---

### Step 6: Count Attempts

```python
tries = tries + 1
```

Tracks the number of guesses.

---

### Step 7: Compare Values

```python
if guess < 1 or guess > 20:
```

Checks whether the number is valid.

```python
elif guess < secret:
```

Checks whether the guess is too low.

```python
elif guess > secret:
```

Checks whether the guess is too high.

```python
else:
```

Handles the correct answer.

---

### Step 8: End Program

Once:

```python
guess == secret
```

The loop terminates and the program exits successfully.

---

## Complete Program

```python
import random

secret = random.randint(1, 20)
tries = 0
guess = 0

print("I'm thinking of a number between 1 and 20")

while guess != secret:

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

## Important Components Learned

| Component          | Purpose                                |
| ------------------ | -------------------------------------- |
| `import random`    | Imports random number functions        |
| `random.randint()` | Generates a random integer             |
| Variables          | Store program data                     |
| `input()`          | Receives user input                    |
| `int()`            | Converts text into integers            |
| `print()`          | Displays output                        |
| `if`               | Executes code when a condition is true |
| `elif`             | Checks additional conditions           |
| `else`             | Executes default code                  |
| `while`            | Repeats code until a condition changes |
| `!=`               | Not Equal comparison operator          |
| `<`                | Less Than operator                     |
| `>`                | Greater Than operator                  |
| `or`               | Logical OR operator                    |

---

## Cybersecurity Relevance

Although this room focused on a simple game, the same programming concepts are heavily used throughout cybersecurity.

### Variables

Used to store:

* IP addresses
* Usernames
* Password hashes
* Network packets
* Scan results

Example:

```python
target_ip = "192.168.1.10"
```

---

### Conditional Statements

Used in:

* Authentication systems
* Access control
* Intrusion detection
* Malware analysis
* Security monitoring

Example:

```python
if login_attempts > 5:
    lock_account()
```

---

### Loops

Used for:

* Port scanning
* Password auditing
* Log analysis
* Vulnerability scanning
* Threat hunting

Example:

```python
for port in range(1, 65536):
    scan(port)
```

---

## Advantages of Learning Python

### Beginner Friendly

Python syntax is simple and easy to read.

### Powerful Automation

Automates repetitive tasks efficiently.

### Cybersecurity Integration

Widely used in:

* Penetration Testing
* Digital Forensics
* Malware Analysis
* Threat Intelligence
* Security Automation

### Large Community Support

Extensive libraries, tutorials, and documentation are available.

### Cross-Platform Compatibility

Runs on:

* Windows
* Linux
* macOS

---

## Key Characteristics of Python

* High-level programming language
* General-purpose language
* Easy-to-read syntax
* Supports procedural programming
* Supports object-oriented programming
* Supports automation scripting
* Large ecosystem of libraries
* Widely adopted in cybersecurity and DevOps

---

## Example Real-World Cybersecurity Scenario

### Brute Force Password Testing

```python
password_found = False

while not password_found:

    password = get_next_password()

    if check_password(password):
        password_found = True
```

This uses:

* Variables
* Conditional statements
* Loops

The same three concepts learned in this room.

---

## Key Notes

* Variables store information during program execution.
* Conditional statements enable decision-making.
* Loops allow repeated execution of code.
* `if`, `elif`, and `else` control program flow.
* `while` loops repeat until a condition becomes false.
* Python is beginner-friendly yet powerful.
* The Guess the Number project combines all major concepts learned.
* Programming skills improve primarily through practice.
* These concepts apply to software development, automation, and cybersecurity.
* Variables, conditions, and loops are considered the core pillars of imperative programming.

---

## Learning Outcome

After completing this room, I gained a solid understanding of the three fundamental pillars of imperative programming: variables, conditional statements, and loops. Through the development of the Guess the Number game, I learned how to store data using variables, make decisions using `if`, `elif`, and `else` statements, and repeatedly execute code using `while` loops. I also developed an understanding of how user input, program flow, and logical conditions work together to create interactive applications. These foundational programming concepts provide the basis for more advanced Python development and are directly applicable to cybersecurity tasks such as automation, vulnerability scanning, log analysis, authentication systems, and security monitoring.
