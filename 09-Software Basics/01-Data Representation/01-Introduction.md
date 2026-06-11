# Numbers and Colors

## Introduction to Computer Representation

### Overview

Computers process, store, and transmit information using only two states: **0** and **1**. Unlike humans, who naturally use the decimal number system (0–9), computers rely on the **binary number system** to represent all forms of data, including numbers, text, images, colors, audio, and videos.

Understanding how computers represent information is a fundamental skill in computer science, networking, programming, and cyber security. This knowledge helps security professionals analyze memory, inspect network traffic, understand file structures, and interpret hexadecimal values commonly encountered during penetration testing and digital forensics.

---

## Main Concept

### What is Computer Data Representation?

Computer data representation is the method by which computers store and process information using binary digits (bits).

Since electronic devices can easily distinguish between two states (such as ON/OFF or HIGH/LOW voltage), computers use:

```text
0 = OFF
1 = ON
```

Using combinations of these binary values, computers can represent:

* Numbers
* Characters
* Colors
* Images
* Audio
* Video
* Instructions

---

## How It Works

### Step 1: Binary States

A computer's hardware recognizes only two electrical states:

```text
0 → Low Voltage
1 → High Voltage
```

These states form the basis of all digital information.

### Step 2: Bits and Bytes

A binary digit is called a **bit**.

Examples:

```text
0
1
```

Eight bits together form one byte:

```text
10101010
```

### Step 3: Representing Numbers

Humans use decimal numbers:

```text
0 1 2 3 4 5 6 7 8 9
```

Computers use binary:

```text
0 1
```

Example:

| Decimal | Binary |
| ------- | ------ |
| 0       | 0000   |
| 1       | 0001   |
| 2       | 0010   |
| 3       | 0011   |
| 4       | 0100   |
| 5       | 0101   |

### Step 4: Representing Colors

Computers combine binary values to create colors.

Using combinations of:

* Red (R)
* Green (G)
* Blue (B)

Computers can display millions of different colors.

---

## Important Components

### Binary Number System

A base-2 numbering system that uses only:

```text
0
1
```

Example:

```text
Decimal: 13
Binary : 1101
```

---

### Decimal Number System

The numbering system used by humans.

Digits:

```text
0–9
```

Base:

```text
10
```

Example:

```text
239
3049
17
99
```

---

### Hexadecimal Number System

A compact representation of binary data.

Uses:

```text
0 1 2 3 4 5 6 7 8 9 A B C D E F
```

Where:

| Hex | Decimal |
| --- | ------- |
| A   | 10      |
| B   | 11      |
| C   | 12      |
| D   | 13      |
| E   | 14      |
| F   | 15      |

Example:

```text
Binary : 11111111
Hex    : FF
```

---

### Octal Number System (Optional)

A base-8 numbering system.

Digits:

```text
0 1 2 3 4 5 6 7
```

Example:

```text
Decimal: 8
Octal  : 10
```

---

### Color Representation

Computers commonly use the RGB model.

| Component | Meaning |
| --------- | ------- |
| R         | Red     |
| G         | Green   |
| B         | Blue    |

Each component can store different intensity values.

Example:

```text
Red   = 255
Green = 0
Blue  = 0
```

Produces:

```text
Pure Red
```

---

### 8-Color Representation

With only three bits:

```text
RGB
```

Each bit can be:

```text
0 or 1
```

Total colors:

```text
2³ = 8 Colors
```

Example:

| Binary | Color   |
| ------ | ------- |
| 000    | Black   |
| 001    | Blue    |
| 010    | Green   |
| 011    | Cyan    |
| 100    | Red     |
| 101    | Magenta |
| 110    | Yellow  |
| 111    | White   |

---

### 16 Million Color Representation

Modern systems typically use 24-bit color.

Each RGB component receives:

```text
8 bits
```

Possible values:

```text
0 - 255
```

Calculation:

```text
256 × 256 × 256
=
16,777,216 Colors
```

This is commonly referred to as:

```text
24-bit True Color
```

---

## Advantages / Benefits

* Efficient data storage
* Fast electronic processing
* Reliable communication between devices
* Supports complex multimedia systems
* Enables accurate color representation
* Essential for programming and cyber security
* Simplifies hardware design through binary logic

---

## Key Characteristics

* Computers operate using binary values.
* A bit is the smallest unit of data.
* Eight bits equal one byte.
* Binary is the foundation of digital systems.
* Hexadecimal provides a human-friendly representation of binary data.
* RGB is the standard color model for digital displays.
* 24-bit color supports over 16 million colors.
* Binary and hexadecimal are heavily used in cyber security tools and analysis.

---

## Example

### Binary Number Example

Convert decimal 13 into binary:

```text
13 = 8 + 4 + 1

Binary:
1101
```

### Color Example

RGB Value:

```text
RGB(255, 0, 255)
```

Produces:

```text
Magenta (Purple)
```

Hexadecimal representation:

```text
#FF00FF
```

---

## Key Notes

* Binary uses only 0 and 1.
* Decimal uses digits 0–9.
* Hexadecimal uses digits 0–9 and A–F.
* One byte contains 8 bits.
* RGB stands for Red, Green, Blue.
* 3-bit RGB creates 8 colors.
* 24-bit RGB creates 16,777,216 colors.
* Hexadecimal is commonly used in memory analysis, networking, and cyber security.
* Understanding binary and hexadecimal is essential for penetration testing and digital forensics.

---

## Learning Outcome

After completing this section, I understood how computers represent data using binary values, how decimal, binary, hexadecimal, and octal number systems relate to one another, and how colors are stored using RGB values. I also learned why binary and hexadecimal representations are fundamental concepts in computer systems, networking, programming, digital forensics, and cyber security operations.
