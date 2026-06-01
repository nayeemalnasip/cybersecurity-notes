# Introducing LAN Topologies

## Overview

This task introduced Local Area Network (LAN) topologies and explained how devices can be connected within a network. Different topology designs were explored, including Star, Bus, and Ring topologies, along with the roles of switches and routers in network communication.

---

## Objectives

* Understand the concept of network topology.
* Learn the characteristics of Star, Bus, and Ring topologies.
* Identify the advantages and disadvantages of each topology.
* Understand the role of switches in a LAN.
* Understand the role of routers in network communication.

---

## Tools Used

* TryHackMe Interactive Lab

---

## Methodology / Steps

### 1. Understanding Network Topologies

A network topology refers to the physical or logical design of a network and how devices are connected.

The following topologies were studied:

* Star Topology
* Bus Topology
* Ring Topology

---

### 2. Star Topology

In a Star Topology, all devices connect to a central networking device such as a switch or hub.

#### Advantages

* Easy to scale and add new devices.
* Reliable communication between devices.
* Failure of one device does not affect others.

#### Disadvantages

* Requires more cabling.
* Higher implementation cost.
* Failure of the central device affects the entire network.

---

### 3. Bus Topology

In a Bus Topology, all devices share a single backbone cable for communication.

#### Advantages

* Easy to install.
* Cost-effective.
* Requires less networking equipment.

#### Disadvantages

* Prone to network congestion.
* Difficult to troubleshoot.
* Backbone cable failure affects the entire network.

---

### 4. Ring Topology

In a Ring Topology, devices form a circular connection and forward data around the network.

#### Advantages

* Less network congestion.
* Easier fault tracing.

#### Disadvantages

* Data may pass through multiple devices before reaching its destination.
* Failure of a device or cable can disrupt the entire network.

---

### 5. Understanding Switches

A switch is a networking device used to connect multiple devices within a LAN.

Functions:

* Connects devices using Ethernet ports.
* Tracks connected devices.
* Sends data directly to the intended destination.
* Reduces unnecessary network traffic.

---

### 6. Understanding Routers

A router connects multiple networks and forwards data between them.

Functions:

* Connects different networks.
* Performs routing.
* Determines paths for data transmission.
* Provides alternative communication routes when available.

---

### 7. Practical Exercise

The interactive lab demonstrated how different LAN topologies behave when failures occur.

The exercise focused on:

* Identifying single points of failure.
* Understanding network reliability.
* Observing how topology design affects communication.

---

## Commands

No commands were used in this task.

---

## Key Findings / Notes

* Network topology defines how devices are connected.
* Star Topology is the most common modern topology.
* Bus Topology relies on a single backbone cable.
* Ring Topology transfers data around a circular path.
* Switches improve communication efficiency by forwarding packets only to intended devices.
* Routers connect networks and manage data routing.
* Redundancy improves network reliability.

---

## Learning Outcome

After completing this task, I understood the design and functionality of Star, Bus, and Ring topologies, as well as the roles of switches and routers in network communication. I also learned how topology design impacts scalability, performance, and fault tolerance.
