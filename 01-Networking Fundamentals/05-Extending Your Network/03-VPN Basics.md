# Extending Your Network

## VPN Basics

### Overview

A Virtual Private Network (VPN) is a technology that enables secure communication between devices located on different networks by creating an encrypted connection, known as a tunnel, over the Internet.

Devices connected through a VPN can communicate as if they were part of the same private network, even when they are geographically separated.

---

## What is a VPN?

VPN stands for:

```text
Virtual Private Network
```

A VPN creates a secure tunnel between devices across the Internet, allowing data to travel safely between them.

This tunnel forms a private communication path that is isolated from normal Internet traffic.

---

## How a VPN Works

Normally, devices can only directly communicate with other devices on the same network.

A VPN extends this capability by securely connecting separate networks together.

### Example Scenario

```text
Network #1 → Office 1
Network #2 → Office 2
Network #3 → VPN Tunnel Network
```

Devices connected through the VPN:

* Remain part of their original networks.
* Simultaneously become members of a secure private VPN network.
* Can communicate securely across the Internet.

---

## Benefits of VPN Technology

### Connecting Multiple Locations

VPNs allow organizations to connect offices and remote locations securely.

#### Example

```text
Office A ↔ VPN ↔ Office B
```

Benefits:

* Shared access to servers.
* Access to centralized infrastructure.
* Secure communication between locations.

---

### Privacy Protection

VPNs use encryption to secure transmitted data.

Because traffic is encrypted:

* Unauthorized users cannot easily read the data.
* Network sniffing becomes significantly more difficult.
* Public Wi-Fi connections become safer.

#### Example

When using public Wi-Fi:

```text
User → Encrypted VPN Tunnel → Destination
```

Even if someone intercepts the traffic, the encrypted data is difficult to understand.

---

### Online Anonymity

VPNs can help hide network activity from intermediaries.

Without a VPN:

```text
User → ISP → Internet
```

With a VPN:

```text
User → VPN Tunnel → Internet
```

Benefits:

* Reduces visibility of browsing activity.
* Provides additional privacy protection.
* Commonly used by journalists and activists operating in restrictive environments.

### Important Note

The level of anonymity depends on the VPN provider's privacy practices.

If a VPN provider stores activity logs, privacy benefits may be reduced.

---

## VPN Usage in TryHackMe

TryHackMe uses VPN technology to connect users to vulnerable machines securely.

Benefits include:

### Secure Access

Users can safely interact with lab environments.

### ISP Protection

Internet Service Providers are less likely to interpret lab activity as malicious external attacks.

### Platform Security

Vulnerable machines remain inaccessible from the public Internet.

This reduces exposure and improves overall platform security.

---

## Common VPN Technologies

### PPP (Point-to-Point Protocol)

PPP provides:

* Authentication
* Data Encryption

It works using:

```text
Private Key + Public Certificate
```

Both must match for successful authentication.

#### Characteristics

* Provides secure communication.
* Non-routable by itself.
* Requires another protocol to transport traffic.

---

### PPTP (Point-to-Point Tunneling Protocol)

PPTP enables PPP traffic to travel across networks and the Internet.

#### Advantages

* Easy to configure.
* Supported by many devices.

#### Disadvantages

* Weak encryption compared to modern alternatives.
* Considered less secure today.

---

### IPSec (Internet Protocol Security)

IPSec secures communication using the existing IP framework.

#### Advantages

* Strong encryption.
* Widely supported.
* Enterprise-grade security.

#### Disadvantages

* More difficult to configure.
* Requires additional setup and management.

---

## VPN Technology Comparison

| Technology | Purpose                     | Advantages            | Limitations           |
| ---------- | --------------------------- | --------------------- | --------------------- |
| PPP        | Authentication & Encryption | Secure authentication | Non-routable          |
| PPTP       | VPN Tunneling               | Easy setup            | Weak encryption       |
| IPSec      | Secure IP Communication     | Strong encryption     | Complex configuration |

---

## Key Notes

* VPN stands for Virtual Private Network.
* VPNs create encrypted tunnels over the Internet.
* Devices on separate networks can securely communicate through a VPN.
* VPNs provide privacy, security, and limited anonymity.
* Encryption protects data from interception.
* TryHackMe uses VPN technology to provide secure lab access.
* PPP provides authentication and encryption.
* PPTP transports PPP traffic across networks.
* IPSec provides strong encryption using the IP framework.

---

## Learning Outcome

After completing this section, I understood how VPN technology securely connects devices across different networks using encrypted tunnels. I learned the security, privacy, and connectivity benefits of VPNs, explored real-world use cases, and gained an understanding of common VPN technologies including PPP, PPTP, and IPSec.
