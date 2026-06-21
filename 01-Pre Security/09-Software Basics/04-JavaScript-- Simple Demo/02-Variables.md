# JavaScript: Simple Demo

## Variables and Constants in JavaScript

### Overview

Variables and constants are fundamental building blocks in programming. They allow programs to store, retrieve, and manipulate data during execution. In JavaScript, variables are declared using the `let` keyword, while constants are declared using the `const` keyword.

In the Guess the Number game, variables are used to track user input and attempts, while a constant stores the randomly generated secret number that remains unchanged throughout the game.

---

## Main Concept

### What are Variables?

A variable is a named storage location in memory that holds data which can change during program execution.

Variables allow a program to:

* Store user input
* Track values
* Perform calculations
* Control program behavior

### Variable Declaration

JavaScript uses the `let` keyword to declare variables.

```javascript
let tries = 0;
let guess = 0;
```

In this example:

* `tries` stores the number of attempts made by the user.
* `guess` stores the user's current guess.

---

### What are Constants?

A constant is a value that cannot be modified after it has been assigned.

JavaScript uses the `const` keyword to declare constants.

```javascript
const secret = 12;
```

Once assigned, the value of `secret` cannot be changed.

---

## How It Works

### Step 1: Initialize Variables

The game starts by creating variables to track attempts and guesses.

```javascript
let tries = 0;
let guess = 0;
```

Initial values:

| Variable | Value | Purpose                   |
| -------- | ----- | ------------------------- |
| tries    | 0     | Tracks number of attempts |
| guess    | 0     | Stores user's guess       |

---

### Step 2: Generate a Random Secret Number

The game generates a random number between 1 and 20.

```javascript
const secret = Math.floor(Math.random() * 20) + 1;
```

Execution process:

```text
Math.random()
      ↓
0.0000 - 0.9999
      ↓
× 20
      ↓
0.0000 - 19.9999
      ↓
Math.floor()
      ↓
0 - 19
      ↓
+1
      ↓
1 - 20
```

---

### Step 3: Display Information

The game informs the user that a secret number has been selected.

```javascript
console.log("I'm thinking of a number between 1 and 20");
```

Output:

```text
I'm thinking of a number between 1 and 20
```

---

## Important Components

### let Keyword

Used when the value may change during execution.

Example:

```javascript
let score = 0;

score = score + 1;
```

Updated value:

```text
1
```

---

### const Keyword

Used when the value should remain fixed.

Example:

```javascript
const MAX_USERS = 100;
```

Attempting to modify:

```javascript
MAX_USERS = 200;
```

Results in:

```text
TypeError
```

---

### Math.random()

Generates a random decimal number.

Example:

```javascript
Math.random();
```

Possible outputs:

```text
0.12345
0.89231
0.45112
```

Range:

```text
0 ≤ value < 1
```

---

### Math.floor()

Rounds a decimal number down to the nearest integer.

Example:

```javascript
Math.floor(7.99);
```

Output:

```text
7
```

---

### console.log()

Displays output to the terminal or browser console.

Example:

```javascript
console.log("Hello World");
```

Output:

```text
Hello World
```

---

### Node.js Execution

JavaScript files can be executed using Node.js.

Command:

```bash
node demo.js
```

Example:

```bash
node guess_v1.js
```

---

### Browser Execution

JavaScript can also run inside web browsers.

Common Developer Tool Shortcut:

| Browser | Shortcut |
| ------- | -------- |
| Chrome  | F12      |
| Firefox | F12      |
| Edge    | F12      |

After opening Developer Tools:

```javascript
console.log("Testing JavaScript");
```

Output appears in the Console tab.

---

## Variable vs Constant Comparison

| Feature              | Variable (`let`)     | Constant (`const`)   |
| -------------------- | -------------------- | -------------------- |
| Value Can Change     | Yes                  | No                   |
| Memory Allocation    | Dynamic              | Fixed                |
| Used For             | User Input, Counters | Configuration Values |
| Reassignment Allowed | Yes                  | No                   |

Example:

```javascript
let guess = 5;
guess = 10;
```

Valid.

```javascript
const secret = 12;
secret = 15;
```

Invalid.

---

## Advantages / Benefits

### Variables

* Store dynamic information.
* Track program state.
* Enable calculations.
* Allow user interaction.

### Constants

* Prevent accidental modification.
* Improve code reliability.
* Enhance readability.
* Reduce programming errors.

### Node.js

* Runs JavaScript outside browsers.
* Simplifies testing and development.
* Supports server-side applications.

---

## Key Characteristics

* Variables use `let`.
* Constants use `const`.
* `Math.random()` generates randomness.
* `Math.floor()` removes decimal values.
* `console.log()` prints output.
* Node.js executes JavaScript from the terminal.
* Constants cannot be reassigned.
* Variables can be updated multiple times.

---

## Example

### Guess the Number Initialization

```javascript
let tries = 0;
let guess = 0;

const secret = Math.floor(Math.random() * 20) + 1;

console.log("I'm thinking of a number between 1 and 20");
```

Possible output:

```text
I'm thinking of a number between 1 and 20
```

Behind the scenes:

```text
Secret Number: 14
Tries: 0
Guess: 0
```

The user does not see the secret number, but the program stores it internally.

---

## Key Notes

* Variables store values that may change during execution.
* Constants store values that remain fixed.
* JavaScript uses `let` and `const` for declarations.
* `Math.random()` is commonly used for random number generation.
* `Math.floor()` converts decimal values to integers.
* `console.log()` is used for output.
* Node.js allows JavaScript programs to run from the command line.
* Variables and constants form the foundation of most JavaScript programs.
* Proper use of `const` improves code safety and maintainability.

---

## Learning Outcome

After completing this section, I understood how JavaScript stores and manages data using variables and constants. I learned the difference between mutable values declared with `let` and immutable values declared with `const`. I also explored how JavaScript generates random numbers using `Math.random()`, converts values using `Math.floor()`, and displays information through `console.log()`. Additionally, I gained practical experience running JavaScript programs using Node.js, which provides the foundation for building interactive applications and automation scripts.
