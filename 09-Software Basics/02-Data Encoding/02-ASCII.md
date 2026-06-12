# Data Encoding

## ASCII Character Encoding

### Overview

Before modern Unicode standards existed, computers needed a universal method to represent letters, numbers, punctuation marks, and control characters using binary data. The solution was **ASCII (American Standard Code for Information Interchange)**, one of the earliest and most influential character encoding standards.

ASCII established a standardized mapping between characters and numeric values, allowing different computer systems to store, process, and display text consistently.

---

## Main Concept

### What is ASCII?

ASCII (American Standard Code for Information Interchange) is a character encoding standard introduced in 1963 that assigns numeric values to English letters, digits, punctuation symbols, and control characters.

ASCII acts as a dictionary between:

```text
Characters ↔ Numbers ↔ Binary Data
```

For example:

```text
A = 65
B = 66
C = 67
```

When a computer encounters the value:

```text
65
```

it displays:

```text
A
```

---

## How It Works

### Step 1: Character Input

A user types:

```text
A
```

---

### Step 2: ASCII Lookup

The system checks the ASCII table:

```text
A = Decimal 65
```

---

### Step 3: Convert to Binary

```text
65 = 01000001
```

---

### Step 4: Store the Data

The binary value is stored in memory or on disk.

```text
01000001
```

---

### Step 5: Display the Character

When the file is opened, the operating system reads:

```text
01000001
```

Converts it back to:

```text
65
```

Then displays:

```text
A
```

---

## Important Components

### ASCII Character Set

ASCII originally uses:

```text
7 Bits
```

This allows:

```text
2⁷ = 128 Characters
```

Range:

```text
0 – 127
```

These include:

* Uppercase letters
* Lowercase letters
* Numbers
* Symbols
* Control characters

---

### ASCII Categories

| Category           | Examples           |
| ------------------ | ------------------ |
| Uppercase Letters  | A–Z                |
| Lowercase Letters  | a–z                |
| Digits             | 0–9                |
| Symbols            | ! @ # $ %          |
| Control Characters | Enter, Tab, Delete |

---

### Common ASCII Values

#### Numbers

| Character | Decimal | Hex |
| --------- | ------- | --- |
| 0         | 48      | 30  |
| 1         | 49      | 31  |
| 2         | 50      | 32  |
| 9         | 57      | 39  |

---

#### Uppercase Letters

| Character | Decimal | Hex |
| --------- | ------- | --- |
| A         | 65      | 41  |
| B         | 66      | 42  |
| C         | 67      | 43  |
| Z         | 90      | 5A  |

---

#### Lowercase Letters

| Character | Decimal | Hex |
| --------- | ------- | --- |
| a         | 97      | 61  |
| b         | 98      | 62  |
| c         | 99      | 63  |
| z         | 122     | 7A  |

---

### Control Characters

Control characters perform actions rather than displaying symbols.

Examples:

| Character | Description |
| --------- | ----------- |
| `\n`      | New Line    |
| `\t`      | Tab         |
| DEL       | Delete      |

Example:

```text
Hello\nWorld
```

Displays as:

```text
Hello
World
```

---

## ASCII Pattern Recognition

ASCII values follow predictable sequences.

### Uppercase Letters

| Character | Hex |
| --------- | --- |
| A         | 41  |
| B         | 42  |
| C         | 43  |
| D         | 44  |

---

### Lowercase Letters

| Character | Hex |
| --------- | --- |
| a         | 61  |
| b         | 62  |
| c         | 63  |
| d         | 64  |

This pattern makes manual analysis easier during programming and forensic investigations.

---

## "TryHackMe" in ASCII

### Text Representation

Original text:

```text
TryHackMe
```

---

### Binary Representation

```text
01010100 01110010 01111001 01001000
01100001 01100011 01101011 01001101
01100101 00001010
```

---

### Hexadecimal Representation

```text
54 72 79 48 61 63 6B 4D 65 0A
```

---

### Character Breakdown

| Character | Hex |
| --------- | --- |
| T         | 54  |
| r         | 72  |
| y         | 79  |
| H         | 48  |
| a         | 61  |
| c         | 63  |
| k         | 6B  |
| M         | 4D  |
| e         | 65  |
| New Line  | 0A  |

---

## Extended ASCII and European Languages

### The Limitation of ASCII

ASCII was designed primarily for English.

It cannot properly represent characters such as:

```text
ñ
ü
ß
ł
č
ș
```

ASCII only supports:

```text
128 Characters
```

which is insufficient for many languages.

---

### Extended ASCII

Using an additional bit:

```text
8 Bits
```

provides:

```text
256 Characters
```

However, even 256 characters were not enough to support all European languages simultaneously.

---

### ISO-8859 Character Sets

To address this limitation, multiple regional encoding standards were created.

---

### ISO-8859-1 (Latin-1)

Supports Western European languages:

* English
* French
* German
* Spanish
* Portuguese
* Italian

Examples:

```text
é
ç
ñ
ü
ß
```

---

### ISO-8859-2 (Latin-2)

Supports Central and Eastern European languages:

* Polish
* Czech
* Slovak
* Hungarian
* Romanian
* Croatian

Examples:

```text
ł
ń
č
ř
ș
ț
```

---

### Encoding Mismatch Problem

If a file is saved using one encoding and opened using another:

```text
ISO-8859-1
```

Opened as:

```text
ISO-8859-2
```

the displayed characters may become corrupted.

Example:

```text
é
```

may appear as an unexpected symbol.

This phenomenon is commonly known as:

```text
Character Encoding Mismatch
```

or

```text
Mojibake
```

---

## Advantages / Benefits

* Standardized text representation.
* Allowed interoperability between computer systems.
* Simplified text storage and transmission.
* Easy conversion between text and binary data.
* Formed the foundation for modern encoding standards.
* Widely supported across early operating systems and software.

---

## Key Characteristics

* ASCII was introduced in 1963.
* Uses 7 bits.
* Supports 128 characters.
* Maps characters to numeric values.
* Includes letters, digits, symbols, and control characters.
* ASCII values follow predictable sequential patterns.
* ASCII serves as the foundation for Unicode and UTF encodings.
* Extended ASCII attempted to support additional languages.
* Regional encodings led to compatibility issues.

---

## Example

### ASCII Analysis Example

Character:

```text
b
```

ASCII Decimal:

```text
98
```

Hexadecimal:

```text
62
```

Binary:

```text
01100010
```

This conversion process is commonly used in:

* Malware analysis
* Network packet inspection
* Memory forensics
* File format analysis
* Reverse engineering

---

## Key Notes

* ASCII stands for American Standard Code for Information Interchange.
* ASCII uses 7 bits and supports 128 characters.
* Every character has a unique numeric value.
* Letters, numbers, and symbols are stored as binary data.
* Hexadecimal notation is commonly used to display ASCII values.
* ASCII primarily supports English text.
* Extended ASCII attempted to support additional languages.
* ISO-8859 standards expanded support for European languages.
* Encoding mismatches can cause corrupted text display.
* ASCII remains the foundation of modern text encoding systems.

---

## Learning Outcome

After completing this section, I understood how ASCII encoding maps characters to numeric values and how computers store text as binary data. I learned how ASCII represents letters, digits, symbols, and control characters, how text such as "TryHackMe" is stored in binary and hexadecimal form, and why extended encoding standards were developed to support additional languages. I also gained an understanding of encoding mismatch issues and their impact on text interpretation across different systems.
