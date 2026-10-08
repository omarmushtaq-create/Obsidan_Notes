aa
## NAT (Network Address Translation)
- On SOHO networks, LAN devices reach the Internet through the **router** using **NAT**
- NAT = translates **private IPs** (LAN) to **public IPs** (Internet)

---

## PAT (Port Address Translation)

### What It Is
- Most SOHO routers use **PAT**
- Also called:
  - **Overloaded NAT**
  - **Port-based NAT**

### How It Works
- Translates **many private IPs** -> **one single public IP** (the router's WAN interface address)
- Many devices can share that one public IP because **each connection gets a unique port number**

> Think of it like an apartment building with one street address: the public IP is the street address, and the port number tells the mail room which apartment (device) each connection belongs to.

---

## Proxy Servers

### What It Is
- Alternative (or addition) to NAT, common in **enterprise networks**
- Does more than just translate addresses:
  1. Takes the **whole HTTP request** from a client
  2. **Checks** it
  3. **Forwards** it to the destination server on the Internet
  4. When the reply comes back, **checks it** again
  5. **Sends it back** to the LAN computer
- Can handle other traffic too (e.g., **email**)

### Transparent vs Non-Transparent

| Type | Client Setup Needed? |
|------|------------------------|
| **Transparent proxy** | No special client configuration |
| **Non-transparent proxy** | Client must be configured with the proxy's **IP address + port** |

- Common proxy port by convention: **8080**

### Example (Firefox)
- Manual proxy config: HTTP Proxy = `192.168.0.1`, port `8080`
- Option to use the same proxy for all protocols (SSL, FTP, SOCKS)
- "No Proxy" list can exclude addresses (e.g., `localhost`, `127.0.0.1`)

### Proxy Functions
| Function | Description |
|----------|--------------|
| **Content filtering** | Blocks access to inappropriate sites |
| **Access rules** | Time limits or **time-of-day restrictions** |
| **Caching** | Stores content to **improve performance** and **reduce bandwidth use** |
| **Request management** | Manages/filters **outgoing** requests |

---

## Quick Comparison

| Feature | NAT/PAT | Proxy Server |
|---------|---------|---------------|
| Translates IP addresses | Yes | Not its main job |
| Inspects request content | No | Yes |
| Content filtering | No | Yes |
| Caching | No | Yes |
| Typical use | SOHO routers | Enterprise networks |

---

## Quick Summary
- **NAT** = private <-> public IP translation
- **PAT** = NAT variant where many devices share **one public IP**, distinguished by **port numbers** (used by most SOHO routers)
- **Proxy server** = checks and forwards requests on a client's behalf
- Proxy can be **transparent** (no client setup) or **non-transparent** (client needs IP + port, often **8080**)
- Proxy benefits: **content filtering, access rules, caching**

