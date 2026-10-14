
## "Limited Connectivity" (Windows)

### What It Means
- Host has a **physical connection** to the network
- BUT it **did not get an IP lease from a DHCP server**
- Windows assigns an **APIPA address** in the **169.254.x.y** range
- Other systems:
  - **Linux** might also use APIPA, **or**
  - Set the IP to **0.0.0.0** (unknown), **or**
  - Leave the IP **unconfigured**

### Troubleshooting Steps

#### 1. Establish the Scope
- **Multiple users affected?** -> Likely a problem with the **DHCP server itself**
- Note: DHCP leases take time to expire, so a server problem may take **a few hours** to show up as clients renew
- Possible DHCP server problems:
  - Server is **offline**
  - Server **ran out of available leases**
  - **Forwarding** between server and clients is **misconfigured**

#### 2. Check Patch Cord Configuration
- Verify the **wall port** connects to the **correct switch port** (via the patch panel)
- Wrong switch port = host likely **can't reach** its **default gateway, DHCP, or DNS**

#### 3. Check VLAN Configuration
- If the switch port has the **wrong VLAN ID**, it has the **same effect as being plugged into the wrong port**

---

## "No Internet Access" (Windows)

### What It Means
- Adapter **has an IP configuration** (from DHCP or static)
- BUT it **can't reach the Microsoft test site** to download a test file

### Likely Causes
- **No Internet access** at the **gateway router**, or
- **Name resolution (DNS)** problem

### Troubleshooting Steps (SOHO Network)
1. Open the **router management interface**
2. Check the **status page** to verify the **Internet connection**
3. If the **link is down** -> **contact your ISP**
4. Use the router's built-in **connectivity test tools** if available
5. Verify the router can reach the **configured DNS servers**

---

## Quick Comparison

| Message | Means | Likely Cause |
|---------|-------|----------------|
| **Limited connectivity** | Physical link OK, **no DHCP lease** (APIPA 169.254.x.y) | DHCP server down/out of leases, wrong switch port, wrong VLAN |
| **No Internet access** | Has IP config, **can't reach the Internet** | Router/ISP outage or DNS problem |

---

## Quick Summary
- **Limited connectivity** = no DHCP lease -> **169.254.x.y** (APIPA)
  - Check **scope** (one user vs many), **patch cords**, and **VLAN ID**
  - Many users affected -> suspect the **DHCP server** (offline, out of leases, forwarding issue)
- **No Internet access** = has IP but can't reach the Internet
  - Check the **router's Internet connection status** and **DNS**
  - Link down -> **call the ISP**
