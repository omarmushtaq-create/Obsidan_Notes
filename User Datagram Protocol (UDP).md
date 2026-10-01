

## Overview
- **Trade-off:** Speed vs. Reliability.
- While TCP prioritizes reliability, **User Datagram Protocol (UDP)** prioritizes **speed and reduced overhead**.
- **Key Characteristic:** UDP is a **connectionless**, non-guaranteed transport protocol.
- **No Guarantees:** 
  - No connection setup (no 3-way handshake).
  - No packet delivery guarantees.
  - No packet reordering (no sequence numbers).
  - No error correction/acknowledgments (no ACKs/NACKs).

---

## UDP Characteristics vs. TCP

| Feature | TCP | UDP |
|---------|-----|-----|
| **Connection Type** | Connection-oriented | Connectionless |
| **Reliability** | Guaranteed delivery (ACKs/NACKs) | Best-effort ("fire and forget") |
| **Ordering** | Guaranteed via sequence numbers | Out-of-order delivery possible |
| **Overhead** | High ($\ge$ 20-byte header) | Extremely low (8-byte header) |
| **Speed** | Slower (latency from handshakes/ACKs) | Faster (minimal latency) |
| **Broadcast Support** | No (unicast only) | **Yes** (supports unicast, broadcast, multicast) |

---

## When to Use UDP

UDP is ideal when applications:
1. Transfer **time-sensitive data** where speed matters more than 100% completeness.
2. Can tolerate minor packet loss (loss results in brief glitches rather than connection failures).
3. Need **broadcast transmissions** (not supported by TCP).
4. Handle their own reliability at the Application Layer if needed.

---

## Common UDP Protocol Examples

### 1. Real-time Audio/Video & Streaming (Voice / VoIP / Video Calls)
- Small data losses cause minor audio/video stuttering or dropouts ("glitches").
- Retransmitting delayed packets via TCP would be useless because real-time media cannot wait for old packets.

### 2. Dynamic Host Configuration Protocol (DHCP)
- Used by clients to automatically request IP configuration parameters from a network server.
- Uses **broadcast messages** to locate servers, which TCP cannot perform.
- Simple mechanism: If no response arrives, the client simply retries after a timeout.

### 3. Trivial File Transfer Protocol (TFTP)
- Lightweight file transfer protocol often used by network equipment to fetch firmware or configuration files.
- Uses UDP because the **application layer itself** handles simple acknowledgment messages, making TCP's transport reliability redundant.

---

## Quick Summary
- **UDP** = Connectionless, fast, best-effort transport protocol with low overhead.
- **No Handshakes, ACKs, NACKs, or Sequence Numbers.**
- **Supports Broadcasts** (unlike TCP).
- **Primary Use Cases:** Real-time streaming/VoIP, DHCP, TFTP, DNS queries.

Observing a UDP header in the final frame of the DHCP lease process with the Wireshark protocol analyzer![A screenshot of a network packet capture tool Wireshark, displaying D H C P traffic filtered by U D P ports 67 and 68.](https://cdn.testout.com/a-plus-220-120x-en-us/materials/resources/text/s_protocols_and_ports/4501-1638440375934-wireshark_udp_header_dhcp_dora.png)