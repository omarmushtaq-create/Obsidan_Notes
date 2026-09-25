

## SSID (Service Set Identifier)
- = the **network name** clients use to identify a WLAN
- Max length: **32 bytes**
- Best practice for compatibility: use only
  - ASCII letters
  - digits
  - hyphen (-)
  - underscore (_)

---

## Same vs Different SSID Per Band

| Setup                  | Behavior                                                  |
|-------------------------|-------------------------------------------------------------|
| **Same SSID** for both bands | Client device "probes" and auto-picks the band with strongest signal |
| **Different SSID** per band  | User manually chooses which network/band to connect to     |

---

## Operation Mode
- Set **per frequency band**
- Determines:
  - Compatibility with **older wireless standards**
  - Support for **legacy client devices**
- Tradeoff: Supporting older devices can **reduce performance for all connected stations**

---

## Channel Configuration
For each frequency band, configure:
1. **Channel number**
2. **Channel bonding** (on/off)

### Key Rules
- Multiple APs with **overlapping range** -> use **nonoverlapping channels** to avoid interference
- AP can **auto-configure** best channel, but **doesn't always work well**
- **Channel bonding** = wider channel = more bandwidth
  - Risk: **increased interference** if other wireless networks are nearby
  - Bonding is typically only practical in **5 GHz band** (depends on site design)

---

## Note
- Besides band/channel settings, you must also configure **security settings** to control who can connect to the network

---

## Quick Summary
- SSID = network name (max 32 bytes, keep it simple: letters/digits/-/_)
- Same SSID = auto band selection; different SSID = manual selection
- Operation mode = legacy compatibility (tradeoff: performance)
- Channel setup = number + bonding; avoid overlap; bonding best on 5 GHz
- Don't forget: security config is also required


### Configuring an access point
![A screenshot of the T P-Link Archer V R 900 router's web-based interface displays the Wireless Settings page under the Advanced tab.](https://cdn.testout.com/a-plus-220-120x-en-us/materials/resources/text/s_wireless_networking_types/9986-1637605645920-ap_configuration.png)