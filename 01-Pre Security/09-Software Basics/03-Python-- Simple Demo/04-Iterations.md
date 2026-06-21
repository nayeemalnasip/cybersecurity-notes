# Python Basics

## Iterations (Loops)

### Overview

Iteration is a fundamental programming concept that allows a program to repeatedly execute a block of code until a specified condition is met. Without loops, developers would need to manually duplicate the same code multiple times, making programs inefficient and difficult to maintain.

In the **Guess the Number** game, iteration allows the user to continue making guesses until the correct number is found. This transforms the program from a single-attempt demonstration into a fully functional interactive game.

Loops are widely used in software development, automation, cybersecurity, system administration, data processing, and artificial intelligence because they enable computers to perform repetitive tasks efficiently.

---

## Main Concept

### What is Iteration?

Iteration is the process of repeatedly executing a block of code while a condition remains true.

A loop continues running until its stopping condition becomes false.

Think of iteration as performing the same action repeatedly until a goal is achieved.

### Real-World Examples

#### Finding a Parking Space

```text
Check Parking Spot 1
↓
Available?
↓ No

Check Parking Spot 2
↓
Available?
↓ No

Check Parking Spot 3
↓
Available?
↓ Yes

Park Vehicle
Stop Searching
```

---

#### Shopping for a T-Shirt

```text
Visit Shop 1
↓
Suitable?
↓ No

Visit Shop 2
↓
Suitable?
↓ No

Visit Shop 3
↓
Suitable?
↓ Yes

Purchase T-Shirt
Stop Searching
```

---

#### Guess the Number Game

```text
Enter Guess
↓
Correct?
↓ No

Try Again
↓
Enter Guess
↓
Correct?
↓ No

Try Again
↓
Enter Guess
↓
Correct?
↓ Yes

Game Ends
```

---

## How Iteration Works

### Step-by-Step Process

1. The computer generates a secret number.
2. The user enters a guess.
3. The program compares the guess with the secret number.
4. If the guess is incorrect:

   * Provide a hint.
   * Ask for another guess.
5. Repeat until the correct number is entered.
6. Display the success message.
7. Terminate the program.

---

## The While Loop

Python uses the `while` loop to repeat code while a condition remains true.

### Syntax

```python
while condition:
    statements
```

The condition is checked before every iteration.

If the condition is:

```text
True
```

The loop continues.

If the condition becomes:

```text
False
```

The loop stops.

---

## While Loop Used in the Game

```python
while guess != secret:
```

This statement means:

```text
Continue looping while
guess is NOT equal to secret
```

---

### Understanding the Condition

The operator:

```python
!=
```

means:

```text
Not Equal To
```

Examples:

```python
5 != 10
```

Result:

```text
True
```

---

```python
10 != 10
```

Result:

```text
False
```

---

## Loop Execution Flow

### Initial State

```python
secret = 10
guess = 0
```

Condition:

```python
guess != secret
```

Evaluation:

```python
0 != 10
```

Result:

```text
True
```

The loop starts.

---

### First Guess

User enters:

```python
5
```

Condition:

```python
5 != 10
```

Result:

```text
True
```

The loop continues.

---

### Second Guess

User enters:

```python
8
```

Condition:

```python
8 != 10
```

Result:

```text
True
```

The loop continues.

---

### Correct Guess

User enters:

```python
10
```

Condition:

```python
10 != 10
```

Result:

```text
False
```

The loop terminates.

---

## Complete Loop Block

```python
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

## Important Components

### 1. Loop Condition

Controls whether the loop continues.

```python
while guess != secret:
```

Purpose:

```text
Keep asking for guesses until the correct answer is entered.
```

---

### 2. User Input

Receives data from the user.

```python
text = input("Take a guess: ")
```

Example:

```text
Take a guess: 7
```

---

### 3. Type Conversion

Converts text input into an integer.

```python
guess = int(text)
```

Example:

```python
"7" → 7
```

---

### 4. Counter Variable

Tracks the number of attempts.

```python
tries = tries + 1
```

Example:

```text
Guess 1 → tries = 1
Guess 2 → tries = 2
Guess 3 → tries = 3
```

---

### 5. Conditional Logic

Provides feedback to the user.

```python
if guess < secret:
```

Output:

```text
Too low
```

---

```python
elif guess > secret:
```

Output:

```text
Too high
```

---

```python
else:
```

Output:

```text
Correct
```

---

## Program Structure (Version 3)

```python
import random

