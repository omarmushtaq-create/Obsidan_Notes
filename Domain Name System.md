
# DNS, Domain Names, and FQDNs

## Host Names
- IP uses **binary addresses** to locate hosts
- Dotted decimal/hex forms are still hard for humans to remember
- Solution: assign a **"friendly" host name**
  - Set when the OS is installed
  - Must be **unique on the local network**

---

## FQDN (Fully Qualified Domain Name)

### Purpose
- To avoid **duplicate host names on the Internet**, combine:
  - **Host name** + **Domain name** + **Suffix (TLD)**
- This full combination = **FQDN**

### Example Breakdown
```

nut.widget.example

```

| Part | Value |
|------|-------|
| Host name | `nut` |
| Domain name | `widget` |
| TLD (top-level domain) | `.example` |

> A domain suffix can also include **subdomains** (extra parts between host and domain name)

---

## DNS (Domain Name System)
- **FQDNs** are assigned/managed using **DNS**
- DNS = a **global hierarchy** of distributed name server databases
  - Stores info about domains and the hosts within them

---

## DNS Hierarchy

### Root
- **Top of the hierarchy**
- Represented by a **null label** = just a period `.`
- There are **13 root-level servers** (labeled A through M)

### Top-Level Domains (TLDs)
Sit directly below the root. Three main types:

| TLD Type | Examples |
|----------|----------|
| **Generic** | .com, .org, .net, .info, .biz |
| **Sponsored** | .gov, .edu |
| **Country code** | .uk, .ca, .de |

### Who Manages DNS?
- **ICANN** (icann.org) operates DNS overall and manages **generic TLDs**
- **Country code TLDs** = managed by an organization appointed by that country's government

---

## FQDN Structure (Hierarchy Order)
- Read **left to right**: most specific -> least specific
- Format: **Host -> Subdomain(s) -> Domain -> TLD -> Root**

### Example
```

pc.corp.515support.com.

```

| Part                  | Meaning                   |
| --------------------- | ------------------------- |
| `pc`                  | Host name (most specific) |
| `corp`                | Subdomain                 |
| `515support`          | Domain name               |
| `com`                 | TLD                       |
| `.` (trailing period) | Root (least specific)     |

> **Note:** The trailing period at the end of a URL can be left off - it's just assumed to be there (represents the root zone).

---

## Quick Summary
- Host name = friendly name for a device (unique on local network)
- **FQDN** = host name + domain + TLD (unique globally)
- **DNS** = distributed system that manages/resolves FQDNs
- Hierarchy: **Root (.) -> TLD -> Domain -> Subdomain -> Host**
- TLD types: **generic** (.com), **sponsored** (.gov/.edu), **country code** (.uk/.ca)
- **ICANN** manages DNS + generic TLDs; country TLDs managed by local government-appointed orgs

DNS hierarchy
![[aplus_fig06_04_02-2.png]]