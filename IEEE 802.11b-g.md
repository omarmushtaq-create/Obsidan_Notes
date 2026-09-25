
# 802.11b
- Uses **2.4 GHz** band
- Released **alongside 802.11a**
- Uses inferior encoding compared to 802.11a
- Nominal data rate: **11 Mbps**

### Channels (802.11b)
- 2.4 GHz band split into up to **14 channels**
- Spaced **5 MHz apart** (2,412 MHz -> 2,484 MHz)
- Each channel is **22 MHz wide** -> channels overlap a lot since spacing (5 MHz) < width (22 MHz)
- To avoid interference, use only the **3 non-overlapping channels: 1, 6, 11**

### Regional Channel Rules
| Region    | Channels Allowed |
|-----------|-------------------|
| Americas  | 1-11              |
| Europe    | 1-13              |
| Japan     | 1-14 (all)        |

---

# 802.11g
- Simple **upgrade path** from 802.11b
- Same **encoding + speed as 802.11a** (54 Mbps)
- BUT operates in **2.4 GHz** band (like 802.11b)
- Backward compatible with 802.11b clients (easy for vendors to support both)

### Channel Width Difference
| Standard | Modulation | Channel Width |
|----------|------------|----------------|
| 802.11b  | DSSS       | 22 MHz         |
| 802.11g  | OFDM       | 20 MHz         |

> **Modulation** = technique to modify a radio wave so it can carry data

### Modulation Types
- **DSSS (Direct-Sequence Spread Spectrum)** - used by 802.11b
  - Spreads signal across wider channel (22 MHz)
  - Improves resistance to interference
- **OFDM (Orthogonal Frequency-Division Multiplexing)** - used by 802.11g
  - More efficient
  - Sends more data over a smaller channel (20 MHz)

> Note: Even though 802.11g's channel is technically narrower, it stays on the **same 2.4 GHz channel layout** as 802.11b to maintain compatibility.

---

## Quick Comparison Table

| Feature        | 802.11b    | 802.11g    |
|----------------|------------|------------|
| Band           | 2.4 GHz    | 2.4 GHz    |
| Max Speed      | 11 Mbps    | 54 Mbps    |
| Modulation     | DSSS       | OFDM       |
| Channel Width  | 22 MHz     | 20 MHz     |
| Backward Compat| N/A        | Yes (with b)|

![A table and a graph illustrating 2.4 gigahertz Wi-Fi frequencies and channel overlaps.](https://cdn.testout.com/a-plus-220-120x-en-us/materials/resources/text/s_wireless_networking_types/1940-1637605271390-50a97b9a-172a-4898-aaef-cf64de0099575920-1624290638467-channel_overlap_in_the_2point4_ghz_band.png)