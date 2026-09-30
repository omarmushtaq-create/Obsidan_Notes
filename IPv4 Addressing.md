

## The Core Protocol: IP
- **IP (Internet Protocol)** = core protocol in TCP/IP
- Provides:
  - **Network and host addressing**
  - **Packet forwarding** between networks
- An IP packet adds headers to whatever data it's carrying
- Two most important header fields:
  - **Source IP address**
  - **Destination IP address**

---

## IPv4 Address Basics
- IPv4 address = **32 bits long**
- Raw binary form (example):
```

11000000101010000000000000000001

```

### Octets
- 32 bits are split into **4 groups of 8 bits** = **octets**
```

11000000 10101000 00000000 00000001

```

### Dotted Decimal Notation
- Binary is hard for humans -> convert each octet to **decimal**, separate with periods
- Example:
```

192.168.0.1

```

### Value Ranges
| Bit Pattern | Decimal Value |
|-------------|----------------|
| All 1s (11111111) | 255 (max) |
| All 0s (00000000) | 0 (min) |

- Theoretical range: **0.0.0.0** to **255.255.255.255**
- Note: some addresses are **reserved/not permitted** for normal use

---

## Configuring IP with PowerShell (netsh)

### Set a Static IP Address
**Command:** `netsh interface ip set address`

| Parameter | Meaning |
|-----------|---------|
| `name="InterfaceName"` | Which network interface to configure (e.g., "Ethernet") |
| `static` | Use a static IP (not DHCP) |
| `IPAddress` | The static IP to assign |
| `SubnetMask` | Subnet mask for the address |
| `DefaultGateway` | Default gateway (use `0.0.0.0` if none) |

**Example:**
```

netsh interface ip set address name="Ethernet" static 192.168.0.5 255.255.255.0 192.168.0.1

```

---

### Configure DNS Servers

**Set Primary DNS:** `netsh interface ip set dns`
**Add Secondary/Tertiary DNS:** `netsh interface ip add dns`

| Parameter | Meaning |
|-----------|---------|
| `name="InterfaceName"` | Interface to configure |
| `static` | Static DNS assignment |
| `DNSServerAddress` | IP address of the DNS server |
| `primary` | Marks this as the primary DNS server |
| `index=Number` | Order/position of DNS server (e.g., `index=2`) |

**Examples:**
```

netsh interface ip set dns name="InterfaceName" static 10.23.88.32 primary  
netsh interface ip add dns name="InterfaceName" 10.23.40.32 index=2

```

---

## Quick Summary
- IP = handles addressing + forwarding; key header fields = source/destination IP
- IPv4 address = 32 bits = 4 octets, written in **dotted decimal notation** (e.g., 192.168.0.1)
- Range: 0.0.0.0 to 255.255.255.255 (some reserved)
- `netsh interface ip set address` = configure static IP
- `netsh interface ip set dns` / `add dns` = configure DNS servers
- [[https://www.omnicalculator.com/other/ip-subnet]]
- 