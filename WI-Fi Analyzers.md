

## Wi-Fi Analyzer
- Tool used to measure signal strength and troubleshoot wireless performance
- Helps determine best **channel layout**
- Can be **hardware or software**
  - Software version: installs on laptop/smartphone
  - Records stats for the AP currently connected to
  - Also detects **other nearby APs**

---

## Signal Strength (dBm)

### Basics
- Measured in **decibel milliwatts (dBm)**
- Based on ratio to **1 milliwatt (mW)**
  - **0 dBm = 1 mW**
  - Negative dBm = a fraction of a mW
    - Example: -30 dBm = 0.001 mW
    - Example: -60 dBm = 0.000001 mW
- Wi-Fi devices output **low power** due to regulations

### Reading Signal Strength
> **Closer to 0 = better signal**

| Signal Value        | Meaning                         |
|----------------------|----------------------------------|
| ~ -65 dBm            | Good signal                      |
| Worse than -80 dBm   | Likely packet loss / dropped connection |

---

## Logarithmic Scale (Important Note)
- dB = logarithmic ratio between two values (**nonlinear**)
- Small number changes = big performance changes
  - **+3 dB = doubling** of power
  - **-3 dB = halving** of power

---

## Signal-to-Noise Ratio (SNR)
- = comparison between the **actual signal** and **background noise**
- Noise is also measured in dBm, BUT:
  - **Closer to 0 = worse** (more noise = bad)
- SNR = Signal (dBm) - Noise (dBm), result expressed in dB

### Examples
| Signal   | Noise   | SNR    | Result           |
|----------|---------|--------|-------------------|
| -65 dBm  | -90 dBm | 25 dB  | Good connection   |
| -65 dBm  | -80 dBm | 15 dB  | Much worse connection |

> Higher SNR = better connection quality

---

## Example: Wi-Fi Analyzer Reading (inSSIDer)
- "Home" network uses **2 APs**, same SSID on both bands
- **2.4 GHz band:**
  - Channel 6 (stronger signal) -> closer AP
  - Channel 11 (weaker signal) -> farther AP
- **5 GHz band:**
  - Only channel 36 detected (5 GHz has shorter range than 2.4 GHz)
- Other nearby networks (different owners) = much weaker signals
- Client adapter supports **Wi-Fi 6 (ax)**, but APs only support **b/g/n/ac**
  - Means: client can't use Wi-Fi 6 speeds since AP doesn't support it

---

## Quick Summary
- Use a Wi-Fi analyzer to check signal strength + pick best channels
- dBm closer to 0 = stronger/better signal
- -65 dBm = good, worse than -80 dBm = bad
- dB scale is logarithmic (+3dB = double, -3dB = half)
- SNR = Signal - Noise (bigger SNR = better)
- Even with a fast client (Wi-Fi 6), speed is limited by the AP's supported standard

### Metageek inSSIDer Wi-Fi analyzer software showing nearby access points
![[7575-1638430456803-metageek_inssider_wifi_analyzer_privacy_blurred-01.png]]