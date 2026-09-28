
## The Internet
- A **global network of networks**
- **Backbone** = high-bandwidth **fiber optic links** connecting **Internet Exchange Points (IXPs)**
- Trunk links and IXPs are mostly built by **telecom companies and academic institutions**

---

## IXPs and ISP Relationships
- **IXP** = datacenter where ISPs connect their networks together
- ISPs use two types of arrangements to carry traffic they don't physically own:

| Arrangement | Meaning |
|-------------|---------|
| **Transit** | One ISP pays another to carry its traffic |
| **Peering** | ISPs exchange traffic directly with each other |

- ISPs are arranged in a **tiered hierarchy**
  - Tier = how much an ISP depends on transit deals with other ISPs

---

## Connecting a Customer to the Internet
- Customers connect through an **ISP's network**
- Connection goes to the ISP's nearest **Point of Presence (PoP)**
  - Example: a local telephone exchange
- **Internet connection type** = the media, hardware, and protocols that link a home/small office network to the ISP's PoP

### WAN Interface
- Usually a **point-to-point connection**
  - Only **two devices** on the media (unlike Ethernet)
- Ethernet uses **NICs and switches**
- WAN connection uses a type of **digital modem**

---

## Modem vs Router

| Device | Job |
|--------|-----|
| **Digital modem** | Makes the **physical connection** to the WAN interface |
| **Router** | Identifies each network and **forwards data between them** using **IP (Internet Protocol)** |

> The modem gets you connected physically. The router handles the logical side: which network is which, and where data should go.

---

## Quick Summary
- Internet = network of networks, backbone = fiber links + IXPs
- ISPs share traffic using **transit** and **peering**
- Home/office connects to the ISP's **PoP** over a **point-to-point WAN link**
- **Modem** = physical connection
- **Router (IP)** = logical networks and forwarding

Role of a digital modem to connect a local network to an ISP's network for Internet access![A diagram illustrates the structure and functionality of a small office or home office network setup.](https://cdn.testout.com/a-plus-220-120x-en-us/materials/resources/text/s_internet_connection_types/1145-1638447756897-internet_connection_types_modem-01.png)

Role of the router and Internet Protocol (IP) in distinguishing logical networks![A diagram illustrating a network setup with a local private network and an Internet-connected public network using a router.](https://cdn.testout.com/a-plus-220-120x-en-us/materials/resources/text/s_internet_connection_types/6733-1638446307232-internet_connection_types_router_public_private-01.png)