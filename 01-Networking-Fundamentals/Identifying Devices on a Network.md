# Identifying Devices on a Network

## Overview

Devices on a network must be uniquely identifiable to communicate effectively. Similar to how humans can be identified by their names and fingerprints, network devices use two primary identifiers:

* IP Address
* MAC Address

An IP address can change over time, while a MAC address is typically permanently assigned to the device's network interface.

---

## Objectives

* Understand how devices are identified on a network.
* Learn the difference between IP addresses and MAC addresses.
* Distinguish between public and private IP addresses.
* Understand IPv4 and IPv6 addressing.
* Learn the purpose of MAC addresses and MAC spoofing.

---

## Tools Used

* Interactive TryHackMe Lab

---

## Methodology / Steps

### 1. Device Identification

Every device connected to a network requires unique identifiers to enable communication and maintain network organization.

The two main identifiers are:

| Identifier  | Purpose                                                |
| ----------- | ------------------------------------------------------ |
| IP Address  | Logical address used to identify a device on a network |
| MAC Address | Physical address assigned to the network interface     |

---

### 2. Understanding IP Addresses

An IP (Internet Protocol) address is a logical address assigned to a device on a network.

Example IPv4 Address:

```text
192.168.1.77
```

Characteristics:

* Consists of four octets separated by periods.
* Used to identify devices on a network.
* Can change over time.
* Must be unique within the same network.

---

### 3. Public vs Private IP Addresses

Devices can have both private and public IP addresses.

#### Private IP Address

Used for communication within a local network.

Examples:

```text
192.168.1.77
192.168.1.74
```

#### Public IP Address

Used to identify a network on the Internet.

Example:

```text
86.157.52.21
```

Example Network:

| Device          | Private IP   | Public IP    |
| --------------- | ------------ | ------------ |
| DESKTOP-KJE57FD | 192.168.1.77 | 86.157.52.21 |
| CMNatic-PC      | 192.168.1.74 | 86.157.52.21 |

Key Observation:

* Devices communicate internally using private IP addresses.
* Traffic sent to the Internet appears under the same public IP address.
* Public IP addresses are assigned by an Internet Service Provider (ISP).

---

### 4. IPv4 and IPv6

#### IPv4

IPv4 uses a 32-bit addressing scheme.

Example:

```text
192.168.1.77
```

Characteristics:

* Supports approximately 4.29 billion addresses (2³²).
* Limited address space due to the increasing number of connected devices.

#### IPv6

IPv6 was introduced to overcome IPv4 address limitations.

Example:

```text
2001:0db8:85a3:0000:0000:8a2e:0370:7334
```

Benefits:

* Supports approximately 2¹²⁸ addresses.
* Provides significantly larger address space.
* Improves network efficiency through newer technologies.

---

### 5. Understanding MAC Addresses

A MAC (Media Access Control) address is a unique identifier assigned to a device's network interface during manufacturing.

Example:

```text
a4:c3:f0:85:ac:2d
```

Characteristics:

* Consists of 12 hexadecimal characters.
* Divided into six pairs separated by colons.
* First six characters identify the manufacturer.
* Last six characters uniquely identify the device.

---

### 6. MAC Address Spoofing

MAC spoofing is the process of changing a device's MAC address to impersonate another device.

Potential Impact:

* Can bypass poorly configured security controls.
* May allow unauthorized access to network resources.
* Can be used to impersonate trusted devices.

Example Scenario:

* A firewall allows traffic from an administrator's MAC address.
* An attacker spoofs that MAC address.
* The firewall incorrectly trusts the attacker's device.

---

### 7. Practical Lab Scenario

The interactive lab simulated a hotel Wi-Fi network.

Scenario:

* Alice has paid for Wi-Fi access.
* Bob has not paid for Wi-Fi access.
* The router allows Alice's traffic while blocking Bob's traffic.

Task:

* Change Bob's MAC address to match Alice's MAC address.
* Observe how the router treats Bob's traffic after spoofing.

This demonstrates how MAC-based access controls can be bypassed when relying solely on MAC addresses for authentication.

---

## Commands

No commands were used in this task.

---

## Key Findings / Notes

* Devices use IP addresses and MAC addresses for identification.
* IP addresses are logical and can change.
* MAC addresses are physical identifiers assigned to network interfaces.
* Private IP addresses are used within local networks.
* Public IP addresses identify networks on the Internet.
* IPv4 provides approximately 4.29 billion addresses.
* IPv6 provides a significantly larger address space.
* MAC spoofing allows a device to impersonate another device.
* Security mechanisms based solely on MAC addresses can be bypassed.

---

## Learning Outcome

After completing this task, I understood how devices are identified on a network using IP and MAC addresses. I learned the differences between public and private IP addresses, the purpose of IPv4 and IPv6, and how MAC spoofing can be used to bypass weak network access controls.
