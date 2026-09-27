
## Wi-Fi 5 (802.11ac)

### Band
- Works **only in 5 GHz**
- Dual-band AP: 2.4 GHz radio handles legacy clients (802.11g/n)
- Tri-band AP: 1x 2.4 GHz radio + 2x 5 GHz radios

### Streams
- Supports up to **8 streams** (theoretical)
- Most real APs only support **4x4 streams**
- Single stream over **80 MHz channel** = **433 Mbps** nominal

### Channel Bonding
- Supports wider bonded channels: **80 MHz and 160 MHz**

### Marketing (AC values)
Example: **AC5300**

| Radio            | Streams | Channel  | Speed      |
|------------------|---------|----------|------------|
| 2.4 GHz          | 2x2     | 40 MHz   | 1,000 Mbps |
| 5 GHz (radio 1)  | 4x4     | 80 MHz   | 2,166 Mbps |
| 5 GHz (radio 2)  | 4x4     | 80 MHz   | 2,166 Mbps |

> Total marketed = **5300** (combined, not real-world combined throughput)

> **Important:** Marketing numbers (N, AC, AX labels) don't mathematically "add up" cleanly with per-stream rates. They're only useful for **relative comparison**, not literal math.

---

### MU-MIMO (Multiuser MIMO)
- Normally: AP talks to **one station at a time**, others queue
- Wi-Fi 5 introduces **Downlink MU-MIMO (DL MU-MIMO)**
  - AP uses multiple antennas to send data to **up to 4 clients simultaneously**

---

## Wi-Fi 6 (802.11ax)

### Speed Improvement
- Per-stream rate over 80 MHz channel: **600 Mbps** (up from 433 Mbps in Wi-Fi 5)

### Marketing (AX values)
Example: **AX6000**
- 2.4 GHz radio: **1,148 Mbps**
- 5 GHz radio: **4,804 Mbps**

### Bands
- Works in **2.4 GHz and 5 GHz**
- **Wi-Fi 6E** = adds support for **6 GHz band**
  - 6 GHz = less range, but more frequency space
  - Easier to use **80/160 MHz channels** without congestion

### MU-MIMO Improvements
| Feature              | Wi-Fi 5         | Wi-Fi 6              |
|----------------------|-----------------|------------------------|
| Simultaneous clients | Up to 4 (5 GHz only) | Up to 8            |
| Uplink MU-MIMO       | No              | Yes                   |

- More simultaneous clients = **better performance in congested areas**

### OFDMA (New in Wi-Fi 6)
- **Orthogonal Frequency-Division Multiple Access**
- Works **alongside MU-MIMO**
- Improves **client density**
- Helps sustain **high data rates** even when many devices connect to same AP

---

## Quick Comparison Table

| Feature         | Wi-Fi 5 (802.11ac)        | Wi-Fi 6 (802.11ax)             |
| --------------- | ------------------------- | ------------------------------ |
| Bands           | 5 GHz only                | 2.4 GHz + 5 GHz (+6 GHz w/ 6E) |
| Max streams     | 8 (theoretical)           | More efficient per stream      |
| Per-stream rate | 433 Mbps (80 MHz)         | 600 Mbps (80 MHz)              |
| MU-MIMO         | Downlink only (4 clients) | Downlink + Uplink (8 clients)  |
| New tech        | MU-MIMO                   | OFDMA + Uplink MU-MIMO         |