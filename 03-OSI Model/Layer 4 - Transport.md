# Layer 4 - Transport

## Overview

This task introduced the Transport Layer, which is Layer 4 of the OSI Model. The Transport Layer is responsible for delivering data between devices and ensuring communication occurs using the appropriate protocol. Two primary protocols operate at this layer: TCP (Transmission Control Protocol) and UDP (User Datagram Protocol).

---

## Objectives

* Understand the purpose of the Transport Layer.
* Learn the differences between TCP and UDP.
* Understand how TCP ensures reliable communication.
* Learn why UDP provides faster communication.
* Identify real-world use cases for both protocols.

---

## Tools Used

* No tools were used in this task.

---

## Methodology / Steps

### 1. Understanding the Transport Layer

The Transport Layer is Layer 4 of the OSI Model.

Its primary responsibilities include:

* Transporting data between devices.
* Managing communication sessions.
* Ensuring data delivery based on the selected protocol.
* Controlling how data is transmitted across a network.

At this layer, communication occurs using one of two protocols:

* TCP (Transmission Control Protocol)
* UDP (User Datagram Protocol)

---

### 2. Transmission Control Protocol (TCP)

TCP is designed for reliable communication.

It establishes a dedicated connection between devices and ensures that data arrives accurately and in the correct order.

TCP performs additional processes such as:

* Error checking
* Packet verification
* Data synchronization
* Packet reassembly

This makes TCP highly reliable for important communications.

---

### 3. Advantages of TCP

* Guarantees accurate data delivery.
* Ensures packets arrive in the correct order.
* Provides error checking and verification.
* Synchronizes communication between devices.
* Prevents devices from overwhelming each other with data.

---

### 4. Disadvantages of TCP

* Slower than UDP.
* Requires a constant connection between devices.
* Additional processing increases communication overhead.
* Lost packets can delay the entire transmission.

---

### 5. Common Uses of TCP

TCP is commonly used when data accuracy is critical.

Examples include:

* File Sharing
* Web Browsing
* Email Communication

These services require complete and accurate data delivery.

---

### 6. User Datagram Protocol (UDP)

UDP is designed for speed rather than reliability.

Unlike TCP, UDP does not establish a dedicated connection between devices.

It sends data without:

* Error checking
* Packet verification
* Delivery confirmation

The data is transmitted without guaranteeing successful delivery.

---

### 7. Advantages of UDP

* Faster than TCP.
* Requires fewer resources.
* Does not maintain a continuous connection.
* Provides flexibility for applications.

---

### 8. Disadvantages of UDP

* No guarantee that data will arrive.
* No packet ordering.
* No error checking.
* Packet loss can occur without notification.

---

### 9. Common Uses of UDP

UDP is useful when speed is more important than perfect accuracy.

Examples include:

* ARP Communications
* DHCP Communications
* Video Streaming
* Real-Time Applications

Minor packet loss is often acceptable in these scenarios.

---

### 10. TCP vs UDP Comparison

| Feature             | TCP        | UDP            |
| ------------------- | ---------- | -------------- |
| Reliability         | High       | Low            |
| Error Checking      | Yes        | No             |
| Connection Required | Yes        | No             |
| Speed               | Slower     | Faster         |
| Packet Ordering     | Guaranteed | Not Guaranteed |
| Data Verification   | Yes        | No             |

---

### 11. Communication Process

#### TCP Workflow

1. Establishes a connection.
2. Sends data packets.
3. Verifies packet delivery.
4. Reassembles packets in order.
5. Delivers complete data to the application.

#### UDP Workflow

1. Sends packets immediately.
2. Does not verify delivery.
3. Does not reorder packets.
4. Delivers received data directly to the application.

---

## Commands

No commands were used in this task.

---

## Key Findings / Notes

* The Transport Layer is Layer 4 of the OSI Model.
* TCP and UDP are the primary protocols used at this layer.
* TCP prioritizes reliability and accuracy.
* UDP prioritizes speed and efficiency.
* TCP uses error checking and packet verification.
* UDP sends data without delivery guarantees.
* File transfers, web browsing, and email commonly use TCP.
* Streaming and discovery protocols commonly use UDP.
* Choosing between TCP and UDP depends on the communication requirements.

---

## Learning Outcome

After completing this task, I understood the role of the Transport Layer and the differences between TCP and UDP. I learned how TCP ensures reliable communication through error checking and packet verification, while UDP provides faster communication by sacrificing reliability and delivery guarantees.
