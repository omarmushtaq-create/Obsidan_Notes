

## Overview
- Wi-Fi (2.4/5/6 GHz) has **limited range**
- Fixed wireless needs a **large dish antenna**
- **Cellular** covers much **larger distances** for mobile devices
- Also used by **IoT devices** (e.g., smart energy meters)
- Cellular standards are grouped into **generations** (3G, 4G, 5G, etc.)

---

## 3G

### Basics
- Device connects to the **closest base station**
- Area served by one base station = a **"cell"**
- Cell range: up to **5 miles (8 km)** (can be blocked by buildings)

### Frequency Bands
| Region | Bands |
|--------|-------|
| Americas | 850 MHz, 1,900 MHz |
| Rest of world | 900 MHz, 1,800 MHz |

> Lower frequencies need **less power** to travel long distances

### Two Competing 3G Formats

| Format | Full Name | SIM Card? |
|--------|-----------|-----------|
| **GSM** | Global System for Mobile Communication | Yes - removable SIM, works with any unlocked handset |
| **CDMA** | Code Division Multiple Access | No - handset directly managed by provider |

### Status Bar Codes
| Code | Meaning | Speed |
|------|---------|-------|
| G, E, 1X | Minimal service | 50-400 Kbps |
| **3G** | UMTS (GSM) or EV-DO (CDMA) | Up to ~3 Mbps |
| **H / H+** | HSPA / HSPA+ (GSM only) | Up to 42 Mbps (nominal; real speeds lower) |

---

## 4G

### LTE (Long-Term Evolution)
- Series of **converged 4G standards**
- Supported by **both GSM and CDMA** providers
- **Requires a SIM card** issued by the network provider

### Frequency Bands
| Region | Bands |
|--------|-------|
| Americas | 600-2500 MHz |
| Elsewhere | 700-2600 MHz |

---

## 5G

### Spectrum Bands
| Band Type | Frequency | Range | Penetration |
|-----------|-----------|-------|---------------|
| Low band (sub-6 GHz) | Lower freq | Longer range | Good penetration |
| Mid/High band (mmWave) | 20-60 GHz | Short range (a few hundred feet) | Cannot penetrate walls/windows |

> **mmWave** = millimeter wave (the high-frequency 5G band)

### Design Challenge
- Because high bands don't travel far or penetrate walls, 5G design is **more complex**
- Solution: use **many small antennas** instead of one big antenna per cell
- Antennas form an array using:
  - **Multipath**
  - **Beamforming**
- This tech = **massive MIMO (mMIMO)**
  - Helps overcome the range/penetration limits of high-frequency 5G bands

---

## Extra Uses (4G/5G)
- Not just for mobile phones - also used for:
  - **Fixed-access wireless broadband** (homes/businesses)
  - **IoT network support**

---

## Quick Comparison Table

| Generation | Key Tech      | SIM Required | Notes                                            |
| ---------- | ------------- | ------------ | ------------------------------------------------ |
| 2G         |               |              | 14.4 Kbps                                        |
| 3G         | GSM or CDMA   | GSM only     | Up to 3 Mbps (or 42 Mbps w/ HSPA+)               |
| 4G         | LTE           | Yes (all)    | Converged standard for GSM + CDMA 300 Mbps       |
| 5G         | mMIMO, mmWave | Yes          | Complex due to short range of high bands 10 Gbps |
