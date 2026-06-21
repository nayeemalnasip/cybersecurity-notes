# Numbers and Colors

## Representing Colors

### Overview

Modern computers and digital devices represent colors using the **RGB (Red, Green, Blue)** color model. By combining different intensities of red, green, and blue light, a computer can generate millions of unique colors. Understanding color representation is important in computer graphics, web development, digital forensics, image analysis, and cyber security investigations involving multimedia files.

---

## Main Concept

### What is Color Representation?

Color representation is the method computers use to store and display colors digitally.

Computers create colors by combining three primary light colors:

* Red (R)
* Green (G)
* Blue (B)

Each color component is assigned a numeric value that determines its intensity.

```text
RGB = Red + Green + Blue
```

Different combinations of these values produce different colors.

---

## How It Works

### Step 1: Using Three Color Channels

A computer treats every color as a combination of:

```text
Red
Green
Blue
```

Each channel can have different intensity levels.

---

### Step 2: Simple On/Off Color System

Assume each color channel can only be:

```text
0 = OFF
1 = ON
```

Since there are three channels:

```text
2 × 2 × 2 = 8 Colors
```

Each channel is represented by one bit.

```text
RGB
```

Example:

```text
100
```

Means:

```text
Red   = ON
Green = OFF
Blue  = OFF
```

Result:

```text
Red Color
```

---

### Step 3: Creating the First Eight Colors

| Binary | Red | Green | Blue | Color   |
| ------ | --- | ----- | ---- | ------- |
| 000    | Off | Off   | Off  | Black   |
| 001    | Off | Off   | On   | Blue    |
| 010    | Off | On    | Off  | Green   |
| 011    | Off | On    | On   | Cyan    |
| 100    | On  | Off   | Off  | Red     |
| 101    | On  | Off   | On   | Magenta |
| 110    | On  | On    | Off  | Yellow  |
| 111    | On  | On    | On   | White   |

---

### Step 4: Expanding to Millions of Colors

Using only ON/OFF values is very limiting.

Modern systems allow each RGB component to have:

```text
256 Levels
```

Range:

```text
0 - 255
```

Therefore:

```text
256 × 256 × 256
=
16,777,216 Colors
```

This provides over 16 million unique colors.

---

## Important Components

### Bit

A **bit** is the smallest unit of data in computing.

Possible values:

```text
0
1
```

Example:

```text
Red = 1
Green = 0
Blue = 1
```

Binary:

```text
101
```

Produces:

```text
Magenta
```

---

### Byte

A **byte** consists of eight bits.

```text
1 Byte = 8 Bits
```

Example:

```text
11111111
```

Maximum value:

```text
255
```

---

### Octet

An octet is another name for a byte.

```text
1 Octet = 8 Bits
```

Commonly used in networking and cybersecurity documentation.

---

### RGB Color Model

RGB uses three bytes:

| Component | Size   |
| --------- | ------ |
| Red       | 8 Bits |
| Green     | 8 Bits |
| Blue      | 8 Bits |

Total:

```text
8 + 8 + 8 = 24 Bits
```

or

```text
3 Bytes
```

---

### 24-Bit Color

Modern displays typically use:

```text
24-bit Color
```

Structure:

```text
RRRRRRRR GGGGGGGG BBBBBBBB
```

Example:

```text
10100011 11101010 00101010
```

---

### Hexadecimal Representation

Binary values are difficult for humans to read.

Hexadecimal provides a compact representation.

Every:

```text
4 Bits
```

are represented by:

```text
1 Hexadecimal Digit
```

---

### Binary to Hexadecimal Mapping

| Hex | Binary |
| --- | ------ |
| 0   | 0000   |
| 1   | 0001   |
| 2   | 0010   |
| 3   | 0011   |
| 4   | 0100   |
| 5   | 0101   |
| 6   | 0110   |
| 7   | 0111   |
| 8   | 1000   |
| 9   | 1001   |
| A   | 1010   |
| B   | 1011   |
| C   | 1100   |
| D   | 1101   |
| E   | 1110   |
| F   | 1111   |

---

### Color Code Conversion Example

Binary Color:

```text
10100011 11101010 00101010
```

Split into groups of 4 bits:

```text
1010 0011 1110 1010 0010 1010
```

Convert each group:

| Binary | Hex |
| ------ | --- |
| 1010   | A   |
| 0011   | 3   |
| 1110   | E   |
| 1010   | A   |
| 0010   | 2   |
| 1010   | A   |

Result:

```text
A3EA2A
```

This is the hexadecimal color code.

---

## Advantages / Benefits

* Efficient color storage
* Supports over 16 million colors
* Produces realistic digital images
* Compact hexadecimal notation
* Easy integration with web technologies
* Widely supported across operating systems
* Simplifies image processing and graphics rendering

---

## Key Characteristics

* RGB is the standard color model used by displays.
* Each RGB component uses one byte.
* A color requires 24 bits (3 bytes).
* Each byte stores values from 0–255.
* 24-bit color provides 16,777,216 possible colors.
* Every hexadecimal digit represents 4 bits.
* Two hexadecimal digits represent one byte.
* Hexadecimal notation is commonly used in web design, programming, and cybersecurity tools.

---

## Example

### Red Color

RGB Values:

```text
255, 0, 0
```

Binary:

```text
11111111 00000000 00000000
```

Hexadecimal:

```text
FF0000
```

---

### Green Color

RGB Values:

```text
0, 255, 0
```

Hexadecimal:

```text
00FF00
```

---

### Blue Color

RGB Values:

```text
0, 0, 255
```

Hexadecimal:

```text
0000FF
```

---

### White Color

RGB Values:

```text
255, 255, 255
```

Hexadecimal:

```text
FFFFFF
```

---

## Key Notes

* RGB stands for Red, Green, and Blue.
* Three bits can represent 8 colors.
* One bit stores either 0 or 1.
* One byte equals 8 bits.
* One color is represented using 24 bits.
* 24-bit color supports 16,777,216 colors.
* Every hexadecimal digit represents 4 bits.
* Two hexadecimal digits represent one byte.
* Hexadecimal notation makes color values easier to read and write.
* RGB and hexadecimal color codes are widely used in web development, graphics, image analysis, and digital forensics.

---

## Learning Outcome

After completing this section, I understood how computers represent colors using the RGB color model, how binary values control color intensity, and how 24-bit color enables the representation of more than 16 million colors. I also learned how hexadecimal notation simplifies binary color representation and why RGB and hexadecimal values are widely used in computer graphics, web technologies, digital forensics, and cybersecurity analysis.
