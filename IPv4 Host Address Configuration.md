
## Minimum Requirements
- To communicate on an IPv4 network, a host needs **at minimum**:
  - **IP address**
  - **Subnet mask**
- But this minimum config = limited usability
- For full network/Internet use, more parameters are needed

---

## Static Configuration

### IPv4 Address
- Entered as **4 decimal numbers separated by periods**
- Example: `192.168.0.100`

### Subnet Mask
- Entered in **dotted decimal notation**
- Example: `255.255.255.0`
- Can also be entered as **prefix/mask length** (e.g., `/24`) instead of dotted decimal

**Example breakdown:**
- IP: `192.168.0.100`
- Mask: `255.255.255.0`
- Result: Network ID = `192.168.0` | Host ID = `.100`

> Some systems (like Windows 10) let you enter a **prefix length** instead of typing the full dotted decimal mask.

---

## Reserved Addresses (Cannot Assign to a Host)

| Address | Purpose |
|---------|---------|
| **First address** in network (e.g., `192.168.0.0`) | Identifies the network itself |
| **Last address** in network (e.g., `192.168.0.255`) | Broadcast address (sends to all hosts) |

> **Valid host range** for `192.168.0.0/24` = `192.168.0.1` to `192.168.0.254`

---

## Additional Parameters for Full Functionality

### Default Gateway
- IP address of a **router** (e.g., `192.168.0.1`)
- Used to send packets to **remote networks**
- **Not required**, but without it:
  - Host can only talk to devices on its **local network**

### DNS Server Address(es)
- **DNS (Domain Name System)** = resolves domain/host names to IP addresses
- Needed for:
  - Browsing the Internet
  - Local network name resolution
- Typically:
  - **Primary DNS** = often same as the **default gateway** address
  - Router then forwards DNS queries to a secure external resolver
- Usually **two DNS addresses** configured:
  - **Preferred** (primary)
  - **Alternate** (secondary) - for **redundancy** (backup if primary fails)

---

## Quick Summary
- Minimum config = **IP address + subnet mask**
- Full config also needs = **default gateway** + **DNS server(s)**
- Can't use the **network address** (first) or **broadcast address** (last) as a host IP
- Default gateway = router IP, lets host reach other networks
- DNS = translates names to IPs; usually 2 servers configured (primary + backup)

