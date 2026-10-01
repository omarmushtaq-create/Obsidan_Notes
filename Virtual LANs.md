## Broadcast Domains
- All hosts on the **same unmanaged switch** = same **broadcast domain**
- Fine for small networks
- Problem on **enterprise networks**:
  - Switches can have **thousands of ports**
  - Too many hosts in one broadcast domain = **reduced performance**

---

## What is a VLAN?
- **VLAN (Virtual Local Area Network)** = feature of **managed switches**
- Divides switch ports into **logical groups**
- Benefits:
  - **Increases performance** (smaller broadcast domains)
  - **Increases security** (in some cases)

---

## Assigning Ports to a VLAN

### Basic Method
- Configure each **switch port** with a **VLAN ID**
- Valid VLAN ID range: **2 to 4094**

### Example
| Switch Ports | VLAN ID |
|---------------|----------|
| Ports 5-8 | VLAN 100 |
| Ports 9-12 | VLAN 200 |

- Host A on port 5 -> in **VLAN 100**
- Host B on port 12 -> in **VLAN 200**

> **Note:** VLAN ID **1** = the **"default VLAN"**. All switch ports default to VLAN 1 unless configured otherwise.

---

## How VLANs Affect Communication

### Within Same VLAN
- Hosts can communicate **directly** (like normal)

### Between Different VLANs
- Hosts **CANNOT** communicate directly - **even if on the same physical switch**
- Each VLAN needs its **own**:
  - Subnet address
  - IP address range
  - DHCP service
  - DNS service
- To communicate **between VLANs**, traffic **must pass through an IP router**

---

## Why Use VLANs?

### 1. Performance
- Smaller broadcast domains = **less broadcast traffic per group** = better performance

### 2. Security
- Each VLAN = a **separate security zone**
- Traffic **between VLANs** can be:
  - **Filtered**
  - **Monitored**
  - Checked against **security policies**

### 3. Traffic Type Separation
- VLANs can separate devices by **traffic type**
- Example: isolate **voice traffic** devices into their own VLAN
  - Allows **prioritizing voice traffic** over regular data traffic

---

## Quick Summary
- **VLAN** = logically splits one physical switch into multiple separate networks
- Configured via **VLAN ID** (2-4094) on switch ports; **VLAN 1** = default
- Devices in **different VLANs** need a **router** to talk to each other
- Each VLAN needs its **own subnet, DHCP, and DNS**
- Benefits: **better performance**, **better security**, and **traffic prioritization** (e.g., voice vs data)

