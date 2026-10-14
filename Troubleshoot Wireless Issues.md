

## Overview
- Like wired links, wireless problems fall into two groups:
  - **Physical media issues** (interference, distance)
  - **Configuration issues**
- **RF signal weakens a lot with distance**

### First Steps
1. If connection is **intermittent, slow, or won't connect** -> **move the devices closer together**
2. Still failing -> check **security/authentication settings** on both devices
   - Most authentication failures = **wrong password** or **wrong security standard**

---

## Wireless Configuration Issues

### SSID Not Found
- Possible causes:
  - User is **out of range**
  - **SSID broadcast is suppressed** (hidden network)
- Fix for hidden SSID: **manually configure** the connection on the client

### Standards Mismatch
- If the AP is **not in compatibility mode**, it can't talk to devices that only support **older standards**
- **Older devices slow down the whole network:**
  - To support **802.11b** clients, a b/g/n AP must send **legacy preamble + collision avoidance frames** -> extra overhead
  - Best fix: **upgrade 802.11b devices** instead of letting them join
  - 802.11g and 802.11n/ac/ax negotiate collision avoidance more compatibly

### Dual-Band Mismatch
- Not all **802.11n** clients have **dual-band** radios
- If a client **can't connect on 5 GHz**, check if its radio is **2.4 GHz only**

---

## RSSI (Received Signal Strength Indicator)

### What It Is
- An **index level** calculated from the **signal strength**
- Adapter lowers speed if RSSI is below a required level

### Example (802.11n adapter)
| Signal | Possible Data Rate |
|--------|----------------------|
| Optimum | 144 Mbps |
| Weak | Drops to 54 Mbps or 11 Mbps (more reliable) |
| Too low | **Drops connection** and tries another network |

- If two weak networks are available, the adapter may **"flap"** between them
- Fix: **move to a location with better reception**

---

## Wireless Signal Issues
If the device is **within range** but signal is weak or intermittent, check these:

| Cause | Details | Fix |
|-------|---------|-----|
| **Interference from another radio source** | Another device on the **same frequency** | **Change the channel** |
| **Powerful electromagnetic source** | **Motors**, **microwave ovens** | Move away or change band/channel |
| **Physical obstruction** | Radio waves struggle through **metal and dense objects** | **Reposition/angle** the device or antenna |

### Materials That Block or Weaken Signals
- **Wire mesh**
- **Foil-backed plasterboard**
- **Concrete**
- **Mirrors**

---

## Wi-Fi Analyzer (inSSIDer Example)
- Software that shows **signal strength of nearby networks per channel**
- Signal in **dBm**, shown as a **negative value**
  - **Closer to zero = stronger signal**
- Shows **how many networks use each channel**
- Use it to pick a **less congested channel** and improve performance
- inSSIDer table columns: SSID, Signal, Radios, Clients, Channels, Security, Mode, Max rate, Last modified
- Graphs shown for **2.4 GHz** and **5 GHz**

---

## Quick Troubleshooting Table

| Symptom | Likely Cause | Fix |
|---------|---------------|-----|
| Can't connect, auth fails | Wrong password or security type | Re-enter password, match security standard |
| SSID not listed | Out of range or hidden SSID | Move closer or configure manually |
| Old device slows everyone | Legacy 802.11b client on the network | Upgrade the old device |
| Can't see 5 GHz network | Client is 2.4 GHz only | Use a dual-band client |
| Speed drops / disconnects | Low RSSI (weak signal) | Move closer / better location |
| Weak or intermittent signal in range | Interference or obstruction | Change channel, move away from motors/microwaves, reposition |

---

## Quick Summary
- First step for most wireless issues: **move closer**
- Check **password and security type**, then **SSID visibility**
- **Legacy (802.11b) devices** and **2.4 GHz-only clients** cause compatibility problems
- **Low RSSI** = adapter reduces speed or drops the connection
- **Interference** (other radios, motors, microwaves) -> **change channel**
- **Obstructions** (metal, concrete, mirrors, foil-backed plasterboard) -> **reposition**
- Use a **Wi-Fi analyzer** to find the least congested channel
