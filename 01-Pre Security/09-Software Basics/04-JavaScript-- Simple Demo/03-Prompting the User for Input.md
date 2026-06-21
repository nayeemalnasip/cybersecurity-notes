# JavaScript: Simple Demo

## User Input and Readline Interface

### Overview

Interactive applications require communication between the user and the program. In the Guess the Number game, the program must receive a user's guess, convert it into a numeric value, and process it accordingly.

Unlike web browsers where JavaScript interacts directly with users through web pages, Node.js applications running in the command line require a special interface to capture user input. This functionality is provided by the **readline** module.

This section demonstrates how JavaScript accepts user input, converts text into numbers, manages asynchronous execution using `await`, and safely closes resources after program execution.

---

## Main Concept

### What is User Input?

User input is any information entered by a user while a program is running.

Examples include:

* Typing a username
* Entering a password
* Providing a number
* Selecting menu options

For the Guess the Number game:

```text
User Input → Guess Number → Program Processes Input
```

Example:

```text
Take a guess: 7
```

The value `7` is initially received as text and must be converted into a number before mathematical comparisons can be performed.

---

## How It Works

### Step 1: Import Required Modules

Node.js requires external modules to interact with the keyboard and terminal.

```javascript
import * as readline from "node:readline/promises";
import { stdin as input, stdout as output } from "node:process";
```

Purpose:

| Module   | Function                  |
| -------- | ------------------------- |
| readline | Reads user input          |
| stdin    | Standard input (keyboard) |
| stdout   | Standard output (screen)  |

---

### Step 2: Create Readline Interface

A communication channel is created between the user and the application.

```javascript
const rl = readline.createInterface({ input, output });
```

This interface allows:

* Asking questions
* Receiving responses
* Waiting for user interaction

Workflow:

```text
Keyboard
    │
    ▼
stdin
    │
    ▼
readline Interface
    │
    ▼
JavaScript Program
```

---

### Step 3: Generate Secret Number

The game generates a random number.

```javascript
const secret = Math.floor(Math.random() * 20) + 1;
```

Possible values:

```text
1 - 20
```

---

### Step 4: Initialize Variables

Variables store game information.

```javascript
let tries = 0;
let guess = 0;
```

Purpose:

| Variable | Description       |
| -------- | ----------------- |
| tries    | Tracks attempts   |
| guess    | Stores user guess |

---

### Step 5: Display Instructions

The user is informed that the game has started.

```javascript
console.log("I'm thinking of a number between 1 and 20");
```

Output:

```text
I'm thinking of a number between 1 and 20
```

---

### Step 6: Prompt User for Input

The program waits for the user's response.

```javascript
const text = await rl.question("Take a guess: ");
```

Example:

```text
Take a guess: 12
```

At this stage:

```javascript
text = "12";
```

Important:

The value is stored as a **string**, not a number.

---

### Step 7: Convert Text to Number

To perform numerical comparisons, the input must be converted.

```javascript
guess = parseInt(text, 10);
```

Example:

```javascript
text = "12";
guess = 12;
```

Conversion process:

```text
"12"
 ↓
parseInt()
 ↓
12
```

---

### Step 8: Increment Attempt Counter

Each guess increases the number of attempts.

```javascript
tries = tries + 1;
```

Example:

| Previous Value | New Value |
| -------------- | --------- |
| 0              | 1         |
| 1              | 2         |
| 2              | 3         |

---

### Step 9: Close the Interface

After execution, resources should be released.

```javascript
rl.close();
```

This prevents:

* Resource leaks
* Open terminal sessions
* Unnecessary memory usage

---

## Important Components

### readline Module

Provides input/output functionality for terminal applications.

Import:

```javascript
import * as readline from "node:readline/promises";
```

Capabilities:

* Ask questions
* Receive responses
* Pause execution
* Handle user interaction

---

### stdin (Standard Input)

Represents keyboard input.

Import:

```javascript
import { stdin as input } from "node:process";
```

Examples:

```text
User Types:
7
hello
password123
```

---

### stdout (Standard Output)

Represents terminal output.

Import:

```javascript
import { stdout as output } from "node:process";
```

Example:

```javascript
console.log("Welcome");
```

Output:

```text
Welcome
```

---

### await Keyword

Pauses program execution until an operation completes.

Example:

```javascript
const text = await rl.question("Take a guess: ");
```

Without `await`:

```text
Program Continues Immediately
```

With `await`:

```text
Program Waits For User Response
```

Workflow:

```text
Question Asked
      │
      ▼
User Types Answer
      │
      ▼
Program Continues
```

---

### parseInt()

Converts strings into integers.

Syntax:

```javascript
parseInt(value, radix);
```

Examples:

```javascript
parseInt("10", 10);
```

Output:

```text
10
```

---

```javascript
parseInt("25", 10);
```

Output:

```text
25
```

---

### try / finally

Ensures resources are cleaned up properly.

Syntax:

```javascript
try {

}
finally {

}
```

Example:

```javascript
try {
    console.log("Running");
}
finally {
    rl.close();
}
```

Purpose:

* Guarantees cleanup
* Improves reliability
* Prevents resource leaks

---

## Program Execution Flow

```text
Start Program
      │
      ▼
Import Modules
      │
      ▼
Create Readline Interface
      │
      ▼
Generate Secret Number
      │
      ▼
Initialize Variables
      │
      ▼
Display Instructions
      │
      ▼
Wait For User Input
      │
      ▼
Convert Input To Number
      │
      ▼
Increase Tries
      │
      ▼
Close Interface
      │
      ▼
End Program
```

---

## Advantages / Benefits

### Readline Interface

* Enables terminal interaction.
* Supports user-driven applications.
* Easy integration with Node.js.

### await

* Simplifies asynchronous programming.
* Improves code readability.
* Prevents execution errors.

### parseInt()

* Converts user input into usable numeric data.
* Enables mathematical operations.
* Supports input validation.

### try/finally

* Ensures proper cleanup.
* Improves application stability.
* Prevents resource leakage.

---

## Key Characteristics

* Node.js does not automatically wait for user input.
* The readline module provides interactive terminal communication.
* User input is received as text.
* `parseInt()` converts text into numbers.
* `await` pauses execution until input is received.
* `stdin` handles keyboard input.
* `stdout` handles screen output.
* `rl.close()` releases resources after execution.
* `try/finally` guarantees cleanup operations.

---

## Example

### User Input Example

```javascript
const text = await rl.question("Take a guess: ");
guess = parseInt(text, 10);

tries = tries + 1;
```

User interaction:

```text
Take a guess: 15
```

Internal processing:

```text
text  = "15"
guess = 15
tries = 1
```

Program state:

```text
Secret Number = 8
Guess = 15
Attempts = 1
```

The game is now ready to compare the guess against the secret number.

---

## Key Notes

* User input is initially stored as a string.
* `parseInt()` converts text into integers.
* Node.js requires the readline module for terminal input.
* `await` pauses execution until user input is received.
* `stdin` and `stdout` manage communication between the user and the program.
* `try/finally` ensures resources are released safely.
* `rl.close()` should always be called when input operations are finished.
* Interactive applications rely heavily on input processing and validation.
* Proper input handling is a critical programming skill for software development and cybersecurity automation.

---

## Learning Outcome

After completing this section, I understood how JavaScript applications running in Node.js interact with users through the terminal. I learned how to use the readline module to capture user input, how asynchronous operations work with the `await` keyword, and how text input can be converted into numeric values using `parseInt()`. Additionally, I gained practical experience with standard input/output streams and resource management using `try/finally`, which are essential concepts for building interactive command-line applications and automation tools.
