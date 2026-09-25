

## Overview
- Introduced several improvements to increase bandwidth
- Works on **both 2.4 GHz and 5 GHz** bands
- Each band = handled by a **separate radio**
- Officially renamed **Wi-Fi 4**

---

## Dual Band
- Device that supports **simultaneous 2.4 GHz + 5 GHz** = "dual band"
- Some older smartphones only support **2.4 GHz radio**

---

## Channel Bonding
- 802.11n can combine **two adjacent 20 MHz channels** -> one **40 MHz channel**
- Called **channel bonding**
- Practically only usable on **5 GHz** (2.4 GHz has too restricted a channel layout when multiple APs are involved)

### Notes on 5 GHz Bonding
- 5 GHz channels are **not always contiguous**
- Some channels may be **blocked if radar signal detected**
- Bonded channels are identified by their **center channel number**

---

## MIMO (Multiple Input Multiple Output)
- Uses **2-3 separate antennas** to multiplex signal streams
- Increases **reliability + bandwidth**
- Antenna configs written as: **1x1, 2x2, 3x3**
  - Format = (transmit antennas) x (receive antennas)

---

## Data Rates
| Configuration                     | Data Rate        |
|------------------------------------|-------------------|
| Per stream (standard 20 MHz)       | 72 Mbps           |
| Per stream (40 MHz bonded channel) | 150 Mbps          |

### Marketing Naming: "Nxxx"
- xxx = nominal bandwidth number
- Example: **N600** access point
  - 2x2 config, bonded channel -> **300 Mbps** per radio
  - If done simultaneously on **both** 2.4 GHz and 5 GHz radios -> combined **600 Mbps** total

---

## Quick Summary
- 802.11n = **Wi-Fi 4**
- Dual band capable
- Channel bonding (40 MHz) -> mainly on 5 GHz
- MIMO = multiple antennas = more speed/reliability
- Speed marketing (Nxxx) = combined theoretical throughput

#### 802.11n 40 MHz bonded channel options in the 5 GHz band. The center channel number is used to identify each bonded channel
![U-N I I sub bands U-N I I-1, U-N I I-2, U-N I I-2 Extended, and U-N I I-3 from the 20 and 40 Mega hertz channels.](https://cdn.testout.com/a-plus-220-120x-en-us/materials/resources/text/s_wireless_networking_types/3802-1638371248178-wifi_frequency_band_5_ghz_channel_layout_40_mhz_bonding_80211n.png)