

## Overview
- Wi-Fi = networking computer hosts
- Other wireless tech = used for **Personal Area Networking (PAN)**
  - Bluetooth
  - RFID
  - NFC

---

## Bluetooth

### Basics
- Connects **peripheral devices** (mice, keyboards, headphones, etc.) to PCs/mobiles
- Used to **share data** between two systems
- Common on: smartphones, tablets, wearables, speakers, headphones
- Uses **radio communications**
- Standard speed: up to **3 Mbps**
- Versions 3 & 4: can negotiate an **802.11 radio link** for large file transfers -> up to **24 Mbps**

### Range
| Version         | Max Range              |
|------------------|--------------------------|
| Earliest version | 10 m (30 ft)             |
| Newer versions   | 100+ ft (weak at max distance) |

### Pairing
- Bluetooth devices use **pairing** to authenticate and securely exchange data

---

### Bluetooth Low Energy (BLE)
- Introduced in **Version 4**
- Designed for **small, battery-powered devices**
- Sends **small amounts of data, infrequently**
- Device stays in **low-power state** until a monitoring app starts a connection
- **NOT backward compatible** with classic Bluetooth
  - BUT a device CAN support both standards at once

---

### Bluetooth 5 (Latest Standard)
| Feature            | Bluetooth 5           | vs Bluetooth 4       |
|---------------------|------------------------|------------------------|
| Range               | 240 m (800 ft)         | ~4x farther            |
| Speed               | 2x faster              | -                      |
| Messaging capacity  | 8x more                | -                      |
| Power consumption   | Improved (more efficient) | -                   |

- Benefits: faster transfers, smoother streaming, better real-time responsiveness

---

## RFID (Radio Frequency Identification)

### Purpose
- Identifies and tracks objects using **encoded tags**
- Reader scans tag -> tag responds with programmed info

### Tag Types
| Tag Type  | Power Source     | Range        |
|-----------|-------------------|--------------|
| Passive   | Unpowered         | Up to ~25 m  |
| Active    | Powered           | Up to 100 m  |

### Common Uses
- Passive tags: stickers/labels for tracking **parcels/equipment**
- Also used in **access badges** for electronic locks

---

## NFC (Near Field Communication)

### Basics
- **Peer-to-peer version of RFID**
- A device can act as **both tag and reader**
- Range: up to **2 inches (6 cm)**
- Data rates: **106, 212, or 424 Kbps**

### Common Uses
- Contactless payment (tap-to-pay)
- Security ID tags
- Shelf-edge labels (retail stock control)
- Can be used to **configure/pair Bluetooth devices**

---

## Quick Comparison Table

| Technology | Range        | Speed              | Use Case                          |
|------------|--------------|---------------------|-------------------------------------|
| Bluetooth  | Up to 800 ft (v5) | Up to 3 Mbps (24 Mbps w/ 802.11 link) | Peripherals, audio, file sharing |
| RFID       | 25 m (passive) / 100 m (active) | N/A (ID data only) | Tracking, access badges           |
| NFC        | ~2 in (6 cm) | 106-424 Kbps        | Payments, pairing, ID tags        |
