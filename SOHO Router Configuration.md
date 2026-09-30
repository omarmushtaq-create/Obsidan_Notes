

## Router Interfaces
- Unlike end-system hosts, a **router has multiple interfaces**
- A SOHO router typically has:
  - **Public interface** = connects to the ISP (via digital modem)
  - **Private interface** = Ethernet, connects to the LAN
- **Both** need an IP address + subnet mask

### LAN Interface
- This is the address hosts use as their **default gateway**
- Also used to access the **router's web management page**
  - Example: `https://192.168.0.1` or `https://192.168.1.1`

### Public (WAN) Interface
- IP address is determined by the **ISP**
- Must be from a **valid public range** (e.g., `203.0.113.1`)
- Two ways it's assigned:
  - **Static** (sometimes a paid option)
  - **Dynamic** (via the ISP's own DHCP server) - more common

> Note: `203.0.113.1` isn't actually a real public address - it's a **reserved documentation/example range** (like how examples use "example.com").

### How to Spot a Public IPv4 Address
A public address is one that:
- Is **NOT** in a private range (10.x.x.x, 172.16-31.x.x, 192.168.x.x)
- Does **NOT** start with a zero
- Is **NOT** 224.x.x.x or higher (reserved for multicast/experimental/etc.)

---

## Setting Up a SOHO Router (Step-by-Step)

### 1. Connect to the Router
- Plug into one of the router's **RJ45 ports**, OR
- Join its **default Wi-Fi network** (name found on a sticker on the device)
- Make sure your computer is set to **obtain an IP automatically** (DHCP)
- Wait for the router's DHCP server to assign your computer an IP

### 2. Open the Management Interface
- Use a browser to go to the router's management URL, such as:
[http://192.168.0.1](http://192.168.0.1)  
[http://www.routerlogin.com](http://www.routerlogin.com)
- Might use **HTTPS** instead of HTTP
- **Troubleshooting tip:** if you can't connect, check that your computer's IP is in the **same range** as the router's LAN IP

### 3. Log In
- Enter the **default username/password** (from documentation or a sticker on the router)
- You'll usually be prompted to set a **new admin password**
  - Best practice: use a **strong password, at least 12 characters**

### 4. Configure Internet Connection
- Most routers use a **setup wizard**
- Public IP + DSL/cable settings are usually **self-configuring**
- If manual setup is needed, get the exact settings from your **ISP**

### 5. Check Status / Logs
- Management console can also show:
  - **Line status**
  - **System log**
- Useful for **troubleshooting** with ISP support

---

## Quick Summary
- SOHO router has **2 interfaces**: public (WAN, from ISP) and private (LAN)
- LAN IP = default gateway for hosts + router login address
- Public IP = from ISP, static (paid) or dynamic (ISP's DHCP)
- Public address = NOT private range, doesn't start with 0, not 224+
- Setup steps: **connect -> log in -> change password -> configure Internet -> check status**
