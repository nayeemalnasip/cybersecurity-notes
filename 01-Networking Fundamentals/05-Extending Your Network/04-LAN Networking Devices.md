# Extending Your Network

## LAN Networking Devices

### Overview

LAN (Local Area Network) environments rely on networking devices to enable communication between systems. Two of the most important devices are routers and switches. While both play critical roles in network communication, they perform different functions and operate at different layers of the OSI model.

---

## Router

### What is a Router?

A router is a networking device responsible for connecting multiple networks and forwarding data between them.

The process used by routers to move data between networks is called:

```text
Routing
```

Routers primarily operate at:

```text
OSI Layer 3 (Network Layer)
```

---

## How Routing Works

Routing is the process of determining the best path for data to travel from one network to another.

When multiple paths exist, routers use routing protocols to decide which route should be used.

### Factors Used in Route Selection

* Shortest path available.
* Most reliable path.
* Fastest transmission medium (e.g., Fiber vs Copper).

---

## Router Features

Modern routers commonly provide administrative interfaces such as:

* Web-based dashboards
* Command Line Interfaces (CLI)

These interfaces allow administrators to configure:

* Port Forwarding
* Firewall Rules
* Network Management Settings
* Routing Policies

---

## Key Functions of a Router

* Connects separate networks.
* Routes packets between networks.
* Determines optimal communication paths.
* Provides network security controls.
* Supports Internet connectivity.

---

## Switch

### What is a Switch?

A switch is a networking device used to connect multiple devices within the same network.

Devices commonly connected to switches include:

* Computers
* Printers
* Servers
* Access Points
* IP Phones

Switches use Ethernet connections to facilitate communication between devices.

---

## Switch Capacity

Switches can support multiple connected devices, typically ranging from:

```text
3 – 63 Devices
```

depending on hardware specifications.

---

## Layer 2 Switch

A Layer 2 switch operates at:

```text
OSI Layer 2 (Data Link Layer)
```

### How Layer 2 Switching Works

Layer 2 switches forward frames based on:

```text
MAC Addresses
```

Responsibilities include:

* Receiving frames.
* Identifying destination MAC addresses.
* Forwarding frames to the correct device.

### Key Characteristics

* Works only with MAC addresses.
* Cannot perform routing.
* Operates within the same network segment.

---

## Layer 3 Switch

A Layer 3 switch combines switching and routing functionality.

It operates at:

```text
OSI Layer 2 + Layer 3
```

### Capabilities

Layer 3 switches can:

* Forward frames using MAC addresses.
* Route packets using IP addresses.

This allows them to perform some functions traditionally handled by routers.

---

## VLAN (Virtual Local Area Network)

### What is a VLAN?

A VLAN allows a physical network to be logically divided into multiple separate networks.

Even though devices may connect to the same switch, VLANs can isolate communication between groups of devices.

---

## Example VLAN Segmentation

```text
Sales Department VLAN
Accounting Department VLAN
```

Both departments can:

* Access the Internet.
* Use shared infrastructure.

However:

* Sales cannot directly communicate with Accounting.
* Accounting cannot directly communicate with Sales.

---

## Benefits of VLANs

### Security

Network traffic is isolated between departments.

### Segmentation

Devices can be grouped based on business requirements.

### Access Control

Communication rules can be enforced between VLANs.

### Better Network Management

Administrators can organize devices more efficiently.

---

## Router vs Switch

| Feature                     | Router           | Switch             |
| --------------------------- | ---------------- | ------------------ |
| Primary Function            | Connect Networks | Connect Devices    |
| OSI Layer                   | Layer 3          | Layer 2 or Layer 3 |
| Uses IP Addresses           | Yes              | Layer 3 Only       |
| Uses MAC Addresses          | No               | Yes                |
| Performs Routing            | Yes              | Layer 3 Only       |
| Connects Different Networks | Yes              | No (Layer 2)       |

---

## Key Notes

* Routers connect different networks and perform routing.
* Routing determines the best path for data transmission.
* Routers operate at OSI Layer 3.
* Switches connect devices within a network.
* Layer 2 switches forward frames using MAC addresses.
* Layer 3 switches can forward frames and route packets.
* VLANs provide logical separation inside a network.
* VLANs improve security and network organization.

---

## Learning Outcome

After completing this section, I understood the roles of routers and switches in LAN environments. I learned how routing determines the optimal path for network traffic, how Layer 2 and Layer 3 switches operate, and how VLAN technology provides network segmentation and improved security within shared network infrastructures.
