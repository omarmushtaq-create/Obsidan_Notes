
## How a Host Decides: Local or Remote?
When a host wants to send an IPv4 packet, it compares:
- The **source IP address** (its own)
- The **destination IP address** (where it's sending to)
- Using its **subnet mask** to check both

> **Simple idea:** The subnet mask tells the host which part of an IP address is the "network" part. If the network part of the source and destination match, they're on the same local network.

---

## Case 1: Same Network (Match)

- Example: Source and destination both fall under **192.168.0.0/24**
- Host concludes: **destination is local** (same network/subnet)
- Host delivers the packet **directly** on the local network
- On Ethernet, it uses **ARP** to find the **MAC address** matching that destination IP

> Think of it like: "This person lives on my street, I can just walk it over myself."

---

## Case 2: Different Network (No Match)

- Example: Source = **192.168.0.100** (network 192.168.0.0/24)
- Destination = on **192.168.1.0/24** (a different network)
- Host concludes: **destination is remote** -> must be **routed**
- Packet is sent to a **router** instead of being delivered directly

> Think of it like: "This person doesn't live on my street, so I hand the letter to the post office (router) instead."

---

## Default Gateway

- Most hosts have a **default gateway** setting
- **Default gateway** = the IP address of a **router interface** used to forward packets to other networks
- **Important rule:** The default gateway **must be on the same IP network** as the host itself

> Simple explanation: The default gateway is like your host's "exit door" to reach any network it doesn't already know how to reach directly.

---

## Quick Summary
- Host compares source + destination IP against its **subnet mask**
- **Match** = same network -> deliver locally (uses **ARP** to find MAC address)
- **No match** = different network -> send to **default gateway** (a router)
- **Default gateway** = router IP, must be in the **same subnet** as the host
