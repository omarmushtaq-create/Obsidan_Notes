
## The Problem
- **Client-wired connectivity issue** = either:
  - **No link at all** (no connectivity), or
  - **Unstable/intermittent** connection
- First, confirm the issue affects **only one host**
- Then **isolate the exact location** of the physical problem

---

## Components of a Typical Ethernet Link
Think of the path from the computer to the switch as a chain. A fault in any link can break the connection:

| #   | Component                                                                                              |
| --- | ------------------------------------------------------------------------------------------------------ |
| 1   | **NIC port** on the host                                                                               |
| 2   | **RJ45 patch cord** (host to wall port)                                                                |
| 3   | **Structured cable** (wall port to patch panel) - the **permanent link**, terminated to **IDC blocks** |
| 4   | **RJ45 patch cord** (patch panel to switch port)                                                       |
| 5   | **Network transceiver** in the switch port                                                             |

> **Tip:** **Link LEDs** on the NIC and switch port show if the link is active (and sometimes the speed). They **flicker** to show network activity.

---

## Troubleshooting Steps (In Order)

### Step 1: Check the Patch Cords
- Check they are **properly terminated** and **firmly connected**
- If a fault is suspected, **swap in a known good cable**
- Can verify with a **cable tester**

### Step 2: Test the Transceivers/Ports
- Use a **loopback tool** to test for a **bad port**

### Step 3: Swap Known-Working Hosts (if no loopback tool)
- Connect a **different computer** to the link, or **swap ports** at the switch
- Downsides:
  - May **affect the rest of the network**
  - Features like **port security** can make this unreliable

### Step 4: Test the Structured Cabling
- If patch cords and ports/NICs are ruled out, use a **cable tester** on the **permanent link**
- Possible causes:
  - Bad cable (may need a **new permanent link**)
  - **Termination** problem
  - **External interference**
- **Certifier** = advanced cable tester that reports **detailed performance and interference** info

### Step 5: Check Configuration and Drivers
- Verify **speed/duplex** settings on the **switch interface** and **NIC**
  - Should normally be **auto-negotiate**
- Try **updating the NIC driver**

---

## Quick Reference: Tools

| Tool | Used To |
|------|---------|
| **Cable tester** | Verify patch cords and structured cabling |
| **Loopback tool** | Test if a port/NIC is faulty |
| **Certifier** | Advanced cable testing (performance + interference details) |
| **Known good cable/host** | Substitution testing to isolate the fault |

---

## Port Flapping

### What It Is
- A NIC or switch interface **continually switches between up and down states**
- A form of **intermittent connectivity**

### Common Causes
- **Bad cabling**
- **External interference**
- **Faulty NIC** at the host end

### How to Check
- Use the **switch configuration interface** to see **how long a port stays in the up state**

---

## Quick Summary
- Troubleshoot **from the host outward**: patch cords -> ports/transceivers -> structured cabling -> speed/duplex + drivers
- **Substitute known-good parts** to isolate the fault
- **Loopback tool** = test a port | **Cable tester** = test cable | **Certifier** = detailed cable performance
- Speed/duplex should typically be **auto-negotiate**
- **Port flapping** = port repeatedly goes up/down; usually bad cabling, interference, or a faulty NIC
