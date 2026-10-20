
## Real-Time vs Bursty Traffic

### Real-Time Traffic
- "Real time" = services like **voice and video**
- Example: **VoIP (Voice over IP)** = voice calling over data networks
- **Poor VoIP symptoms:** dropouts, echo, glitches in the call

### Bursty (Ordinary) Data
- Examples: **HTTP, FTP, email**
- Goal: transfer as fast as possible
- **Packet order** and **variable gaps** between packets don't matter much

### The Key Difference

| Traffic Type | Packet Loss | Delays / Out-of-order Packets |
|--------------|-------------|-------------------------------|
| **Bursty** (HTTP, FTP, email) | **Sensitive** | **Tolerant** |
| **Real-time** (VoIP, video) | **Tolerant** (can handle some loss) | **Very sensitive** |

---

## Latency and Jitter

### Latency
- **Time for a signal to reach the recipient**, measured in **milliseconds (ms)**
- Increases with **distance**
- Made worse by **processing delays** at routers and other intermediate systems
- **VoIP limit:** max about **150 ms one-way**
- **RTT (Round Trip Time)** = two-way latency (time to get a response to a probe)

### Jitter
- **Variation in delay over time**
- Measured by sampling the **time between packets arriving**
- **VoIP tolerance:** about **30 ms** (using **buffering**) without a serious drop in call quality
- Usually caused by **network congestion** affecting packet processing on routers/switches

| Term | Meaning | VoIP Limit |
|------|---------|-------------|
| **Latency** | Delay for a signal to arrive | ~150 ms one-way |
| **Jitter** | Variation in that delay | ~30 ms |

---

## QoS (Quality of Service)

### What It Is
- A mechanism where **switches, APs, and routers** are all configured to:
  - **Identify VoIP data**
  - **Prioritize it** over bursty data
- Only way to really ensure good VoIP call quality

### Where It Works
| Network | QoS Support |
|---------|--------------|
| **Enterprise** | Sophisticated QoS + traffic engineering on managed switches/routers |
| **Public (Internet)** | **Hard to guarantee** QoS |
| **SOHO** | Basic QoS or **bandwidth control** on the router/modem |

### SOHO Example
- Prioritize the **port used by a VoIP app** over all other protocols
- Helps when, for example:
  - One PC is downloading a **large Windows update**
  - While others are in a **video conference**
- Router interface (TP-Link example): **Advanced -> Bandwidth Control**
  - Set **line type** and **total upstream/downstream bandwidth**
  - Add **controlling rules** with **priority** and **min/max up/down** rates

---

## Measuring Latency and Jitter
- Use the router's **management interface** to view **latency** (and possibly **jitter**)
- If not available, use a **speed test site** to measure **latency and bandwidth**
- If latency is **persistently above the agreed service level**, **contact your ISP**

---

## Quick Summary
- **Real-time apps** (VoIP, video) need **steady, in-order, on-time** delivery; they can tolerate some **packet loss**
- **Bursty apps** (HTTP, FTP, email) tolerate **delay** but not **packet loss**
- **Latency** = delay (VoIP max ~150 ms one-way) | **Jitter** = delay variation (VoIP ~30 ms)
- **QoS** = prioritizes VoIP/real-time traffic across switches, APs, and routers
- SOHO routers may offer **bandwidth control** for basic QoS
- Check latency via router interface or speed test; **persistent high latency -> call the ISP**
