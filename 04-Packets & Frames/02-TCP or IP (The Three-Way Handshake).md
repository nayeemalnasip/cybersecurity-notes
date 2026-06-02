# TCP/IP (The Three-Way Handshake)

## Overview

This task introduced the TCP/IP model and the TCP Three-Way Handshake process. I explored how TCP establishes reliable communication between devices, how encapsulation works within the TCP/IP model, and how connections are created, maintained, and terminated. I also examined important TCP packet headers and their role in ensuring data integrity and accurate delivery.

---

## Objectives

* Understand the TCP/IP model.
* Learn the concept of encapsulation and decapsulation.
* Explore how TCP establishes reliable communication.
* Understand the TCP Three-Way Handshake process.
* Learn the purpose of important TCP packet headers.
* Understand how TCP connections are terminated.

---

## Tools Used

* No tools were used in this task.

---

## Methodology / Steps

### 1. Understanding the TCP/IP Model

The TCP/IP model is a networking framework used for communication across networks and the Internet.

The model consists of four layers:

* Application
* Transport
* Internet
* Network Interface

Similar to the OSI Model, data moves through these layers and additional information is added during transmission through a process called encapsulation.

At the receiving side, this information is removed through decapsulation.

---

### 2. Understanding TCP

TCP (Transmission Control Protocol) is a connection-oriented protocol designed to provide reliable communication between devices.

Before data can be transmitted, TCP establishes a connection between the sender and receiver.

Key characteristics of TCP:

* Reliable communication
* Error checking
* Data integrity verification
* Packet ordering
* Connection management

---

### 3. Advantages of TCP

* Guarantees data integrity.
* Ensures packets arrive in the correct order.
* Synchronizes communication between devices.
* Prevents data flooding.
* Performs extensive reliability checks.

---

### 4. Disadvantages of TCP

* Requires a stable connection.
* Slower than UDP.
* Uses additional system resources.
* Lost packets require retransmission.
* Connection overhead can reduce performance.

---

### 5. Understanding TCP Packet Headers

TCP packets contain multiple headers that provide information required for communication.

#### Source Port

Identifies the sender's communication port.

* Randomly selected.
* Range: 0–65535

---

#### Destination Port

Identifies the service or application receiving the data.

Examples:

* Port 80 (HTTP)
* Port 443 (HTTPS)

---

#### Source IP

The IP address of the sending device.

---

#### Destination IP

The IP address of the receiving device.

---

#### Sequence Number

A unique number assigned to transmitted data.

Used to:

* Track packets
* Maintain packet order
* Reconstruct transmitted data

---

#### Acknowledgement Number

Confirms successful receipt of data.

Typically:

```text
Acknowledgement Number = Sequence Number + 1
```

---

#### Checksum

Used for integrity verification.

Purpose:

* Detect data corruption.
* Validate packet contents.

---

#### Data

Contains the actual transmitted information.

Examples:

* Files
* Web content
* Messages

---

#### Flag

Controls how packets are handled during communication.

Examples:

* SYN
* ACK
* FIN
* RST

---

### 6. Understanding the Three-Way Handshake

TCP uses the Three-Way Handshake to establish a reliable connection between two devices.

This process synchronizes both devices before data transmission begins.

---

### Step 1 - SYN

The client initiates communication by sending a SYN packet.

Purpose:

* Request a connection.
* Share its Initial Sequence Number (ISN).

Example:

```text
Client → Server : SYN
ISN = 0
```

---

### Step 2 - SYN/ACK

The server acknowledges the client's request and sends its own sequence number.

Purpose:

* Confirm synchronization request.
* Provide server ISN.

Example:

```text
Server → Client : SYN/ACK
ISN = 5000
ACK = 0
```

---

### Step 3 - ACK

The client acknowledges the server's sequence number.

Purpose:

* Confirm synchronization.
* Complete connection establishment.

Example:

```text
Client → Server : ACK
ACK = 5000
```

Once this process is completed, data transmission can begin.

---

### 7. Sequence Number Progression

TCP uses sequence numbers to maintain packet order.

Example:

| Sequence Number | Next Sequence Number |
| --------------- | -------------------- |
| 0               | 1                    |
| 1               | 2                    |
| 2               | 3                    |

This mechanism ensures that data is reconstructed correctly at the destination.

---

### 8. Data Transmission

After the Three-Way Handshake:

1. Connection is established.
2. Data packets are transmitted.
3. Packets are acknowledged.
4. Data is reconstructed in the correct order.

This guarantees reliable communication between devices.

---

### 9. Closing a TCP Connection

TCP connections should be closed once communication is complete.

This frees system resources and prevents unnecessary connections from remaining active.

---

### Step 1 - FIN

The initiating device sends a FIN packet requesting connection termination.

```text
Client → Server : FIN
```

---

### Step 2 - ACK

The receiving device acknowledges the FIN request.

```text
Server → Client : ACK
```

---

### Step 3 - FIN

The receiving device also requests connection termination.

```text
Server → Client : FIN
```

---

### Step 4 - ACK

The initiating device acknowledges the request.

```text
Client → Server : ACK
```

The connection is now successfully closed.

---

### 10. RST Packet

In certain situations, communication may terminate abruptly using an RST (Reset) packet.

This occurs when:

* Services fail.
* Applications encounter errors.
* System resources become unavailable.
* Communication cannot continue normally.

RST immediately ends the connection.

---

## Commands

No commands were used in this task.

---

## Key Findings / Notes

* TCP/IP consists of four layers.
* Encapsulation adds information as data moves through the layers.
* TCP is a connection-oriented protocol.
* TCP guarantees reliable data delivery.
* Sequence numbers maintain packet order.
* Checksum verifies packet integrity.
* The Three-Way Handshake establishes communication.
* SYN, SYN/ACK, and ACK are used during connection establishment.
* FIN and ACK are used during connection termination.
* RST immediately resets a connection when errors occur.

---

## Learning Outcome

After completing this task, I understood how the TCP/IP model supports network communication and how TCP establishes reliable connections using the Three-Way Handshake. I learned the purpose of TCP packet headers, sequence numbers, acknowledgements, connection management, and how TCP ensures data integrity throughout transmission.
