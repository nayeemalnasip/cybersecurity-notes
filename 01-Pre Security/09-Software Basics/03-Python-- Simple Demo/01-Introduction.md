# Python Basics

## Introduction to Python Programming

### Overview

Python is one of the most popular and beginner-friendly programming languages used in modern computing. It is a **high-level, general-purpose programming language** that allows developers to write readable and efficient code without worrying about many low-level hardware details.

Python is widely used in:

* Cybersecurity
* Automation
* Web Development
* Data Science
* Artificial Intelligence
* Machine Learning
* Cloud Computing
* Digital Forensics

In this room, Python is introduced through a simple **"Guess the Number"** game that demonstrates core programming concepts such as variables, user input, conditional statements, and loops.

---

## Main Concept

### What is Python?

Python is an interpreted, high-level programming language designed to emphasize code readability and simplicity.

Unlike low-level languages that require direct memory and hardware management, Python allows programmers to focus on solving problems through logical instructions.

Example:

```python
print("Hello, World!")
```

Output:

```text
Hello, World!
```

---

## How It Works

### The "Guess the Number" Program Workflow

The game follows a simple sequence:

### Step 1: Computer Selects a Secret Number

The program generates a random number between:

```text
1 - 20
```

Example:

```python
secret_number = 8
```

(The user does not know this value.)

---

### Step 2: User Enters a Guess

The program asks the user for input.

Example:

```python
guess = input("Take a guess: ")
```

User enters:

```text
10
```

---

### Step 3: Program Compares Values

The entered value is compared against the secret number.

Example:

```python
if guess > secret_number:
```

---

### Step 4: Feedback is Displayed

If the guess is incorrect:

```text
Too high, try again.
```

or

```text
Too low, try again.
```

---

### Step 5: Loop Continues

The program repeatedly asks for guesses until the correct number is entered.

---

### Step 6: User Wins

When the guess matches the secret number:

```text
You got it in 4 tries!
```

The game ends.

---

## Important Components

### High-Level Language

A high-level language abstracts complex hardware operations and provides easy-to-read syntax.

Example:

```python
print("Welcome")
```

Advantages:

* Easier to learn
* Faster development
* Improved readability

---

### General-Purpose Language

Python can be used across multiple domains.

| Area            | Usage                        |
| --------------- | ---------------------------- |
| Cybersecurity   | Automation, Pentesting Tools |
| Web Development | Websites & APIs              |
| Data Science    | Data Analysis                |
| AI/ML           | Machine Learning Models      |
| Networking      | Network Automation           |
| Forensics       | Evidence Processing          |

---

### Variables

Variables store data in memory.

Example:

```python
secret_number = 8
```

Here:

```text
secret_number
```

is the variable name.

```text
8
```

is the stored value.

---

### User Input

Python allows interaction with users through input.

Example:

```python
guess = input("Take a guess: ")
```

Output:

```text
Take a guess:
```

The user's response is stored in the variable.

---

### Conditional Statements

Conditional statements allow decisions to be made.

Example:

```python
if guess > secret_number:
    print("Too high")
```

---

### Common Conditional Operators

| Operator | Meaning               |
| -------- | --------------------- |
| ==       | Equal To              |
| !=       | Not Equal To          |
| >        | Greater Than          |
| <        | Less Than             |
| >=       | Greater Than or Equal |
| <=       | Less Than or Equal    |

Example:

```python
if guess == secret_number:
    print("Correct!")
```

---

### Loops

Loops allow code to repeat until a condition is met.

Example:

```python
while guess != secret_number:
```

The loop continues until the correct answer is entered.

---

### Random Number Generation

Games often require unpredictable values.

Example:

```python
import random

secret_number = random.randint(1,20)
```

This generates a random number between:

```text
1 and 20
```

---

## Advantages / Benefits

* Simple syntax and readability.
* Excellent for beginners.
* Cross-platform compatibility.
* Extensive libraries and frameworks.
* Strong community support.
* Rapid application development.
* Widely used in cybersecurity automation.
* Ideal for scripting and tool development.

---

## Key Characteristics

* Python is a high-level language.
* Python is interpreted rather than compiled.
* Supports multiple programming paradigms.
* Easy-to-read syntax.
* Strong support for automation.
* Frequently used in cybersecurity.
* Suitable for both small scripts and large applications.
* Provides powerful built-in libraries.

---

## Example

### Guess the Number Program Logic

```python
import random

secret_number = random.randint(1,20)

while True:
    guess = int(input("Take a guess: "))

    if guess < secret_number:
        print("Too low, try again.")

    elif guess > secret_number:
        print("Too high, try again.")

    else:
        print("You got it!")
        break
```

Example Output:

```text
Take a guess: 10
Too high, try again.

Take a guess: 5
Too low, try again.

Take a guess: 8
You got it!
```

---

## Key Notes

* Python is a high-level, general-purpose programming language.
* Variables store data values.
* User input enables interaction with programs.
* Conditional statements allow decision-making.
* Loops enable repeated execution of code.
* Random number generation is commonly used in games and simulations.
* Python is widely used in cybersecurity automation and scripting.
* Understanding variables, conditions, and loops forms the foundation of programming.

---

## Learning Outcome

After completing this section, I understood the purpose of Python as a high-level, general-purpose programming language and how it is used to solve real-world problems through logical instructions. I learned how variables store data, how user input allows interaction, how conditional statements control program flow, and how loops enable repeated execution of tasks. Through the "Guess the Number" game, I gained practical insight into the core programming concepts that form the foundation for automation, scripting, cybersecurity tools, and software development.
