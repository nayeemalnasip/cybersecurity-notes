Number Systems and Data Representation
Overview

Computers operate using only two states, represented as 0 and 1. While humans naturally use the decimal (base-10) system, computers rely on the binary (base-2) system to store, process, and transmit data. To simplify working with binary values, hexadecimal (base-16) and octal (base-8) representations are also commonly used.

Understanding these number systems is fundamental for networking, programming, operating systems, digital forensics, reverse engineering, and cybersecurity.

Main Concept
What are Number Systems?

A number system defines how numerical values are represented using a specific set of symbols and a base value.

Number System	Base	Digits Used
Decimal	10	0–9
Binary	2	0–1
Octal	8	0–7
Hexadecimal	16	0–9, A–F

Each digit position represents a power of the system's base.

How It Works
Decimal Number System (Base-10)

Humans use decimal numbers daily.

Example:

213

Can be expanded as:

213 = (2 × 10²) + (1 × 10¹) + (3 × 10⁰)

213 = (2 × 100) + (1 × 10) + (3 × 1)
Binary Number System (Base-2)

Binary uses only two digits:

0 and 1

Each position represents a power of 2.

Example:

1001

Calculation:

1001

= (1 × 2³) + (0 × 2²) + (0 × 2¹) + (1 × 2⁰)

= (1 × 8) + (0 × 4) + (0 × 2) + (1 × 1)

= 9
Binary to Decimal Examples
Binary	Decimal
0000	0
0001	1
0010	2
0011	3
0100	4
1000	8
1100	12
1101	13
1110	14
1111	15
Why Computers Use Binary

Computer hardware can easily distinguish between two physical states:

Physical State	Binary Value
Low Voltage	0
High Voltage	1
Magnetic South	0
Magnetic North	1
No Light	0
Light Present	1

These physical states form the foundation of all digital systems.

Important Components
Bit

A bit (Binary Digit) is the smallest unit of data.

Possible values:

0
1
Byte

A byte consists of 8 bits.

1 Byte = 8 Bits

A byte can represent:

256 different values

Range:

0 – 255
Hexadecimal Number System (Base-16)

Hexadecimal provides a compact representation of binary values.

Digits:

0 1 2 3 4 5 6 7 8 9 A B C D E F

Where:

Hex	Decimal
A	10
B	11
C	12
D	13
E	14
F	15
Binary and Hexadecimal Relationship

Every 4 bits correspond to one hexadecimal digit.

Binary	Hex
0000	0
0001	1
0010	2
0011	3
0100	4
0101	5
0110	6
0111	7
1000	8
1001	9
1010	A
1011	B
1100	C
1101	D
1110	E
1111	F
Hexadecimal to Decimal Example

Hexadecimal:

9BDF

Calculation:

9BDF

= (9 × 16³)
+ (11 × 16²)
+ (13 × 16¹)
+ (15 × 16⁰)

= 36864
+ 2816
+ 208
+ 15

= 39903
Octal Number System (Base-8)

Octal uses eight digits:

0–7

Each octal digit represents 3 binary bits.

Octal	Binary
0	000
1	001
2	010
3	011
4	100
5	101
6	110
7	111
Octal to Decimal Example
357

Calculation:

357

= (3 × 8²)
+ (5 × 8¹)
+ (7 × 8⁰)

= (3 × 64)
+ (5 × 8)
+ (7 × 1)

= 239
Advantages / Benefits
Enables efficient data representation.
Matches the physical operation of digital hardware.
Simplifies memory and storage management.
Makes network and packet analysis easier.
Supports compact representation through hexadecimal notation.
Essential for programming and cybersecurity analysis.
Key Characteristics
Binary uses only 0 and 1.
Decimal uses digits 0–9.
Octal uses digits 0–7.
Hexadecimal uses digits 0–9 and A–F.
Every binary position represents a power of 2.
Every hexadecimal position represents a power of 16.
Every octal position represents a power of 8.
4 bits equal 1 hexadecimal digit.
3 bits equal 1 octal digit.
8 bits equal 1 byte.
Example
Memory Analysis Example

A cybersecurity analyst examining memory may encounter:

0xFF

Hexadecimal:

FF

Binary:

11111111

Decimal:

255

Understanding these conversions is essential when analyzing memory dumps, packet captures, malware behavior, and system logs.

Key Notes
Binary is the native language of computers.
A bit stores one binary value.
A byte consists of 8 bits.
Hexadecimal is the most commonly used compact binary representation.
Memory addresses are often displayed in hexadecimal.
Network packets frequently contain hexadecimal values.
Digital forensics tools rely heavily on hexadecimal analysis.
Binary and hexadecimal knowledge is fundamental for cybersecurity professionals.
Learning Outcome

After completing this section, I understood how decimal, binary, hexadecimal, and octal number systems represent data, how computers use binary values to process information, and how hexadecimal simplifies binary representation. I also learned how these number systems are applied in memory analysis, networking, programming, digital forensics, and cybersecurity operations.