
## Duplex Mismatch
- Transfer speed can drop if **duplex settings don't match** between the **NIC** and the **switch port**
- For Gigabit Ethernet, both should be set to **autonegotiate**
- Check:
  - NIC driver settings on the **client OS**
  - Switch port settings via the **switch management software**

---

## Structured Troubleshooting Process
If configuration is fine, slow speeds can have many causes and are hard to diagnose. Work through these steps in order.

### Step 1: Define the Problem
- Ask the user **exactly what they were doing** (web browsing, file transfer, logging in, etc.)
- Confirm there really is a **link speed problem**:
  - Check the **nominal link speed**
  - Use a utility to **measure transfer rate** independent of specific apps/services

### Step 2: Check for Interference (Cabling)
- If the problem is isolated to **one cable segment**, suspect **interference**

| Type | Causes |
|------|--------|
| **External interference** | Nearby **power lines, fluorescent lighting, motors, generators** |
| **Crosstalk** | **Poor cable installation or connector termination** (signals leaking between wire pairs) |

**How to check:**
- Look at cable ends for **excessive untwisting** of wire pairs or **bad termination**
- A **network tap** + analyzer software can report **high numbers of damaged frames**
- Switch management software can show **error rates**
- Fix: may need **shielded cables**

### Step 3: Check the NIC Driver
- Install a **driver update** if available
- If already up to date, check if **other hosts with the same NIC + driver version** have the issue

### Step 4: Check for Malware or Faulty Software
- Host may be **infected** or running **faulty software**
- Consider **removing it from the network** to scan
- Test by **plugging a different host into the same port**
  - If that fixes it, find **what's different** about the original host

### Step 5: Establish the Scope
- Who is affected?
  - **One user** only?
  - **All users on the same switch**?
  - **Everyone accessing the Internet**?
- Could be **congestion** at a switch/router or another **network-wide issue**
- Causes: a **fault**, or **user behavior** (e.g., transferring a very large amount of data)

---

## Quick Reference: Common Causes of Slow Speeds

| Cause | What to Check |
|-------|-----------------|
| **Duplex mismatch** | NIC and switch port both set to **autonegotiate** |
| **Interference** | Power lines, lights, motors, generators nearby |
| **Crosstalk** | Cable termination, untwisted wire pairs |
| **Bad NIC driver** | Update driver; check other hosts with same NIC |
| **Malware/faulty software** | Scan host; swap in a different host on the same port |
| **Network congestion** | Check scope (one user, one switch, whole network) |

---

## Quick Summary
- First check **duplex/auto-negotiate** settings
- Then follow a structured process: **define problem -> check cabling/interference -> check NIC driver -> check malware -> check scope**
- **Crosstalk** = interference from poor cable termination; **external interference** = from power lines, lights, motors, etc.
- **Network tap + analyzer** or **switch error rates** can reveal damaged frames
- Always determine the **scope**: one user vs. whole network
