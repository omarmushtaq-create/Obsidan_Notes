

## Overview
- **The Problem:** IP is inherently unreliable—packets can be lost, damaged, or arrive out of order due to network faults or congestion.
- **The Solution:** **TCP (Transmission Control Protocol)** operates at the Transport Layer to add reliability and order on top of IP.
- **Key Characteristic:** TCP is a **connection-oriented** protocol, meaning it establishes and maintains a verified logical connection between sender and receiver before exchanging application data.

---

## How TCP Ensures Reliability

| Reliability Mechanism                | Function                                                                                            |
| ------------------------------------ | --------------------------------------------------------------------------------------------------- |
| **Three-Way Handshake**              | Establishes the connection using `SYN` $\rightarrow$ `SYN/ACK` $\rightarrow$ `ACK` packets.         |
| **Sequence Numbers**                 | Assigns every packet a sequence number so data can be reassembled in the correct order and tracked. |
| **Acknowledgements (ACK)**           | Receiver sends an `ACK` to confirm packets were successfully received.                              |
| **Negative Acknowledgements (NACK)** | Receiver prompts a retransmission if a packet is detected as missing or corrupted.                  |
| **Session Termination**              | Gracefully closes the connection when data transfer is finished using a `FIN` handshake.            |
|                                      |                                                                                                     |

---

## The Overhead Trade-off
- **Drawback:** The reliable, connection-oriented nature of TCP comes with additional protocol overhead.
- **Header Size:** A TCP header adds **20 bytes or more** to the size of every IP packet (compared to simpler protocols like UDP).

---

## When to Use TCP
TCP is used whenever an application **cannot tolerate missing or damaged data** (where reliability is more critical than raw speed).

### Common Examples Requiring TCP
- **HTTPS (HyperText Transfer Protocol Secure):** Delivers encrypted web content. Missing or corrupted packets break encryption/decryption, causing the session to fail entirely.
- **SSH (Secure Shell):** Secure, encrypted command-line access. Integrity is essential; missing packets disrupt session security and execution.

---

## Quick Summary
- **TCP** = Connection-oriented, reliable transport protocol.
- **3-Way Handshake:** `SYN` $\rightarrow$ `SYN/ACK` $\rightarrow$ `ACK`.
- **Reliability Tools:** Sequence numbers, ACKs, NACKs (retransmissions), graceful `FIN` teardown.
- **Header Overhead:** Adds $\ge$ **20 bytes** per packet.
- **Use Cases:** Apps requiring 100% data integrity (e.g., HTTPS, SSH, Web, File Transfers).

Observing the TCP handshake with the Wireshark protocol analyzer
![A screenshot of a packet analysis tool, likely Wireshark, displaying network traffic and details of a specific packet.](https://cdn.testout.com/a-plus-220-120x-en-us/materials/resources/text/s_protocols_and_ports/4860-1636638670081-06b-lab_01_wireshark_tcp_handshake.png)