

## Physical Links vs Logical Addressing (Recap)
- Devices discussed so far = **physical links** using **hardware (MAC) addressing** only
- **Ethernet switches / Wi-Fi APs** = forward **frames** using **MAC addresses**
  - A **network segment** = hosts that can reach each other using just MAC addresses
- **Modems, ONTs, cellular radios** = connect local network to ISP over DSL/cable/fiber/satellite/cellular
  - Typically **point-to-point** -> no need for unique interface addressing
  - These segments use different media and **can't talk to each other directly**

---

## Why We Need IP + Routers
- To connect a **private LAN** to the **public WAN (Internet)**, you need:
  1. A protocol that can **distinguish** between LAN and WAN -> **Internet Protocol (IP)**
  2. A device with interfaces in **both** networks -> a **router**

---

## Switch vs Router

| Device | Forwards Using | Address Identifies |
|--------|------------------|----------------------|
| **Switch** | MAC (hardware) address | Just the hardware port |
| **Router** | IP address | The network AND the specific host within it |

> Key difference: A **MAC address** only IDs a hardware interface. An **IP address** identifies both **which network** and **which host** on that network.

---

## Types of Routers

### SOHO Router
- Simple setup
- Routes between:
  - Local network interface
  - WAN/Internet interface

### Enterprise Routers (Different Models, Different Jobs)

#### LAN Router
- Splits **one physical network** into **multiple logical subnetworks**
- Each subnetwork = its own **broadcast domain**
- Benefits:
  - **Performance**: too many hosts in one broadcast domain = slower
  - **Security**: traffic between logical networks can be **filtered**
- Interfaces: typically **all Ethernet**

#### WAN / Border Router
- Forwards traffic **to/from the Internet** or over a **private WAN link**
- Interfaces:
  - **Ethernet** (for local network)
  - **Digital modem interface** (for WAN)

---

## Quick Summary
- MAC address = hardware-only identity (switches use this)
- IP address = network + host identity (routers use this)
- **Router** = the device that connects LAN <-> WAN using IP
- **LAN router** = splits network into subnets/broadcast domains (performance + security)
- **WAN/border router** = connects local network to the Internet/WAN link![A router with power light with multiple L E D indicator lights.](https://cdn.testout.com/a-plus-220-120x-en-us/materials/resources/text/s_internet_connection_types/7410-1637606364809-router-modem.png)