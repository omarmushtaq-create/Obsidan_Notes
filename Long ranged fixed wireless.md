

## Overview
- Wireless can create a **bridge between two networks**
- More cost-effective/practical than laying physical cable
- Requires careful configuration due to **radio spectrum regulation**
- Called: **long-range fixed wireless**

---

## Point-to-Point Line-of-Sight Wireless
- Uses **ground-based, high-gain microwave antennas**
- "High-gain" = **strongly directional** antenna
- Antennas must be **precisely aligned** with each other
- Range: up to **~30 miles** (if unobstructed)
- Mounted on:
  - Tall buildings
  - Tall poles
  - (Reduces risk of physical obstructions)

---

## Licensed vs Unlicensed Spectrum

### Licensed Spectrum
- Operator **purchases exclusive rights** to a frequency band in a specific area
- Regulated in the US by the **FCC** (Federal Communications Commission)
- Benefit: If interference occurs, operator has **legal right to get it shut down**

### Unlicensed Spectrum
- Uses **public frequency bands**: 900 MHz, 2.4 GHz, 5 GHz
- **Anyone can use** these bands -> higher risk of interference
- Power output is **limited by regulation** to reduce conflicts

---

## Components of Wireless Signal Power

| Component            | Description                                             | Measured In      |
|------------------------|-----------------------------------------------------------|-------------------|
| **Transmit power**     | Basic strength of the radio                              | dBm               |
| **Antenna gain**       | Boost from directionality (focusing signal one direction) | dBi (decibels per isotropic) |
| **EIRP**               | Effective Isotropic Radiated Power = Transmit power + Gain | dBm               |

---

## Power Rules
- **Lower frequencies** (travel farther) -> **stricter power limits**
- **Higher frequencies** -> generally more relaxed limits
- **Highly directional antennas** are allowed **higher EIRP**

### Example (2.4 GHz Band Rule)
- Every **+3 dBi gain** can be offset by just **-1 dBm transmit power reduction**
- This tradeoff allows **point-to-point antennas** to reach much **longer ranges** than standard Wi-Fi APs

---

## Quick Summary
- Long-range fixed wireless = wireless bridge between networks over long distances
- Point-to-point = high-gain antennas, precisely aligned, up to 30 miles
- Licensed spectrum = exclusive rights, protected from interference (FCC regulated)
- Unlicensed spectrum = public bands, more interference risk, power-limited
- EIRP = Transmit Power + Antenna Gain
- Directional antennas can achieve long range using low transmit power + high gain
