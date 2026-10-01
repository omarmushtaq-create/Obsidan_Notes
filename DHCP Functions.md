
## Why Use DHCP?
- Manual static config = risk of mistakes:
  - Duplicate IPs
  - Wrong subnet mask
  - Needs manual re-entry if network changes
- **DHCP server** solves this by automatically assigning IP config to hosts

---

## DHCP Scope
- **Scope** = the range of IP addresses a DHCP server can hand out on a subnet
- Must **exclude** any addresses already set statically (like the router's own LAN IP)

### Example
- Router LAN IP (also runs DHCP): `192.168.0.1` -> excluded from scope
- Scope defined as: `192.168.0.100` to `192.168.0.199`
  - = 100 addresses available for dynamic assignment

---

## DHCP Leases

### Setup
- Client is set to **"obtain an IP automatically"**
- Uses **UDP**:
  - Server listens on **port 67**
  - Client listens on **port 68**

### The DORA Process
DHCP uses a 4-step process called **DORA**:

| Step | Packet | Description |
|------|--------|--------------|
| 1 | **D**iscover | Client **broadcasts** DHCPDISCOVER to find a server |
| 2 | **O**ffer | Server responds with DHCPOFFER (IP + config info) |
| 3 | **R**equest | Client broadcasts DHCPREQUEST to accept the offer |
| 4 | **A**cknowledge | Server confirms with DHCPACK |

> **Note:** Client uses broadcast, so it doesn't need to know the DHCP server's address in advance. BUT the **DHCP server itself must have a static IP**.

### After DHCPACK
- Client sends an **ARP** message to double-check the address **isn't already in use**
  - If free: client starts using it
  - If in use: client **declines** and requests a different address

### Lease Expiration
- IP address is **leased for a limited time**
- Client can **renew/rebind** before it expires
- If renewal fails: client must **release** the address and **start discovery again**

---

## DHCP Reservations

### Why Use Them?
- Some devices (servers, routers, printers) benefit from having a **consistent IP**
- Option 1: Static addressing -> harder to manage at scale
- Option 2: **DHCP Reservation** -> easier, still automatic

### How Reservations Work
- DHCP server keeps a list of **MAC addresses** -> each tied to a specific IP
- When a device with a **listed MAC address** connects:
  - Server always issues the **same reserved IP**

> **Note:** Some OSes send a different unique identifier instead of the MAC address by default - make sure the client's identification method matches what the server expects.

---

## Quick Summary
- **DHCP Scope** = range of IPs available to hand out (excludes static addresses)
- **DORA** = Discover -> Offer -> Request -> Acknowledge (the DHCP handshake)
- DHCP uses **UDP** (server: port 67, client: port 68)
- Client double-checks with **ARP** before using an assigned address
- **Leases expire** - client must renew or restart DORA
- **DHCP Reservation** = ties a specific IP to a device's MAC address (consistent IP without static config)


