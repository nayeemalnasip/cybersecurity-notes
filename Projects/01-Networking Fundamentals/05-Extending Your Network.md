# Extending Your Network - Project Summary

## Project Overview

This project focused on expanding core networking knowledge by exploring how networks securely communicate beyond their local boundaries. Throughout the room, I learned about port forwarding, firewall technologies, routing, LAN networking devices, VPN concepts, and practical network traffic management through interactive simulations.

---

## Task Completion Process

### Understanding Port Forwarding

The first section introduced the concept of Port Forwarding and its role in exposing internal services to external networks.

I learned that routers are responsible for forwarding incoming traffic from a public network to a specific device and service inside a private network. This mechanism allows services such as web servers to become accessible over the Internet while still operating within a local network.

**Outcome:**

* Understood the purpose of Port Forwarding.
* Learned how internal services become externally accessible.
* Identified the router as the device responsible for Port Forwarding configuration.

---

### Exploring Firewall Technologies

The next section focused on understanding how firewalls protect networks by filtering traffic.

I learned that firewalls inspect traffic based on multiple factors such as source, destination, protocol, and port information. I also explored the differences between Stateful and Stateless firewalls.

**Key Concepts Learned:**

| Firewall Type | Function                                  |
| ------------- | ----------------------------------------- |
| Stateful      | Inspects and tracks entire connections    |
| Stateless     | Inspects individual packets independently |

**OSI Layers Used by Firewalls:**

```text
Layer 3 & Layer 4
```

**Outcome:**

* Understood how firewalls filter network traffic.
* Learned the difference between stateful and stateless inspection.
* Explored firewall decision-making processes.

---

### Firewall Practical Challenge

As part of the practical exercise, I configured firewall rules to prevent malicious traffic from reaching a web server.

The challenge required analyzing network traffic and blocking communication targeting Port 80 while allowing legitimate traffic to continue.

**Practical Activity Completed:**

```text
THM{FIREWALLS_RULE}
```

**Outcome:**

* Applied firewall filtering concepts in a simulated environment.
* Practiced identifying malicious traffic.
* Successfully implemented traffic control rules.

---

### Understanding Routers and Switches

I explored the role of routers and switches in network communication and infrastructure.

I learned that routers perform routing, which determines the best path for data to travel between networks. Additionally, I studied the different capabilities of Layer 2 and Layer 3 switches.

**Key Concepts Learned:**

```text
Router Function: Routing
```

**Switch Types:**

```text
Layer 2
Layer 3
```

**Outcome:**

* Understood how routers connect networks.
* Learned the differences between Layer 2 and Layer 3 switches.
* Explored packet forwarding and network segmentation concepts.

---

### Network Simulation Challenge

In the final practical exercise, I analyzed network communication and completed the simulator challenge successfully.

During the activity, I examined network logs, observed connection behavior, and identified handshake events occurring between communicating devices.

**Practical Activity Completed:**

```text
THM{YOU'VE_GOT_DATA}
```

**Network Analysis Result:**

```text
Handshake Entries: 5
```

**Outcome:**

* Practiced network traffic analysis.
* Reviewed communication flow between devices.
* Reinforced understanding of connection establishment processes.

---

## Skills Demonstrated

* Port Forwarding
* Router Configuration Concepts
* Firewall Fundamentals
* Stateful Firewall Analysis
* Stateless Firewall Analysis
* Traffic Filtering
* Network Security Controls
* Routing Fundamentals
* Layer 2 Switching
* Layer 3 Switching
* Network Traffic Analysis
* Packet Inspection
* Network Monitoring

---

## Project Conclusion

By completing this room, I gained practical knowledge of how modern networks are extended, secured, and managed. I explored the relationship between routers, switches, firewalls, and VPN-related technologies while applying traffic filtering and network analysis techniques in hands-on exercises. These concepts provide an important foundation for future cybersecurity, network defense, and penetration testing activities.
