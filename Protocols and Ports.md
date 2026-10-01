
# Transport Layer Basics & Port Multiplexing

## Overview
- Layers covered so far:
  - **Link Layer (Ethernet):** Uses **MAC addresses** to move frames between hosts on the same network segment.
  - **Internet Layer (IP):** Uses **IP addresses** to provide addressing and routing across networks.
- Next layer up: **Transport Layer** (TCP/IP stack).
- **Core Role:** Handles communication between applications running on different (or the same) hosts.

---

## Transport Layer Functions & Port Assignment

### Application Identification
- A single host communicates with many hosts using multiple data streams simultaneously.
- The Transport layer identifies specific network applications using **Port Numbers**.
- **Port Number Range:** `0` to `65535`

### Examples of Standard Ports
| Application / Protocol | Port Number |
|------------------------|-------------|
| **HTTP** (Web Browsing) | Port `80` |
| **SMTP** (Email Transmission) | Port `25` |

### Multiplexing
- Multiple distinct application data streams (e.g., several HTTP sessions and email transfers) are combined (**multiplexed**) onto a single physical/logical network link using their port numbers.

---

## How Port Numbers Work in Conversations

Each host assigns **two port numbers** for every communication session:

```

[ Client Host ] [ Server Host ] Source Port: 47747 (Random) --- Request ---> Destination Port: 80 (HTTP) Destination Port: 80 (HTTP) <--- Response --- Source Port: 80 (HTTP)

```

| Parameter | Client Side (Request) | Server Side (Reply) |
|-----------|------------------------|----------------------|
| **Destination Port** | Set to the **service port** requested (e.g., `80` for HTTP) | Set to the **client's random port** (e.g., `47747`) |
| **Source Port** | Set to a **random client-assigned port** (e.g., `47747`) | Set to the **service port** (e.g., `80`) |

> **Key Benefit:** Dynamic client source ports allow a single host to maintain multiple simultaneous "conversations" (tabs or connections) using the exact same application protocol.

---

## Transport Protocols in TCP/IP
Two core protocols manage port assignments and transport data in the TCP/IP suite:
1. **TCP** (Transmission Control Protocol)
2. **UDP** (User Datagram Protocol)

---

## Quick Summary
- **Transport Layer** manages host-to-host application traffic.
- **Ports (0–65535)** identify specific applications and multiplex traffic over a single network link.
- **Client** uses a random source port + fixed destination service port (e.g., 80).
- **Server** flips source and destination ports in response packets to track unique sessions.
- **Protocols:** Implemented primarily via **TCP** and **UDP**.




Communications at the transport layer
![A network diagram illustrating how different types of data traffic flow from two hosts (2.2 and 2.3) to another host (2.1) over a network.](https://cdn.testout.com/a-plus-220-120x-en-us/materials/resources/text/s_protocols_and_ports/aplus_fig06_03_01.png)