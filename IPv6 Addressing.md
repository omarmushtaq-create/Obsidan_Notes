
## Why IPv6?
- IPv4's public address pool is **too small** for the number of Internet-connected devices
- Private addressing + NAT helps, but is a workaround
- **IPv6** = designed to eventually **replace IPv4** completely
- IPv6 address = **128 bits** (vs IPv4's 32 bits) -> massively more possible addresses

---

## IPv6 Notation

### Hexadecimal Format
- Written in **hexadecimal**, not decimal
- 1 hex digit = 4 bits (a "nibble")
- 128-bit address = split into **8 groups of 16 bits**, separated by colons

**Full example:**
```

2001:0db8:0000:0000:0abc:0000:def0:1234

```

### Shortening Rules
1. **Leading zeros** in a group can be dropped
2. **One** continuous run of all-zero groups can be replaced with `::` (double colon) - only once per address

**Shortened example:**
```

2001:db8::abc:0:def0:1234

```

> Note: You can only use `::` **once** in an address, otherwise it would be ambiguous how many zero-groups it replaces.

---

## IPv6 Network Prefixes

### Structure
- Address is split into 2 halves:
  - **First 64 bits** = Network ID
  - **Last 64 bits** = Interface ID (specific device)

### No Subnet Mask Needed
- Since network/host portions are **fixed size (64/64)**, IPv6 doesn't use subnet masks
- Instead uses **prefix notation**: `/nn` = length of the network prefix in bits

### Typical Allocation
- ISPs usually get a **/32** block
- Each **customer** typically gets a **/48** prefix
- A /48 allows up to **65,536 subnets** on that private network

---

## Global vs Link-Local Addresses

- Unlike IPv4 (usually 1 IP per interface), **IPv6 interfaces often have multiple addresses**

| Address Type | Purpose | Starts With |
|--------------|---------|--------------|
| **Global** | Unique on the Internet (like IPv4 public) | `2` or `3` |
| **Link-local** | Communicate with neighbors on local segment only | `fe80::` |

---

## SLAAC (StateLess Address Auto Configuration)
- Most hosts get their **global + link-local** addresses automatically from the **local router**
- This process = **SLAAC**
- **No default gateway needed** to be manually configured in IPv6

### Neighbor Discovery (ND)
- Protocol used to:
  - Implement **SLAAC**
  - Let a host **discover a router**
  - Do the job **ARP** does in IPv4 (finding other hosts' addresses)

---

## Dual Stack
- IPv6 rollout has been slow -> most hosts/routers run **both IPv4 and IPv6 at once**
- This is called **dual stack**
- Typical behavior:
  - Host **tries IPv6 first**
  - **Falls back to IPv4** if the destination doesn't support IPv6

---

## Quick Summary
- IPv6 = 128-bit address, written in **hex**, shortened using **::" and dropped leading zeros**
- First 64 bits = **network**, last 64 bits = **interface ID** (no subnet mask needed, uses `/nn` prefix)
- **Global** address = public/Internet-facing (starts with 2 or 3)
- **Link-local** address = local-segment only (starts with fe80::)
- **SLAAC** = auto-configuration via router; uses **Neighbor Discovery (ND)** instead of ARP/default gateway
- **Dual stack** = running IPv4 + IPv6 together (IPv6 preferred, falls back to IPv4)
