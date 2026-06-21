# JavaScript Essentials — Study Note

## Iterations and While Loops

### Overview

Iteration is a fundamental programming concept that allows a program to repeat a set of instructions multiple times. Instead of executing code only once, loops enable programs to continue running until a specific condition is met.

In the Number Guessing Game, a loop allows the user to make multiple guesses until the correct secret number is found, creating a more interactive and practical application.

---

## Main Concept

### What is it?

A loop is a control structure that repeatedly executes a block of code while a specified condition remains true.

In JavaScript, the `while` loop is commonly used when the number of repetitions is unknown beforehand.

```javascript
while (condition) {
    // code to repeat
}
```

The loop continues executing as long as the condition evaluates to `true`.

---

## How It Works

### Step 1: Initialize Variables

The program creates:

```javascript
const secret = Math.floor(Math.random() * 20) + 1;
let tries = 0;
let guess = 0;
```

* `secret` stores the random number.
* `tries` counts attempts.
* `guess` stores the user's input.

---

### Step 2: Display Introduction Message

```javascript
console.log("I'm thinking of a number between 1 and 20");
```

This informs the user about the guessing range.

---

### Step 3: Start the While Loop

```javascript
while (guess !== secret)
```

The loop continues as long as:

```javascript
guess is NOT equal to secret
```

The operator:

```javascript
!==
```

means:

```text
Not Equal To
```

---

### Step 4: Ask for User Input

```javascript
const text = await rl.question("Take a guess: ");
```

The program waits for the user's response.

---

### Step 5: Convert Text to Number

```javascript
guess = parseInt(text, 10);
```

Example:

```text
Input: "12"
Output: 12
```

---

### Step 6: Increase Attempt Counter

```javascript
tries = tries + 1;
```

Every guess increases the total attempt count.

---

### Step 7: Evaluate the Guess

The program checks:

```javascript
if (guess < 1 || guess > 20)
```

If invalid:

```text
That number is out of range.
```

---

If too low:

```javascript
else if (guess < secret)
```

Output:

```text
Too low, try again.
```

---

If too high:

```javascript
else if (guess > secret)
```

Output:

```text
Too high, try again.
```

---

If correct:

```javascript
else
```

Output:

```javascript
console.log("You got it in", tries, "tries!");
```

---

### Step 8: Loop Terminates

When:

```javascript
guess === secret
```

The loop condition becomes false.

```javascript
while (guess !== secret)
```

No longer evaluates to true, so execution exits the loop.

---

## Important Components

### While Loop

Repeats code while a condition remains true.

```javascript
while (condition) {
    // repeated code
}
```

---

### Not Equal Operator (`!==`)

Checks whether two values are different.

```javascript
guess !== secret
```

Examples:

```javascript
5 !== 10   // true
10 !== 10  // false
```

---

### Loop Condition

Determines whether another iteration should occur.

```javascript
while (guess !== secret)
```

---

### User Input

```javascript
const text = await rl.question("Take a guess: ");
```

Accepts data from the terminal.

---

### Number Conversion

```javascript
guess = parseInt(text, 10);
```

Converts user input into an integer.

---

### Attempt Tracking

```javascript
tries = tries + 1;
```

Records the number of guesses.

---

### Conditional Feedback

Provides hints using:

```javascript
if
else if
else
```

This improves the user's experience by guiding future guesses.

---

## Advantages / Benefits

* Allows repeated execution of code.
* Improves user interaction.
* Eliminates repetitive coding.
* Supports dynamic program behavior.
* Enables games and interactive applications.
* Makes applications more practical and user-friendly.

---

## Key Characteristics

* Executes repeatedly until a condition becomes false.
* Uses Boolean expressions for control.
* Can run indefinitely if conditions never change.
* Commonly used for user input validation.
* Frequently combined with conditional statements.
* Essential for automation and interactive programming.

---

## Example

### Example Execution

```text
I'm thinking of a number between 1 and 20

Take a guess: 10
Too low, try again.

Take a guess: 15
Too high, try again.

Take a guess: 13
Too low, try again.

Take a guess: 14
You got it in 4 tries!
```

---

### Loop Flow Example

```text
Start Program
      ↓
Generate Secret Number
      ↓
Ask for Guess
      ↓
Compare Guess
      ↓
Correct?
 ┌────┴────┐
 No       Yes
 │          │
Give Hint  Display Success
 │          │
 └──Repeat──┘
```

---

## Key Notes

* `while` loops repeat code until a condition becomes false.
* `!==` means "not equal".
* The loop allows unlimited guesses until success.
* User input is collected on every iteration.
* The attempt counter tracks all guesses.
* Conditional statements provide feedback after each attempt.
* This version is significantly more interactive than the previous single-attempt version.
* Proper loop conditions are essential to avoid infinite loops.

---

## Learning Outcome

After completing this section, I understood how iteration works in JavaScript using the `while` loop. I learned how loops repeatedly execute code until a specified condition becomes false and how user input can be continuously processed within a loop. I also gained practical experience combining loops with conditional statements to build an interactive number-guessing game that accepts multiple attempts, validates input, tracks guesses, and provides real-time feedback to the user.

---

# JavaScript Essentials — Project Report

## Objective

The objective of this section was to understand iteration and looping mechanisms in JavaScript by implementing a `while` loop that repeatedly prompts the user for guesses until the correct secret number is identified. The exercise also reinforced concepts related to user input handling, conditional evaluation, and program flow control.

---

## Tasks Completed

### Challenge 1

**Question:**

How can the guessing game continue running until the user correctly guesses the secret number?

**Answer:**

```javascript
while (guess !== secret) {
    // repeat until correct guess
}
```

---

### Challenge 2

**Question:**

What operator is used to determine whether two values are not equal?

**Answer:**

```javascript
!==
```

Example:

```javascript
5 !== 10   // true
10 !== 10  // false
```

---

### Challenge 3

**Question:**

What operations are repeated inside the loop?

**Answer:**

```text
1. Prompt the user for a guess.
2. Convert input text into a number.
3. Increment the attempt counter.
4. Validate the input range.
5. Compare the guess against the secret number.
6. Display feedback.
7. Repeat until the correct number is guessed.
```

---

### Challenge 4

**Question:**

How does the completed guessing game function?

**Answer:**

```text
The program generates a random secret number,
continuously accepts user guesses,
provides feedback after each attempt,
tracks the number of tries,
and terminates only when the user correctly
guesses the secret number.
```

---

## Skills Practiced

* JavaScript While Loops
* Iteration and Repetition
* User Input Handling
* Input Validation
* Conditional Statements
* Comparison Operators
* Loop Control Logic
* Random Number Generation
* Interactive Program Development
* Terminal-Based Application Design

---

## Key Concepts Learned

* While Loop
* Loop Conditions
* Not Equal Operator (`!==`)
* Repetitive Program Execution
* User Interaction
* Input Processing
* Conditional Logic
* Attempt Tracking
* Program Flow Control
* Interactive Game Logic

---

## Conclusion

Through this section, I gained practical experience implementing iteration in JavaScript using the `while` loop. I learned how loops can repeatedly execute code based on a condition and how they are used to create interactive applications that continuously accept user input. By integrating loops with conditional statements and input validation, I successfully understood how to build a functional number-guessing game that provides feedback, tracks attempts, and continues running until the correct answer is found.