# ----------------------------
# Guess the Number (Beginner Demo)
# ----------------------------

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

## Program Flow Diagram

```text
Start Program
      │
      ▼
Generate Secret Number
      │
      ▼
Display Welcome Message
      │
      ▼
Enter While Loop
      │
      ▼
Ask User For Guess
      │
      ▼
Increment Tries Counter
      │
      ▼
Compare Guess
      │
 ┌────┼─────┐
 │    │     │
 ▼    ▼     ▼
Low High Correct
 │    │      │
 ▼    ▼      ▼
Hint Hint Success
 │    │
 └────┘
      │
      ▼
Repeat Loop
```

---

## Infinite Loop Concept

A loop becomes infinite when its condition never becomes false.

Example:

```python
while True:
    print("Running...")
```

Output:

```text
Running...
Running...
Running...
Running...
```

The loop never ends.

---

### Why Our Program Does Not Create an Infinite Loop

Because eventually:

```python
guess == secret
```

When this happens:

```python
guess != secret
```

becomes:

```python
False
```

The loop exits safely.

---

## Cybersecurity Relevance

Iterations are extremely important in cybersecurity and automation.

### Password Auditing

```python
for password in wordlist:
    test_password(password)
```

The loop tests many passwords automatically.

---

### Port Scanning

```python
for port in range(1, 65536):
    scan(port)
```

Checks thousands of ports sequentially.

---

### Log Analysis

```python
for line in logfile:
    analyze(line)
```

Processes large security logs.

---

### Malware Detection

```python
for file in files:
    check_hash(file)
```

Scans multiple files automatically.

---

### Vulnerability Assessment

```python
for host in network:
    perform_scan(host)
```

Examines every device on a network.

---

## Advantages / Benefits

* Eliminates repetitive code.
* Improves efficiency.
* Supports automation.
* Simplifies large-scale operations.
* Enables continuous user interaction.
* Reduces development time.
* Essential for cybersecurity scripting.
* Improves code maintainability.

---

## Key Characteristics

* Executes code repeatedly.
* Controlled by a condition.
* Stops when the condition becomes false.
* Can process large amounts of data.
* Supports automation and scalability.
* Frequently combined with conditional statements.
* Commonly used in cybersecurity tools and scripts.
* Forms the foundation of automation programming.

---

## Example

### Login Retry System

```python
password = ""

while password != "Cyber123":
    password = input("Enter Password: ")

print("Access Granted")
```

Execution:

```text
Enter Password: test
Enter Password: admin
Enter Password: Cyber123

Access Granted
```

The loop continues until the correct password is entered.

---

## Key Notes

* Iteration means repeating a block of code.
* A loop continues while its condition is True.
* `while` loops are condition-based loops.
* `!=` means "not equal to."
* The Guess the Number game uses a `while` loop for repeated attempts.
* Loops are commonly combined with variables and conditional statements.
* Counter variables help track repetitions.
* Infinite loops occur when conditions never become False.
* Iteration is essential for automation and cybersecurity scripting.
* Mastering loops is a prerequisite for advanced Python programming.

---

## Learning Outcome

After completing this section, I understood how iteration allows a program to repeatedly execute code until a specified condition is met. I learned how Python's `while` loop works, how loop conditions control execution flow, and how variables such as counters can track repeated actions. Through the Guess the Number game, I gained practical experience combining loops with conditional statements and user input, creating a fully interactive application. I also learned how loops form the foundation of automation tasks commonly used in cybersecurity, including log analysis, vulnerability scanning, password auditing, malware detection, and network enumeration.
