# Layer 2 - Data Link

## Overview

This task introduced the Data Link Layer, which is Layer 2 of the OSI Model. The Data Link Layer is responsible for physical addressing and preparing data for transmission across a network. It uses MAC (Media Access Control) addresses to identify devices and ensure data reaches the correct destination.

---

## Objectives

* Understand the purpose of the Data Link Layer.
* Learn the role of MAC addresses in network communication.
* Understand the function of a Network Interface Card (NIC).
* Learn how devices are physically identified on a network.
* Understand how data is prepared for transmission.

---

## Tools Used

* No tools were used in this task.

---

## Methodology / Steps

### 1. Understanding the Data Link Layer

The Data Link Layer is Layer 2 of the OSI Model.

It receives data from the Network Layer and prepares it for transmission over the physical network.

Its primary focus is physical addressing and device identification.

---

### 2. Physical Addressing with MAC Addresses

The Data Link Layer uses MAC (Media Access Control) addresses to identify devices on a local network.

Key points:

* Every network-enabled device has a unique MAC address.
* MAC addresses act as physical identifiers.
* Data is delivered using MAC addresses rather than IP addresses at this layer.

---

### 3. Network Interface Card (NIC)

Every network-enabled computer contains a Network Interface Card (NIC).

The NIC is responsible for:

* Connecting the device to a network.
* Storing the device's unique MAC address.
* Supporting communication with other network devices.

---

### 4. MAC Address Characteristics

MAC addresses are:

* Assigned by the manufacturer.
* Unique to each network interface.
* Permanently embedded into the NIC.

Although MAC addresses are generally fixed, they can be altered through a process known as MAC spoofing.

---

### 5. Data Preparation for Transmission

Another important responsibility of the Data Link Layer is formatting data for transmission.

Before data moves to the Physical Layer:

1. The destination MAC address is added.
2. Data is organized into a suitable format.
3. The formatted data is prepared for physical transmission.

---

### 6. Communication Process

The communication flow at the Data Link Layer:

1. Receives data from the Network Layer.
2. Identifies the destination using a MAC address.
3. Formats the data appropriately.
4. Passes the data to the Physical Layer for transmission.

---

## Commands

No commands were used in this task.

---

## Key Findings / Notes

* The Data Link Layer is Layer 2 of the OSI Model.
* It focuses on physical addressing.
* MAC addresses are used to identify devices.
* Every network-enabled device has a unique MAC address.
* MAC addresses are stored on a Network Interface Card (NIC).
* MAC addresses are assigned by manufacturers.
* MAC addresses can be spoofed despite being permanently assigned.
* The Data Link Layer prepares data for transmission across the network.

---

## Learning Outcome

After completing this task, I understood how the Data Link Layer uses MAC addresses to identify devices and manage local network communication. I also learned the role of the Network Interface Card (NIC) and how data is formatted and prepared for transmission before reaching the Physical Layer.
