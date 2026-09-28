

## Overview
- Usually offered as part of a **cable access TV (CATV)** service
- Network type = **Hybrid Fiber Coax (HFC)**
  - **Fiber optic** core network
  - **Copper coaxial cable** links to the customer's premises
- Also called **broadband cable** or just **cable**

---

## DOCSIS
- **DOCSIS** = Data Over Cable Service Interface Specification
- The standard used by cable Internet

| Version | Downlink | Uplink |
|---------|----------|--------|
| Standard DOCSIS | Up to 42.88 Mbps (North America) or 55.62 Mbps (Europe) | Up to 30.72 Mbps |
| **DOCSIS 4** | Up to **10 Gbps** | Up to **6 Gbps** |

- DOCSIS 4 reaches higher speeds by using **multiplexed channels**

---

## Cable Modem Installation
- Works on the **same general principles as a DSL modem**

### Connections
| Connection | Cable / Port | Goes To |
|------------|--------------|---------|
| Modem to local router | **RJ45** port | Your router |
| Modem to provider network | Short **coax** segment with **F-type connectors** (threaded) | ISP network |

> F-type connectors are threaded (screw on), the same type used for TV coax.

---

## How the Data Travels
1. Customer's **cable modem**
2. **Coax cable** linking all premises in the street
3. **CMTS** (Cable Modem Termination System)
4. **Fiber backbone**
5. ISP's **Point of Presence (PoP)**
6. **Internet**

> **CMTS** = equipment that forwards data traffic from the coax network onto the fiber backbone.

---

## Quick Summary
- Cable Internet = **CATV** = **HFC** (fiber core + coax to customer)
- Standard = **DOCSIS**
- DOCSIS 4 = up to **10 Gbps down / 6 Gbps up**
- Cable modem to router = **RJ45**; modem to provider = **coax with F-type connector**
- Street coax goes to the **CMTS**, which sends data over fiber to the ISP PoP

## DSL vs Cable (Quick Compare)
| Feature | DSL | Cable |
|---------|-----|-------|
| Medium | Copper phone line | Coax (HFC network) |
| Modem to router | RJ45 | RJ45 |
| Modem to provider | RJ11 | F-type (coax) |
| Network name | PSTN | CATV / HFC |


A cable modem: The RJ45 port connects to the local network router, while the coax port connects to the service provider network
![A modem with a cable port, a reset button, an Ethernet port, and a Power port.](https://cdn.testout.com/a-plus-220-120x-en-us/materials/resources/text/s_internet_connection_types/9885-1637606298912-760aad50-59bd-48a7-a313-2601c49cfd0c2376-1624343906232-n10-008_cable_modem.png)