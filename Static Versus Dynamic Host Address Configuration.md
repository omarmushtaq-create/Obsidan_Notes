
## Downsides of Static Addressing
- Requires **manually visiting each host** to configure
- If host **moves to a different subnet**, must be **manually reconfigured**
- Admin must **track allocated addresses** to avoid duplicates
- In large networks: **time-consuming + error-prone**, can disrupt communication

### When Static IS Used
- Reserved for devices needing a **fixed IP**, like:
  - Router interfaces
  - Application servers

---

## DHCP (Dynamic Host Configuration Protocol)

- Alternative to static config
- A **DHCP server** automatically provides:
  - IP address
  - Subnet mask
  - Default gateway
  - DNS server address(es)

> DHCP = automatic configuration instead of typing everything in by hand.

---

## APIPA (Automatic Private IP Addressing)

### What It Is
- **Failover mechanism** for when a host is set to use DHCP but **can't reach a DHCP server**
- Host picks a **random address** from:
```

169.254.0.1 to 169.254.255.254

```
- Microsoft term: **APIPA**
- Other vendors/open-source: **"link-local"** addressing

### What APIPA Can/Can't Do
| Can Do | Can't Do |
|--------|----------|
| Talk to other hosts on same network **also using APIPA** | Reach other networks |
| - | Communicate with hosts that got a **valid DHCP lease** |

---

## Other Fallback Behaviors
- Not all hosts use link-local addressing
- Some instead:
  - Leave IP **unconfigured**, or
  - Use `0.0.0.0` to show the IP is **unknown**

---

## Quick Summary
- **Static IP** = manual, reliable but hard to manage at scale (used for servers/routers)
- **DHCP** = automatic IP configuration (address, mask, gateway, DNS)
- **APIPA/link-local** = backup address (169.254.x.x) used when DHCP fails
  - Only works for **local-only** communication with other APIPA hosts
- Some systems just show `0.0.0.0` instead of using APIPA
