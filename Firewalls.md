

## Purpose
- After connecting LAN + WAN with a router, you need to **control**:
  - Which computers can connect
  - Which types of traffic are allowed
- This job is done by a **network firewall**

---

## Access Control List (ACL)
- A **basic firewall** is configured using rules called an **ACL**
- Each ACL entry specifies:
  - **Source** address/network
  - **Destination** address/network
  - **Protocol type**
  - **Allow or block** decision

> Think of an ACL as a list of "if traffic matches this, allow/block it" rules.

---

## Where Firewalls Are Used

### Between Public and Private Networks
- Most common use: filtering traffic between the **Internet (public)** and **local network (private)**

### Inside a Private Network
- Firewalls can also be used **internally**
- Example: only allow certain clients to reach a specific group of servers
  - Place those servers **behind a local firewall** with its own ACL

---

## Types of Firewall Implementation

| Type | Description |
|------|-------------|
| **Router-based firewall** | Most routers include basic firewall features |
| **Standalone firewall appliance** | Dedicated device for firewall duties |

### Standalone Appliances
- Can do **deeper inspection** of application protocol data
- Use **more sophisticated rules**
- Often built as **UTM (Unified Threat Management)** appliances
  - UTM = combines firewall + other security functions in one device

---

## Quick Summary
- **Firewall** = filters allowed/denied hosts and traffic types
- **ACL** = the rule list a firewall uses (source, destination, protocol, allow/block)
- Firewalls can sit **between networks** (LAN/WAN) or **inside** a network (protecting specific servers)
- Can be built into a **router** or run as a **standalone appliance/UTM**


#### Sample ruleset configured on the OPNsense open-source firewall implementation
![A firewall rule management interface for Wide Area Network connections.](https://cdn.testout.com/a-plus-220-120x-en-us/materials/resources/text/s_internet_connection_types/7516-1638543094513-n10-008_opnsense_firewall_rules_acl_expanded.png)