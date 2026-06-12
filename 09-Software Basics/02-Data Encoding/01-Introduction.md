# Data Encoding

## Introduction to Data Encoding

### Overview

Computers store and process all information as binary data (0s and 1s). While numbers can be represented directly using binary, text requires an additional layer that defines how numeric values correspond to characters, symbols, punctuation marks, and emojis. This mapping system is known as **data encoding**.

Data encoding enables computers to convert human-readable text into machine-readable binary data and back again. Without standardized encoding schemes, systems would be unable to correctly interpret stored or transmitted text data.

---

## Main Concept

### What is Data Encoding?

Data encoding is the process of assigning numeric values to characters, symbols, and other textual elements so that computers can store, process, and transmit them.

In simple terms:

```text
Character → Numeric Value → Binary Representation
```

Example:

```text
A → 65 → 01000001
```

When a user types text, the computer converts each character into its corresponding numeric code according to a predefined encoding standard.

---

## How It Works

### Step 1: User Enters Text

Consider the word:

```text
HELLO
```

---

### Step 2: Characters Are Converted to Numbers

Each character is assigned a unique numeric value based on an encoding standard.

Example (ASCII):

```text
H = 72
E = 69
L = 76
L = 76
O = 79
```

---

### Step 3: Numbers Are Converted to Binary

The computer stores these numeric values as binary data.

Example:

```text
H = 72 = 01001000
```

---

### Step 4: Data Is Stored or Transmitted

The binary values can now be:

* Saved to a file
* Stored in memory
* Sent across a network
* Processed by applications

---

### Step 5: Decoding

When the file is opened, the system reverses the process:

```text
Binary → Number → Character
```

Result:

```text
HELLO
```

---

## Important Components

### Data Representation vs Data Encoding

| Concept             | Description                             |
| ------------------- | --------------------------------------- |
| Data Representation | How data is physically stored as bits   |
| Data Encoding       | How numeric values are assigned meaning |

Example:

```text
01000001
```

Representation:

```text
Binary Data
```

Encoding Interpretation:

```text
ASCII → A
```

---

### Character Encoding

Character encoding defines the relationship between:

```text
Numbers ↔ Characters
```

Examples:

```text
A
B
1
!
@
😊
```

Each character has a unique code value.

---

### ASCII (American Standard Code for Information Interchange)

ASCII was one of the earliest character encoding standards.

Characteristics:

* Uses 7 bits
* Supports 128 characters
* Includes:

  * English letters
  * Numbers
  * Punctuation
  * Control characters

Examples:

| Character | Decimal | Binary   |
| --------- | ------- | -------- |
| A         | 65      | 01000001 |
| B         | 66      | 01000010 |
| a         | 97      | 01100001 |
| 0         | 48      | 00110000 |
| !         | 33      | 00100001 |

---

### Unicode

ASCII became insufficient as computers expanded globally.

Unicode was developed to support:

* Multiple languages
* International symbols
* Mathematical symbols
* Emojis

Unicode provides a unique code point for each character.

Example:

| Character | Unicode |
| --------- | ------- |
| A         | U+0041  |
| €         | U+20AC  |
| 中         | U+4E2D  |
| 😊        | U+1F60A |

---

### UTF (Unicode Transformation Format)

Unicode code points are stored using UTF encoding formats.

Common formats:

| Format | Size      |
| ------ | --------- |
| UTF-8  | 1–4 Bytes |
| UTF-16 | 2–4 Bytes |
| UTF-32 | 4 Bytes   |

---

### UTF-8

Most commonly used encoding today.

Features:

* Backward compatible with ASCII
* Efficient storage
* Supports all Unicode characters
* Dominates web applications

Examples:

```text
A → 1 Byte
€
→ 3 Bytes

😊
→ 4 Bytes
```

---

### UTF-16

Uses:

```text
2 or 4 Bytes
```

Commonly found in:

* Windows systems
* Java applications
* Internal software processing

---

### UTF-32

Uses:

```text
4 Bytes per character
```

Advantages:

* Fixed-length encoding
* Simple processing

Disadvantages:

* Larger storage requirements

---

### Emoji Encoding

Modern emoji characters are also Unicode characters.

Example:

```text
😊
```

Unicode:

```text
U+1F60A
```

Stored using UTF encoding formats.

This allows emojis to be transmitted and displayed across different devices and platforms.

---

### Character Encoding Mismatch

One common issue occurs when text is decoded using the wrong encoding.

Example:

File saved as:

```text
UTF-8
```

But opened as:

```text
ASCII
```

Possible result:

```text
Ã©
â€™
ï»¿
```

This unreadable text is commonly called:

```text
Gibberish
```

or

```text
Mojibake
```

---

## Advantages / Benefits

* Enables consistent text storage.
* Supports multilingual communication.
* Allows global language compatibility.
* Supports symbols and emojis.
* Facilitates reliable data transmission.
* Ensures interoperability between systems.
* Supports modern web applications and databases.

---

## Key Characteristics

* Computers store text as numbers.
* Encodings assign meaning to numeric values.
* ASCII supports 128 characters.
* Unicode supports millions of characters.
* UTF-8 is the most widely used encoding standard.
* UTF-16 and UTF-32 are Unicode encoding formats.
* Emojis are represented using Unicode code points.
* Encoding mismatches can cause unreadable text.

---

## Example

### Encoding the Character "A"

Character:

```text
A
```

ASCII Value:

```text
65
```

Binary Representation:

```text
01000001
```

Unicode Code Point:

```text
U+0041
```

UTF-8 Storage:

```text
41 (Hex)
```

---

## Key Notes

* Encoding maps numbers to characters.
* ASCII was the original text encoding standard.
* Unicode expanded support to global languages and symbols.
* UTF-8 is the standard encoding used on the internet.
* UTF-16 and UTF-32 are alternative Unicode formats.
* Emojis are stored using Unicode code points.
* Incorrect encoding interpretation causes garbled text.
* Understanding encoding is important in cybersecurity, digital forensics, malware analysis, and data recovery.

---

## Learning Outcome

After completing this section, I understood how computers represent text through character encoding systems, how ASCII and Unicode assign numeric values to characters, and how UTF-8, UTF-16, and UTF-32 store Unicode data. I also learned how emojis are encoded and why encoding mismatches can produce unreadable or corrupted text. This knowledge provides a strong foundation for digital forensics, programming, networking, malware analysis, and cybersecurity investigations involving text-based data.
