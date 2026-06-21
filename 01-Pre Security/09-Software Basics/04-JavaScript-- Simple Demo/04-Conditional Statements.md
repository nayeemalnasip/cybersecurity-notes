# JavaScript Essentials — Study Note

## Conditional Statements and Decision Making

### Overview

Conditional statements are one of the most important programming concepts. They allow a program to make decisions based on user input or specific conditions.

In the Number Guessing Game, conditional statements are used to compare the user's guess with the secret number and provide appropriate feedback. This makes the program interactive and improves the user experience.

---

## Main Concept

### What is it?

A conditional statement is a programming structure that executes different blocks of code depending on whether a condition evaluates to `true` or `false`.

JavaScript commonly uses:

```javascript
if
else if
else
```

These statements help control program flow and enable decision-making logic.

---

## How It Works

The guessing game follows a sequence of logical checks:

### Step 1: Validate Input Range

The program first checks whether the user's guess is within the allowed range.

```javascript
if (guess < 1 || guess > 20)
```

If the number is less than 1 or greater than 20:

```javascript
console.log("That number is out of range. Try again.");
```

---

### Step 2: Check if Guess is Too Low

If the first condition is false, the program checks:

```javascript
else if (guess < secret)
```

If true:

```javascript
console.log("Too low, try again.");
```

---

### Step 3: Check if Guess is Too High

If the previous conditions are false:

```javascript
else if (guess > secret)
```

If true:

```javascript
console.log("Too high, try again.");
```

---

### Step 4: Correct Guess

If none of the previous conditions are true:

```javascript
else
```

This means:

```javascript
guess === secret
```

The user successfully guessed the secret number.

```javascript
console.log("You got it in", tries, "tries!");
```

---

## Important Components

### Logical OR Operator (`||`)

Used when either condition can be true.

```javascript
guess < 1 || guess > 20
```

Meaning:

```text
Guess is less than 1 OR greater than 20
```

---

### if Statement

Executes code when a condition is true.

```javascript
if (condition) {
    // code
}
```

---

### else if Statement

Checks another condition if the previous one was false.

```javascript
else if (condition) {
    // code
}
```

---

### else Statement

Runs when all previous conditions are false.

```javascript
else {
    // code
}
```

---

### Random Number Generation

Creates a secret number between 1 and 20.

```javascript
const secret =
Math.floor(Math.random() * 20) + 1;
```

Example:

```text
1 ≤ secret ≤ 20
```

---

### User Input

Collects user input from the terminal.

```javascript
const text = await rl.question("Take a guess: ");
```

---

### String to Integer Conversion

Converts text input into a number.

```javascript
guess = parseInt(text, 10);
```

Example:

```text
Input: "15"
Output: 15
```

---

### Tracking Attempts

Counts the number of guesses made.

```javascript
tries = tries + 1;
```

---

## Advantages / Benefits

* Enables decision-making in programs.
* Improves user interaction.
* Provides meaningful feedback.
* Prevents invalid inputs.
* Creates dynamic application behavior.
* Forms the foundation of game logic and automation.

---

## Key Characteristics

* Conditions evaluate to either `true` or `false`.
* Only one matching condition executes.
* `else if` creates multiple decision paths.
* `else` acts as the default action.
* Conditions are evaluated from top to bottom.
* Logical operators can combine multiple conditions.

---

## Example

### User Enters an Invalid Number

```text
Take a guess: 25
That number is out of range. Try again.
```

---

### User Guesses Too Low

```text
Take a guess: 5
Too low, try again.
```

---

### User Guesses Too High

```text
Take a guess: 18
Too high, try again.
```

---

### User Guesses Correctly

```text
Take a guess: 12
You got it in 1 tries!
```

---

## Key Notes

* `if` checks the first condition.
* `else if` checks additional conditions.
* `else` handles all remaining cases.
* `||` means logical OR.
* User input is received as text and must be converted to a number.
* The secret number is generated randomly.
* The current version of the game only allows one guess.
* A loop will be needed in the next version to allow multiple attempts.

---

## Learning Outcome

After completing this section, I understood how conditional statements are used in JavaScript to control program flow and make decisions based on user input. I learned how `if`, `else if`, and `else` statements evaluate conditions, how logical operators such as `||` are used, and how user guesses can be compared against a secret value to provide meaningful feedback. I also gained practical knowledge of input validation, comparison operators, and interactive application logic used in real-world software development.

---

# JavaScript Essentials — Project Report

## Objective

The objective of this section was to understand how conditional statements work in JavaScript and how they can be used to evaluate user input, validate data, compare values, and provide feedback in an interactive number-guessing game.

---

## Tasks Completed

### Challenge 1

**Question:**

How can a program determine whether a user's guess is valid, too low, too high, or correct?

**Answer:**

```javascript
if (guess < 1 || guess > 20) {
    console.log("That number is out of range. Try again.");
} else if (guess < secret) {
    console.log("Too low, try again.");
} else if (guess > secret) {
    console.log("Too high, try again.");
} else {
    console.log("You got it in", tries, "tries!");
}
```

---

### Challenge 2

**Question:**

How does the updated guessing game process user input?

**Answer:**

```text
1. Generate a random secret number between 1 and 20.
2. Prompt the user for a guess.
3. Convert the input text into a number.
4. Increment the attempt counter.
5. Validate the input range.
6. Compare the guess with the secret number.
7. Display appropriate feedback.
```

---

### Challenge 3

**Question:**

What limitation still exists in the current version of the game?

**Answer:**

```text
The program only allows a single guess before terminating.
A loop mechanism has not yet been implemented to allow
multiple attempts until the correct number is guessed.
```

---

## Skills Practiced

* JavaScript Conditional Statements
* Decision-Making Logic
* Input Validation
* Comparison Operators
* Logical Operators
* User Input Handling
* Random Number Generation
* Interactive Program Development
* Debugging Program Flow
* Terminal-Based Application Development

---

## Key Concepts Learned

* if Statements
* else if Statements
* else Statements
* Logical OR Operator (`||`)
* Comparison Operators (`<`, `>`)
* User Input Processing
* Number Conversion using `parseInt()`
* Random Number Generation with `Math.random()`
* Conditional Execution Flow
* Interactive Feedback Systems

---

## Conclusion

Through this section, I gained practical experience using JavaScript conditional statements to control application behavior and respond dynamically to user input. I learned how to validate user entries, compare values using decision-making logic, and provide meaningful feedback based on different conditions. This exercise strengthened my understanding of program flow control and prepared me for implementing loops and more advanced game logic in subsequent tasks.
