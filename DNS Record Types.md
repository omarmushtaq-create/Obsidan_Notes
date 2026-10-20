
## DNS Server Roles
- **Resolver DNS servers** (configured on clients) = handle queries for hosts across the Internet
- **Authoritative DNS servers** = hold the actual records for a domain (usually a **separate server** from client resolvers)

---

## Zones and Resource Records
- The server managing a **zone** (a domain) stores **resource records**
- These records let the server **resolve names/services to IP addresses**
- Records can be:
  - **Static** (created/updated manually), or
  - **Dynamic** (auto-generated from client/server info on the network)

---

## A and AAAA Records

| Record Type | Resolves Host Name To |
|-------------|--------------------------|
| **A** (Address) | **IPv4** address |
| **AAAA** | **IPv6** address |

> Simple way to remember: AAAA = "A" but 4x longer, matching IPv6 being 4x the length of IPv4 (32 bit -> 128 bit).

---

## CNAME Records

### What It Does
- **CNAME (Canonical Name)** record = links **one domain name to another domain name**

### Example Use Case
- Company A acquires Company B
- Instead of maintaining two separate websites:
  - `www.companyA.com`
  - `www.companyB.com`
- Company A creates a **CNAME** linking `www.companyB.com` -> `www.companyA.com`

### Benefit
- Users typing the old URL (`www.companyB.com`) get **automatically redirected**
- Useful for people who don't know about the acquisition/URL change

---

## MX (Mail Exchanger) Records

### Purpose
- Identifies the **email server(s)** for a domain
- Lets other mail servers know **where to send messages**

### Key Details
- Networks often have **multiple mail servers** for redundancy
  - Each gets its own **MX record**
- Each MX record has a **preference value**
  - **Lowest number = most preferred**
- **Important rule:** The host name in an MX record **must have a matching A or AAAA record**

### Example Logic
| MX Preference | Mail Server | Priority |
|-----------------|--------------|----------|
| 10 | mail1.contoso.com | Preferred (tried first) |
| 20 | mail2.contoso.com | Backup |

---

## Quick Summary

| Record | Purpose |
|--------|---------|
| **A** | Host name -> IPv4 address |
| **AAAA** | Host name -> IPv6 address |
| **CNAME** | Alias - one domain name points to another domain name |
| **MX** | Identifies mail server(s) for a domain (lower preference number = higher priority); must point to a host with an A/AAAA record |
