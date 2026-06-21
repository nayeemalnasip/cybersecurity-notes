# Ping (ICMP)

## Overview

Ping is a fundamental network diagnostic tool used to test connectivity between devices. It uses the Internet Control Message Protocol (ICMP) to determine whether a target device is reachable and to measure the time required for data to travel between devices.

---

## Objectives

* Understand the purpose of the Ping utility.
* Learn how ICMP is used for network communication testing.
* Measure network connectivity and response time.
* Perform basic network troubleshooting using Ping.

---

## Tools Used

* Ping
* ICMP (Internet Control Message Protocol)

---

## Methodology / Steps

### 1. Understanding Ping

Ping is a network utility that checks whether a device or host is reachable over a network.

It helps determine:

* Whether a connection exists.
* Whether a target device is responding.
* The reliability of a network connection.
* The time taken for packets to travel between devices.

---

### 2. How Ping Works

Ping uses ICMP packets to communicate with a target device.

The process consists of:

1. Sending an **ICMP Echo Request** packet to the target.
2. The target responds with an **ICMP Echo Reply** packet.
3. The round-trip time is measured and displayed.

This response time is commonly referred to as **latency**.

---

### 3. Performing a Ping Test

Ping can be used against:

* Devices on a local network
* Servers
* Websites
* Network infrastructure devices

Basic syntax:

```bash
ping <IP_Address>
```

or

```bash
ping <Website_URL>
```

Example:

```bash
ping 192.168.1.254
```

---

### 4. Understanding the Results

Example observation:

* 6 ICMP packets were sent.
* 6 ICMP packets were received.
* No packets were lost.
* Average response time was 4.16 ms.

This indicates:

* The target device is reachable.
* The connection is functioning correctly.
* Network latency is low.

---

## Commands

```bash
ping 192.168.1.254
```

```bash
ping tryhackme.com
```

---

## Key Findings / Notes

* Ping is used to test network connectivity.
* Ping operates using ICMP packets.
* ICMP Echo Request packets are sent to the target device.
* ICMP Echo Reply packets are returned by the target device.
* Ping measures the round-trip time between devices.
* Low response times generally indicate better network performance.
* Ping can be used against both IP addresses and domain names.
* Ping is available by default on operating systems such as Windows and Linux.

---

## Learning Outcome

After completing this task, I learned how Ping uses ICMP to test network connectivity, verify whether a target device is reachable, and measure network latency through Echo Request and Echo Reply packets.
