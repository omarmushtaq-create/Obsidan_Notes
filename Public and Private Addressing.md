
## Public vs Private Addresses
- To use the **Internet**, a host needs a **unique public IP address**
- Public addresses = allocated to customer networks by the **ISP**
- Problem: not enough public IPv4 addresses for every device
- Solution: use **private addressing** + workarounds

---

## Private Address Ranges (RFC 1918)
- Reserved for **private LANs only**
- Cannot be routed on the **public Internet**

| Class | Range |
|-------|-------|
| **Class A (private)** | 10.0.0.0 - 10.255.255.255 |
| **Class B (private)** | 172.16.0.0 - 172.31.255.255 |
| **Class C (private)** | 192.168.0.0 - 192.168.255.255 |

> These are the "RFC 1918" ranges - the document that defined them.

---

## Address Classes and Default Subnet Masks

### Background
- Classes (A, B, C) come from the **earliest version of IP**
- Originally, IP had **no subnet masks** - the address class alone told you the network ID
- "Default masks" = masks that line up exactly with **octet boundaries** (matching the old class system)

### Class Table

| Class | 1st Octet Range | Dotted Decimal Mask | Prefix | Binary Mask |
|-------|-------------------|------------------------|--------|--------------|
| **A** | 0-127 | 255.0.0.0 | /8 | 11111111.00000000.00000000.00000000 |
| **B** | 128-191 | 255.255.0.0 | /16 | 11111111.11111111.00000000.00000000 |
| **C** | 192-223 | 255.255.255.0 | /24 | 11111111.11111111.11111111.00000000 |

> **Simple way to remember:** Prefix number = how many bits (from the left) are "network" bits.
> - /8 = first octet is network, rest is host
> - /16 = first two octets are network
> - /24 = first three octets are network

### Other Classes (Reserved, Not for Normal Hosts)
| Class | 1st Octet Range | Purpose |
|-------|-------------------|---------|
| D | 224-239 | Multicast groups |
| E | 240-255 | Experimental / future use |

---

## Getting Internet Access with Private Addresses
A host with a **private IP** can't reach the Internet directly. Two common solutions:

### 1. NAT (Network Address Translation)
- A **router** is configured with **one or more public IP addresses**
- Router uses **NAT** to translate **private <-> public** addresses
- Most common method (used in home routers)

### 2. Proxy Server
- A **proxy server** makes Internet requests **on behalf of** private clients
- Client never directly touches the Internet - proxy does it for them

---

## Quick Summary
- Public IP = needed for direct Internet access (from ISP)
- Private IP ranges (RFC 1918): 10.x.x.x, 172.16-31.x.x, 192.168.x.x
- Address classes A/B/C = old system, tied to **default subnet masks** (/8, /16, /24)
- Class D = multicast, Class E = experimental
- Private hosts reach the Internet via **NAT** (router) or a **proxy server**
