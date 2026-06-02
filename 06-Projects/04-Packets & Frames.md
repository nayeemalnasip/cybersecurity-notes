# Packets & Frames - Project Summary

## Project Overview

This project focused on understanding how data is transmitted across networks through packets, frames, TCP, UDP, and network ports. Throughout the room, I explored the structure of network communication, learned how TCP and UDP operate, analyzed the TCP Three-Way Handshake process, and completed practical challenges involving network connections and ports.

---

## Task Completion Process

### Understanding Packets and Frames

The first task introduced the fundamental building blocks of network communication: packets and frames.

I learned that packets operate at the Network Layer and contain IP addressing information, while frames operate at the Data Link Layer and encapsulate packets for transmission across a network.

**Key Concepts Learned:**

* Packet = Data containing IP addressing information.
* Frame = Encapsulated data without IP addressing focus.
* Encapsulation process within the OSI Model.
* Role of packets and frames in network communication.

**Outcome:**

* Distinguished between packets and frames.
* Understood how data moves through network layers.
* Learned the concept of encapsulation.

---

### Exploring TCP and the Three-Way Handshake

The second task focused on TCP (Transmission Control Protocol) and how reliable communication is established between devices.

I studied TCP packet headers and learned how integrity is maintained using the checksum field. I also explored the TCP Three-Way Handshake process used to establish communication before data transfer begins.

**Three-Way Handshake Sequence:**

```text
SYN → SYN/ACK → ACK
```

**Key Concepts Learned:**

* TCP connection establishment.
* Sequence and acknowledgement process.
* Checksum validation for data integrity.
* Reliable data transmission.

**Outcome:**

* Understood how TCP guarantees reliable communication.
* Learned how devices synchronize before transmitting data.
* Identified the purpose of the checksum field.

---

### Analyzing TCP Communication

In the practical TCP communication exercise, I analyzed a network conversation and identified the correct flag after understanding the packet exchange process.

**Practical Activity Completed:**

```text
THM{TCP_CHATTER}
```

**Outcome:**

* Reinforced understanding of TCP communication flow.
* Applied packet analysis concepts in a practical scenario.

---

### Understanding UDP Communication

The fourth task introduced UDP (User Datagram Protocol) and highlighted the differences between UDP and TCP.

I learned that UDP is a stateless protocol that does not establish a connection before sending data. Unlike TCP, UDP prioritizes speed over reliability.

**Key Concepts Learned:**

* UDP stands for User Datagram Protocol.
* UDP is stateless.
* No handshake process occurs.
* No delivery guarantees exist.

**Protocol Selection Examples:**

| Activity      | Protocol |
| ------------- | -------- |
| File Transfer | TCP      |
| Video Call    | UDP      |

**Outcome:**

* Understood when to use TCP vs UDP.
* Learned the advantages and limitations of connectionless communication.
* Explored real-world UDP use cases.

---

### Working with Network Ports

The final task focused on ports and how applications communicate through specific network endpoints.

I completed the practical challenge by connecting to the specified IP address and port to retrieve the room flag.

**Connection Details:**

```text
IP Address: 8.8.8.8
Port: 1234
```

**Practical Activity Completed:**

```text
THM{YOU_CONNECTED_TO_A_PORT}
```

**Outcome:**

* Understood the purpose of network ports.
* Learned how services listen on specific ports.
* Successfully connected to a target service and retrieved the flag.

---

## Skills Demonstrated

* Network Communication Fundamentals
* Packets and Frames
* Encapsulation Concepts
* TCP Protocol Analysis
* Three-Way Handshake Understanding
* Checksum Validation Concepts
* UDP Communication
* Network Port Fundamentals
* Service Connectivity
* Basic Packet Analysis

---

## Project Conclusion

By completing this room, I developed a solid understanding of how data is transmitted across networks using packets and frames. I explored both TCP and UDP communication models, learned how reliable connections are established through the Three-Way Handshake, and gained practical experience working with network ports and service connections. These concepts form a strong foundation for future networking, packet analysis, and cybersecurity activities.
