# Extending Your Network

## Introduction to Port Forwarding

### Overview

Port Forwarding is a networking technique that allows devices and services inside a private network to become accessible from external networks, including the Internet. Without port forwarding, services hosted within a local network can only be accessed by devices on that same network.

---

## What is Port Forwarding?

Port Forwarding is the process of directing incoming network traffic from a public IP address to a specific device and service inside a private network.

It allows external users to access internally hosted services such as:

* Web Servers
* Game Servers
* FTP Servers
* Remote Access Services

---

## Why is Port Forwarding Needed?

By default, devices inside a private network are only reachable by other devices on the same network.

### Example Scenario

Private Network:

```text
Web Server IP: 192.168.1.10
Service Port: 80
```

Without Port Forwarding:

* Devices inside the network can access the web server.
* Devices outside the network cannot access the web server.

This creates an internal-only environment known as an:

```text
Intranet
```

---

## How Port Forwarding Works

To make an internal service accessible from the Internet:

1. A public IP address is assigned to the network.
2. The router receives incoming requests.
3. The router forwards specific traffic to the internal device.
4. The internal service responds to the request.

### Example

```text
Public IP: 82.62.51.70
Port: 80
```

Router forwards requests to:

```text
192.168.1.10:80
```

As a result:

* External users access the public IP.
* The router redirects traffic to the internal web server.

---

## Port Forwarding vs Firewall

These concepts are often confused but perform different functions.

### Port Forwarding

Purpose:

* Directs traffic to an internal device.
* Opens a pathway to a specific service.

Example:

```text
Internet → Router → Internal Web Server
```

---

### Firewall

Purpose:

* Controls whether traffic is allowed or blocked.
* Filters incoming and outgoing network traffic.

Even if a port is forwarded, a firewall can still block access.

---

## Where is Port Forwarding Configured?

Port Forwarding is configured on the network router.

The router acts as the gateway between:

* Private Network
* Public Internet

It determines where incoming traffic should be sent.

---

## Key Notes

* Port Forwarding allows external access to internal services.
* Internal services are normally accessible only within the local network.
* Public IP addresses are used to expose services to the Internet.
* Routers perform the forwarding process.
* Port Forwarding and Firewalls serve different purposes.
* A firewall can block traffic even if a port is forwarded.
* Commonly used for web servers, remote access services, and application hosting.

---

## Learning Outcome

After completing this section, I understood how port forwarding enables communication between external users and internal network services. I learned the role of routers in forwarding traffic, the difference between port forwarding and firewalls, and how organizations expose services such as web servers to the Internet.
