# Layer 3 - Network

## Overview

This task introduced the Network Layer, which is Layer 3 of the OSI Model. The Network Layer is responsible for routing data between networks and determining the most efficient path for data to travel from a source device to its destination. It also uses IP addresses to identify devices across networks.

---

## Objectives

* Understand the purpose of the Network Layer.
* Learn how routing works within a network.
* Understand the role of IP addresses.
* Learn how data is forwarded between networks.
* Become familiar with Layer 3 networking devices.

---

## Tools Used

* No tools were used in this task.

---

## Methodology / Steps

### 1. Understanding the Network Layer

The Network Layer is Layer 3 of the OSI Model.

Its primary responsibilities include:

* Routing data between networks.
* Determining the best path for data transmission.
* Managing communication using IP addresses.
* Reassembling transmitted data when required.

---

### 2. Routing Data

Routing is the process of determining how data travels from a source device to a destination device.

The Network Layer evaluates available routes and selects the most suitable path for packet delivery.

Its goal is to ensure efficient and reliable communication across networks.

---

### 3. Factors Used in Route Selection

Several factors influence the route selected by networking devices.

#### Shortest Path

The route containing the fewest intermediary devices is often preferred.

Purpose:

* Reduce travel distance.
* Improve delivery efficiency.

---

#### Reliability

The network considers whether packets have previously been lost on a route.

Purpose:

* Increase delivery success.
* Avoid unstable connections.

---

#### Connection Speed

The physical medium used by a route can affect performance.

Examples:

* Copper Connections
* Fibre Connections

Purpose:

* Select faster transmission paths when available.

---

### 4. Routing Protocols

Routing protocols help devices determine the most efficient route for data transmission.

Examples introduced in this task:

* OSPF (Open Shortest Path First)
* RIP (Routing Information Protocol)

These protocols assist routers in making routing decisions across networks.

---

### 5. IP Addressing

The Network Layer operates using IP addresses.

Example:

```text
192.168.1.100
```

IP addresses provide logical identification for devices and allow data to be routed between different networks.

---

### 6. Layer 3 Devices

Devices that operate at the Network Layer are known as Layer 3 devices.

Example:

* Routers

Responsibilities:

* Forward packets between networks.
* Make routing decisions.
* Deliver data using IP addressing.

---

### 7. Communication Process

The communication process at the Network Layer follows these steps:

1. Data arrives from the upper layers.
2. The destination IP address is examined.
3. The best route is determined.
4. Data is forwarded toward its destination.
5. Packets are delivered across one or more networks.

---

## Commands

No commands were used in this task.

---

## Key Findings / Notes

* The Network Layer is Layer 3 of the OSI Model.
* It is responsible for routing data between networks.
* IP addresses are used for logical device identification.
* Routing determines the best path for data transmission.
* Route selection considers distance, reliability, and connection speed.
* OSPF and RIP are examples of routing protocols.
* Routers are common Layer 3 devices.
* The Network Layer enables communication beyond a local network.

---

## Learning Outcome

After completing this task, I understood how the Network Layer routes data between networks using IP addresses. I learned how routing decisions are made, the factors that influence path selection, and the role of routers and routing protocols in delivering network traffic efficiently.
