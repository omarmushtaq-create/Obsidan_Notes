

## Overview
- Internet-connected networks need protection against **malicious threats**
- Security services can run as:
  - **Software** on PC servers, or
  - **Purpose-built appliances** (more common in enterprise networks)

---

## Security Functions

### Firewall
- **Allows or blocks traffic** based on an **ACL**
- ACL rules use: **source/destination IP addresses** and **application ports**

### IDS and IPS

| Type | What It Does |
|------|----------------|
| **IDS** (Intrusion Detection System) | Uses scripts to **identify known malicious traffic patterns**; **raises an alert** on a match |
| **IPS** (Intrusion Prevention System) | Same as IDS, but can also **take action to block** the source of the malicious packets |

> **Simple way to remember:** IDS = **detects and alerts** | IPS = **detects and blocks**

### Antivirus / Anti-Malware
- **Scans files** being transferred over the network
- Looks for matches to known **malware signatures** in binary data

### Spam Gateway
- Uses **SPF, DKIM, and DMARC** to verify mail servers are authentic
- Has **filters** to catch spoofed, misleading, malicious, or unwanted messages
- Installed as a **network server** that filters mail **before it reaches the user's inbox**

### Content Filter
- Blocks **outgoing access** to unauthorized websites and services

### DLP (Data Leak/Loss Prevention)
- **Scans outgoing traffic** for **confidential or personal information**
- Checks if the transfer is **authorized**
- **Blocks** it if it isn't

---

## UTM (Unified Threat Management)

### The Problem
- These functions could be deployed as **separate appliances/servers**
  - Each with its own configuration + logging/reporting system
  - More complex to manage

### The Solution: UTM
- **UTM appliance** = combines **multiple security functions** into **one device**
- Enforces a variety of security policies/controls
- Benefits:
  - **Centralized** threat management
  - **Simpler configuration**
  - **Simpler reporting**
  - Compared to isolated apps spread across several devices

---

## Quick Summary Table

| Function                   | Job                                                  |
| -------------------------- | ---------------------------------------------------- |
| **Firewall**               | Allow/block traffic using ACL (IPs + ports)          |
| **IDS**                    | Detect known malicious traffic, **alert**            |
| **IPS**                    | Detect known malicious traffic, **alert + block**    |
| **Antivirus/Anti-malware** | Scan network files for malware signatures            |
| **Spam gateway**           | Filter spoofed/unwanted email (uses SPF/DKIM/DMARC)  |
| **Content filter**         | Block outgoing access to unauthorized sites/services |
| **DLP**                    | Block outgoing confidential/personal data            |
| **UTM**                    | **All of the above combined** in one appliance       |
