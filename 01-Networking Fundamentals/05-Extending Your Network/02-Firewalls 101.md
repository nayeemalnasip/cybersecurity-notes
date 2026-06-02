# Extending Your Network

## Firewalls 101

### Overview

A Firewall is a security device that monitors and controls network traffic entering and leaving a network. It acts as a protective barrier between trusted and untrusted networks by allowing or blocking traffic based on predefined security rules.

---

## What is a Firewall?

A firewall is responsible for determining whether network traffic should be allowed or denied.

Think of a firewall as border security for a network:

* Permitted traffic is allowed to pass.
* Suspicious or unauthorized traffic is blocked.

Firewalls help organizations protect systems, services, and sensitive information from unwanted access.

---

## How Firewalls Make Decisions

Firewalls inspect packets and evaluate several factors before allowing communication.

### Common Inspection Criteria

#### Source

Determines where the traffic is coming from.

Example:

```text
Allow traffic from Network A
Block traffic from Network B
```

---

#### Destination

Determines where the traffic is trying to go.

Example:

```text
Allow traffic to Internal Server
Block traffic to Restricted Network
```

---

#### Port

Determines which service the traffic is attempting to access.

Example:

```text
Allow Port 80 (HTTP)
Allow Port 443 (HTTPS)
Block all other ports
```

---

#### Protocol

Determines the communication protocol being used.

Example:

```text
Allow TCP
Allow UDP
Allow Both
Block Specific Protocols
```

---

## Packet Inspection

Firewalls use packet inspection to analyze network traffic.

During inspection, the firewall examines information such as:

* Source Address
* Destination Address
* Port Numbers
* Protocol Type

Based on configured rules, the firewall decides whether the packet should be allowed or blocked.

---

## Types of Firewalls

Firewalls can exist in different forms:

### Hardware Firewalls

Dedicated security appliances commonly used in:

* Enterprises
* Data Centers
* Large Organizations

Advantages:

* High performance
* Handles large volumes of traffic

---

### Software Firewalls

Installed directly on operating systems or servers.

Example:

```text
Snort
```

Advantages:

* Flexible configuration
* Host-level protection

---

## Stateful Firewall

A Stateful Firewall analyzes the entire connection rather than evaluating packets individually.

### Characteristics

* Tracks active connections.
* Makes decisions based on connection behavior.
* Dynamically evaluates traffic.

### Advantages

* Better understanding of network sessions.
* More intelligent filtering decisions.
* Can identify suspicious connection behavior.

### Disadvantages

* Consumes more system resources.
* Requires more processing power.
* Slower compared to stateless alternatives.

### Example

If a connection becomes malicious, the firewall can block the entire connection or host.

---

## Stateless Firewall

A Stateless Firewall evaluates each packet independently using predefined rules.

### Characteristics

* No awareness of previous packets.
* Each packet is inspected individually.
* Uses static rule sets.

### Advantages

* Fast processing.
* Low resource consumption.
* Effective for handling large traffic volumes.

### Disadvantages

* Less intelligent than stateful firewalls.
* Cannot understand connection context.
* Depends entirely on accurate rule configuration.

### Example

A malicious packet may be blocked while other packets from the same device are still allowed.

---

## Stateful vs Stateless Firewall

| Feature               | Stateful Firewall             | Stateless Firewall     |
| --------------------- | ----------------------------- | ---------------------- |
| Connection Awareness  | Yes                           | No                     |
| Decision Making       | Dynamic                       | Static                 |
| Resource Usage        | Higher                        | Lower                  |
| Security Intelligence | Higher                        | Lower                  |
| Performance           | Slower                        | Faster                 |
| Suitable For          | Complex Security Environments | High Traffic Filtering |

---

## Key Notes

* Firewalls control incoming and outgoing network traffic.
* Firewall decisions are based on source, destination, ports, and protocols.
* Packet inspection is used to evaluate network traffic.
* Hardware and software firewalls provide different deployment options.
* Stateful firewalls analyze entire connections.
* Stateless firewalls inspect packets individually.
* Stateful firewalls provide stronger security but require more resources.
* Stateless firewalls provide faster performance but rely heavily on predefined rules.

---

## Learning Outcome

After completing this section, I understood the purpose of firewalls in network security and how they control traffic entering and leaving a network. I learned how packet inspection works, the factors used to make filtering decisions, and the differences between stateful and stateless firewalls, including their advantages, limitations, and real-world use cases.
