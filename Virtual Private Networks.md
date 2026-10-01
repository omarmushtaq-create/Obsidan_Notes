## What is a VPN?
- Lets a host connect to a **LAN** without being **physically present** at the site
- Instead of connecting to a switch/AP, host connects to a **remote access server** that accepts connections over the **Internet**
- Since the Internet is **public**, the connection must be made **secure**

---

## How a Secure VPN Works
- Creates a **protected tunnel** through the Internet
- Uses:
  - **Special connection protocols**
  - **Encryption**
- Purpose:
  - Protects against **snooping**
  - Ensures the user is **properly authenticated**

### Once Connected
- The remote computer effectively **becomes part of the local network**
- Still limited by the **bandwidth of the Internet connection** (not as fast as being physically on-site)

---

## VPN Connection Process (3 Steps)

| Step | What Happens |
|------|----------------|
| 1 | **VPN client** connects to a **VPN gateway** using any type of Internet access |
| 2 | **VPN gateway authenticates** the user and builds a **secure encrypted tunnel** |
| 3 | Client traffic is routed over the network -> can access **authorized services** |

---

## Other Uses for VPNs
- The scenario above = **remote access VPN** (teleworkers/roaming users connecting to LAN)
- VPNs can also be used to:
  - **Connect sites** over public networks (e.g., linking a **branch office to head office**)
  - Add **extra security** within a local network itself

---

## Quick Summary
- VPN = secure remote connection to a LAN over the Internet
- Uses an **encrypted tunnel** + **authentication** for security
- Process: **Client connects -> Gateway authenticates + builds tunnel -> Traffic flows to authorized services**
- Also used for: **site-to-site** connections (branch <-> head office) and **internal network security**
