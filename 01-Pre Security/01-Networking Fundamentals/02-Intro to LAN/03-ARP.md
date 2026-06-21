# ARP (Address Resolution Protocol)

## Overview

This task introduced the Address Resolution Protocol (ARP), a network protocol responsible for mapping IP addresses to MAC addresses within a local network. ARP enables devices to identify and communicate with each other by resolving logical addresses (IP) into physical addresses (MAC).

---

## Objectives

* Understand the purpose of ARP.
* Learn how devices associate IP addresses with MAC addresses.
* Understand the role of the ARP cache.
* Learn the difference between ARP Requests and ARP Replies.
* Explore how devices discover each other on a network.

---

## Tools Used

* No tools were used in this task.

---

## Methodology / Steps

### 1. Understanding ARP

Devices on a network use two identifiers:

* IP Address (Logical Address)
* MAC Address (Physical Address)

ARP (Address Resolution Protocol) is responsible for linking these two identifiers together.

Its primary function is to determine which MAC address belongs to a specific IP address.

---

### 2. Understanding the ARP Cache

Every device maintains a local database known as an ARP Cache.

The ARP Cache stores previously discovered mappings between:

* IP Addresses
* MAC Addresses

This allows devices to communicate efficiently without repeatedly searching for the same device.

---

### 3. ARP Communication Process

ARP operates using two message types:

#### ARP Request

An ARP Request is broadcast to all devices on the local network.

Purpose:

* Ask which device owns a specific IP address.
* Discover the MAC address associated with that IP.

Example Question:

```text
Who has IP address 192.168.1.100?
```

---

#### ARP Reply

The device that owns the requested IP address responds with an ARP Reply.

Purpose:

* Provide its MAC address to the requesting device.

Example Response:

```text
192.168.1.100 is at a4:c3:f0:85:ac:2d
```

---

### 4. Mapping IP Addresses to MAC Addresses

The communication process follows these steps:

1. A device wants to communicate with another device.
2. The device checks its ARP Cache.
3. If no mapping exists, it sends an ARP Request.
4. The target device responds with an ARP Reply.
5. The mapping is stored in the ARP Cache.
6. Future communication uses the cached information.

---

### 5. Why ARP is Important

ARP is essential because:

* Devices communicate using MAC addresses on local networks.
* Users and applications typically use IP addresses.
* ARP bridges the gap between logical and physical addressing.

Without ARP, devices would not know the physical destination of network traffic within a LAN.

---

## Commands

No commands were used in this task.

---

## Key Findings / Notes

* ARP stands for Address Resolution Protocol.
* ARP maps IP addresses to MAC addresses.
* Every device maintains an ARP Cache.
* ARP Requests are broadcast across the network.
* Only the device that owns the requested IP address responds.
* ARP Replies provide the associated MAC address.
* ARP helps devices discover and communicate with one another on a local network.
* Cached ARP entries improve communication efficiency.

---

## Learning Outcome

After completing this task, I understood how ARP enables communication within a local network by mapping IP addresses to MAC addresses. I also learned the roles of ARP Requests, ARP Replies, and the ARP Cache in helping devices identify and communicate with each other efficiently.
