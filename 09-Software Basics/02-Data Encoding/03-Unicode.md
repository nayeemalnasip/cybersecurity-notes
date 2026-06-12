# Data Encoding

# Unicode

## Overview

As computers became widely used across the world, the limitations of ASCII became increasingly apparent. ASCII was designed primarily for English and could only represent 128 characters. Although extended ASCII standards attempted to support additional languages, they introduced compatibility issues because different regions adopted different encoding schemes.

To solve this problem, **Unicode** was developed as a universal character encoding standard capable of representing characters from virtually every language, script, symbol set, and emoji. Unicode ensures that text created on one system can be accurately displayed on another, regardless of language or platform.

Today, Unicode is the foundation of modern computing, powering websites, operating systems, databases, programming languages, messaging platforms, and cloud services worldwide.

---

## Main Concept

### What is Unicode?

Unicode is a universal character set standard that assigns a unique numeric identifier, known as a **code point**, to every character.

Unlike ASCII, which was limited to English characters, Unicode supports:

* Latin alphabets
* Arabic scripts
* Chinese characters
* Japanese writing systems
* Korean Hangul
* Mathematical symbols
* Currency symbols
* Technical symbols
* Emojis
* Historical writing systems

Each character receives a globally unique code point.

Examples:

| Character | Unicode Code Point |
| --------- | ------------------ |
| A         | U+0041             |
| Ω         | U+03A9             |
| あ         | U+3042             |
| ت         | U+062A             |
| 龍         | U+9F8D             |
| 😊        | U+1F60A            |
| ♞         | U+265E             |

---

## Why Unicode Was Needed

### ASCII Limitations

ASCII uses:

```text
7 Bits
```

Which provides:

```text
128 Characters
```

This was sufficient for:

* English letters
* Numbers
* Basic punctuation
* Control characters

However, ASCII could not represent:

```text
ñ
ü
ß
€
あ
ت
龍
😊
```

---

### Extended ASCII Problems

Extended ASCII introduced:

```text
8 Bits
```

Providing:

```text
256 Characters
```

Different regions created their own standards:

| Encoding     | Supported Languages                  |
| ------------ | ------------------------------------ |
| ISO-8859-1   | Western European Languages           |
| ISO-8859-2   | Central & Eastern European Languages |
| Windows-1252 | Microsoft Western European Systems   |

This created compatibility issues.

Example:

A document saved using:

```text
ISO-8859-1
```

might display incorrectly when opened using:

```text
ISO-8859-2
```

Result:

```text
Original Character: Ø
Displayed Character: Ř
```

This phenomenon is known as:

```text
Character Encoding Mismatch
```

or

```text
Mojibake
```

---

## How Unicode Works

Unicode separates:

### Character Definition

Unicode assigns a unique code point:

```text
A → U+0041
Ω → U+03A9
😊 → U+1F60A
```

---

### Character Storage

The code point is then encoded using:

* UTF-8
* UTF-16
* UTF-32

This allows efficient storage while preserving universal compatibility.

---

### Character Display

When displayed:

```text
Stored Bytes
      ↓
Unicode Code Point
      ↓
Rendered Character
```

Example:

```text
U+1F60A
```

Displays as:

```text
😊
```

---

## Unicode Character Structure

### Code Points

Every Unicode character has a unique identifier.

Format:

```text
U+XXXX
```

Examples:

| Character | Code Point |
| --------- | ---------- |
| A         | U+0041     |
| B         | U+0042     |
| Ω         | U+03A9     |
| ت         | U+062A     |
| 龍         | U+9F8D     |
| 😊        | U+1F60A    |

---

## Unicode Scale

Unicode supports an enormous number of characters.

| Category            | Approximate Count   |
| ------------------- | ------------------- |
| English Alphabet    | 52 Letters          |
| Arabic Variations   | 250+ Characters     |
| Japanese JIS X 0208 | 6,879 Characters    |
| Chinese GB18030     | 87,887+ Characters  |
| Unicode 17.0        | ~157,000 Characters |

Unicode also includes:

* Mathematical symbols
* Scientific notation
* Musical symbols
* Currency symbols
* Technical symbols
* Emoji sequences

Unicode 17.0 contains approximately:

```text
157,000 Characters
```

including nearly:

```text
4,000 Emoji Sequences
```

---

## UTF Encodings

Unicode defines characters.

UTF encodings define how those characters are stored.

### Common Unicode Encodings

| Encoding | Storage Size |
| -------- | ------------ |
| UTF-8    | 1–4 Bytes    |
| UTF-16   | 2–4 Bytes    |
| UTF-32   | 4 Bytes      |

---

# UTF-8

## What is UTF-8?

