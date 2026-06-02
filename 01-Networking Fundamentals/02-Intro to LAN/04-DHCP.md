# DHCP (Dynamic Host Configuration Protocol)

## Overview

This task introduced the Dynamic Host Configuration Protocol (DHCP), a network protocol used to automatically assign IP addresses to devices when they join a network. DHCP simplifies network management by eliminating the need for manual IP address configuration.

---

## Objectives

* Understand the purpose of DHCP.
* Learn how devices obtain IP addresses automatically.
* Understand the DHCP communication process.
* Identify the four stages of DHCP address assignment.
* Learn the role of a DHCP server in a network.

---

## Tools Used

* No tools were used in this task.

---

## Methodology / Steps

### 1. Understanding DHCP

Devices require an IP address to communicate on a network.

IP addresses can be assigned in two ways:

#### Manual Assignment

* IP addresses are configured manually by a user or administrator.
* Requires individual configuration on each device.

#### Automatic Assignment

* IP addresses are assigned automatically by a DHCP server.
* Simplifies network administration and device deployment.

---

### 2. Role of a DHCP Server

A DHCP server is responsible for:

* Assigning IP addresses to devices.
* Managing available IP address ranges.
* Preventing IP address conflicts.
* Automating network configuration.

When a device connects to a network without an IP address, it communicates with the DHCP server to obtain one.

---

### 3. DHCP Communication Process

DHCP follows a four-step process commonly known as the DORA process.

---

#### Step 1: DHCP Discover

The device broadcasts a request across the network searching for a DHCP server.

Purpose:

* Locate available DHCP servers.
* Request network configuration information.

---

#### Step 2: DHCP Offer

The DHCP server responds with an available IP address.

Purpose:

* Offer a valid IP address to the requesting device.

---

#### Step 3: DHCP Request

The device responds to the DHCP server indicating that it wants to use the offered IP address.

Purpose:

* Accept the offered IP address.

---

#### Step 4: DHCP ACK (Acknowledgement)

The DHCP server confirms the assignment.

Purpose:

* Finalize the IP address allocation.
* Allow the device to begin network communication.

---

### 4. DHCP Workflow

The complete DHCP process follows this sequence:

```text
DHCP Discover
      ↓
DHCP Offer
      ↓
DHCP Request
      ↓
DHCP ACK
```

This process automatically provides the device with a valid IP address and network configuration.

---

## Commands

No commands were used in this task.

---

## Key Findings / Notes

* DHCP stands for Dynamic Host Configuration Protocol.
* DHCP automatically assigns IP addresses to devices.
* A DHCP server manages and distributes available IP addresses.
* Automatic assignment reduces manual configuration effort.
* DHCP uses a four-step communication process.
* The four DHCP stages are Discover, Offer, Request, and Acknowledgement (DORA).
* Devices cannot communicate on a network until they have a valid IP address.

---

## Learning Outcome

After completing this task, I understood how DHCP automatically assigns IP addresses to devices and learned the four-step DORA process (Discover, Offer, Request, and ACK) used to establish network connectivity.
