

## PSTN (Public Switched Telephone Network)
- National and global **telephone network**
- Many Internet connection types use it
- **Core** = fiber optic
- **Edge** = often still old **two-pair copper cabling**
- This low-grade copper section has several names:
  - **POTS** (Plain Old Telephone System)
  - **Local loop**
  - **Last mile**

---

## DSL Basics
- **DSL** = Digital Subscriber Line
- Uses the **higher frequencies** on copper phone lines as a data channel
- Uses **advanced modulation** and **echo canceling**
- Result: **high-bandwidth, full-duplex** transmission

---

## Types of DSL

### Asymmetrical DSL (ADSL)
- **Fast downlink, slow uplink**
- Latest version = **ADSL2+**

| Direction | Speed |
|-----------|-------|
| Downlink | Up to ~24 Mbps |
| Uplink | 1.4 Mbps or 3.3 Mbps |

### Symmetric DSL
- **Same speed** for uplink and downlink
- Better for **businesses and branch office links**
  - These send more data **upstream** than normal home Internet use

| Type | Downlink vs Uplink | Best For |
|------|--------------------|----------|
| ADSL | Fast down, slow up | Home users |
| Symmetric DSL | Equal | Businesses, branch offices |

---

## DSL Hardware

### DSL Modem
- Connects the customer network to the phone cabling
- Can be:
  - A **separate device**, or
  - **Built into a SOHO router** (Small Office, Home Office)

### Ports on a Standalone DSL Modem
| Port | Connects To |
|------|-------------|
| **RJ11** (WAN port) | Phone point (wall socket) |
| **RJ45** (LAN port) | Router |

> RJ11 = phone-style connector (smaller). RJ45 = Ethernet-style connector (larger).

---

## Filter / Splitter
- **Required** on each phone socket
- Job: **separates voice and data signals**
- Customer can **self-install** on each phone point
- Modern sockets often have a **built-in splitter**

---

## Quick Summary
- PSTN core = fiber, edge (last mile) = old copper
- DSL uses **high frequencies** on copper phone lines
- **ADSL** = fast down, slow up (ADSL2+ ~24 Mbps down)
- **Symmetric DSL** = equal speeds, used by businesses
- DSL modem: **RJ11** to phone point, **RJ45** to router
- Install a **filter/splitter** on each phone socket to split voice and data

RJ11 DSL (left) and RJ45 LAN (right) ports on a DSL modem![A modem with a D S L port, reset button, an Ethernet port, and a Power port.](https://cdn.testout.com/a-plus-220-120x-en-us/materials/resources/text/s_internet_connection_types/9165-1637606238178-d6a05786-c1c2-4879-a8d2-b2ce98cce0307393-1624343840692-n10-008_dsl_modem.png)

A self-installed DSL splitter![An A D S L splitter with a port for modem on the left and 2 ports for phone on the right.](https://cdn.testout.com/a-plus-220-120x-en-us/materials/resources/text/s_internet_connection_types/717-1637606264706-dsl_splitter.png)