UTF-8 is the most widely used Unicode encoding format.

Characteristics:

* Variable-length encoding
* Uses 1–4 bytes
* Backward compatible with ASCII
* Efficient storage
* Standard for websites and APIs

---

## UTF-8 Storage Examples

| Character | Unicode | Bytes Used |
| --------- | ------- | ---------- |
| A         | U+0041  | 1 Byte     |
| Ω         | U+03A9  | 2 Bytes    |
| 龍         | U+9F8D  | 3 Bytes    |
| 😊        | U+1F60A | 4 Bytes    |

---

## Advantages of UTF-8

* Saves storage space
* Supports all Unicode characters
* Compatible with ASCII
* Dominates modern web technologies
* Preferred by Linux systems

---

# UTF-16

## What is UTF-16?

UTF-16 stores Unicode characters using:

```text
2 or 4 Bytes
```

Most common characters require:

```text
2 Bytes
```

Complex characters and emojis require:

```text
4 Bytes
```

---

## UTF-16 Examples

| Character | UTF-16        |
| --------- | ------------- |
| A         | U+0041        |
| Ω         | U+03A9        |
| 😊        | U+D83D U+DE0A |
| 🔥        | U+D83D U+DD25 |

---

## Common Usage

UTF-16 is commonly found in:

* Windows Operating Systems
* Microsoft Applications
* Java Environments
* .NET Applications

---

# UTF-32

## What is UTF-32?

UTF-32 uses:

```text
4 Bytes
```

for every Unicode character.

---

## Examples

| Character | UTF-32     |
| --------- | ---------- |
| A         | U+00000041 |
| Ω         | U+000003A9 |
| 😊        | U+0001F60A |
| 🔥        | U+0001F525 |

---

## Advantages

* Fixed-size storage
* Easy indexing
* Simplified processing

---

## Disadvantages

* High storage consumption
* Less efficient than UTF-8
* Rarely used for general-purpose storage

---

## Unicode Character Examples

### Chinese Character

Character:

```text
龍
```

Meaning:

```text
Dragon
```

Unicode:

```text
U+9F8D
```

---

### Emoji

Character:

```text
😊
```

Unicode:

```text
U+1F60A
```

UTF-32 Representation:

```text
U+0001F60A
```

---

### Japanese Character

Character:

```text
ツ
```

Unicode:

```text
U+30C4
```

---

### Arabic Character

Character:

```text
ت
```

Unicode:

```text
U+062A
```

---

### Chess Piece

Character:

```text
♞
```

Unicode:

```text
U+265E
```

Meaning:

```text
Black Knight
```

---

## Advantages / Benefits

* Universal character support.
* Eliminates regional encoding conflicts.
* Supports multilingual communication.
* Enables consistent text exchange worldwide.
* Supports emojis and special symbols.
* Standardized across platforms and operating systems.
* Facilitates global software development.
* Reduces data corruption caused by incompatible encodings.

---

## Key Characteristics

* Unicode is a universal character set.
* Every character has a unique code point.
* Unicode supports nearly all modern languages.
* UTF-8 is the most widely used Unicode encoding.
* UTF-16 uses 2–4 bytes.
* UTF-32 uses a fixed 4-byte structure.
* Unicode includes emojis and special symbols.
* Modern operating systems rely heavily on Unicode.
* Unicode solves compatibility problems caused by regional encodings.

---

## Example

### Multilingual Unicode Text

A single Unicode file can contain:

```text
Hello World
مرحبا بالعالم
こんにちは世界
你好世界
😊
♞
€
Ω
```

Without requiring separate encoding standards for each language.

This interoperability is one of the primary reasons Unicode became the global standard for text representation.

---

## Key Notes

* ASCII supports 128 characters.
* Extended ASCII supports 256 characters.
* Unicode supports approximately 157,000 characters.
* Every Unicode character has a unique code point.
* UTF-8 is the most common encoding format on the internet.
* UTF-8 remains backward compatible with ASCII.
* UTF-16 is widely used in Windows and Java environments.
* UTF-32 prioritizes simplicity over storage efficiency.
* Emojis are Unicode characters.
* Unicode eliminates character encoding conflicts between languages and systems.

---

## Learning Outcome

After completing this section, I gained a comprehensive understanding of Unicode as the universal character encoding standard used in modern computing. I learned why ASCII and extended ASCII were insufficient for global communication, how Unicode assigns unique code points to characters from every language and symbol set, and how UTF-8, UTF-16, and UTF-32 store Unicode data efficiently. I also developed an understanding of emoji encoding, multilingual text processing, and the importance of Unicode in ensuring consistent data representation across operating systems, applications, databases, web technologies, and cybersecurity environments.
