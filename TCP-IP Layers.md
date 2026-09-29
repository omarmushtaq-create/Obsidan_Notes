

## Link Layer (Network Interface Layer)
- Job: puts **frames onto the physical network**
- No true "TCP/IP protocols" live here
- Uses local network tech: **Ethernet, Wi-Fi**
- Also includes WAN interfaces: **DSL, cable modems**

### Key Points
- Communication here = **local network segment only** (not between different networks)
- Data unit = **frame**
- Interfaces identified by = **MAC address**

---

## Internet Layer
- Handled by **IP (Internet Protocol)**
- Job: **packet addressing and routing** across a network of networks
- **End system host** = any device that communicates on an IP network (PC, laptop, mobile, server)
- Moving data between IP networks requires a **router** (intermediate system)

### ARP (Address Resolution Protocol)
- IP layer needs to connect to Link layer (MAC addresses)
- **ARP** = lets a host **look up the MAC address** associated with an IP address

### IP Delivery Characteristics
- IP = **best-effort delivery**
- **Unreliable** and **connectionless**
- Packets can be:
  - Lost
  - Delivered out of sequence
  - Duplicated
  - Delayed

---

## Transport Layer
- Job: manages **multiple connections** for different application protocols **at the same time**
- Implemented by **one of two protocols**:

### TCP (Transmission Control Protocol)
- **Connection-oriented**
- **Guarantees delivery**
- Can detect and recover from **lost/out-of-order packets**
- Fixes IP's unreliability
- Used by **most application protocols** (errors here can cause serious data problems)

### UDP (User Datagram Protocol)
- **Connectionless**, **unreliable**
- **Faster**, less overhead (no setup needed for reliable connection)
- Used for **time-sensitive** applications: voice, video
- Missing/out-of-order packets = minor glitch (not a crash)

| Protocol | Reliable? | Speed | Used For |
|----------|-----------|-------|----------|
| **TCP** | Yes | Slower (more overhead) | Web, email, file transfer |
| **UDP** | No | Faster (less overhead) | Voice, video, streaming |

---

## Application Layer
- Contains protocols that do **high-level functions** (not just addressing/transport)
- Used to:
  - Configure/manage network hosts
  - Run services like **web and email**
- Each application protocol uses a **TCP or UDP port** to let clients connect to servers

---

## Quick Summary (Layer Overview)

| Layer | Job | Data Unit | Key Protocols |
|-------|-----|-----------|----------------|
| **Link** | Physical delivery on local segment | Frame | Ethernet, Wi-Fi |
| **Internet** | Addressing + routing between networks | Packet | IP, ARP |
| **Transport** | Manage multiple app connections | Segment | TCP, UDP |
| **Application** | High-level services | Data | HTTP, SMTP, etc. |

