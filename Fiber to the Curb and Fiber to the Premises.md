
## The Problem: Last Mile Bandwidth
- Biggest obstacle to LAN-like Internet speeds = **the last mile**
- Copper wiring there is often **low-grade**
- Projects to replace it with fiber = **Fiber to the X (FTTx)** (umbrella term)

---

## Fiber to the Curb (FTTC)
- Fiber runs from the **PoP** to a **communications cabinet** that serves many subscribers
- From the cabinet to the customer, **copper wiring is kept**
- Telephone-based providers use **VDSL** to support it

### VDSL (Very High-speed DSL)
- **Higher bit rates** than other DSL types
- Tradeoff: **shorter range**
- Supports **symmetric and asymmetric** modes

| Mode / Range | Downstream | Upstream |
|--------------|------------|----------|
| Asymmetric, over 300 m (1,000 ft) | 52 Mbps | 16 Mbps |
| Symmetric, over 300 m (1,000 ft) | 26 Mbps | 26 Mbps |
| **VDSL2-Vplus**, very short range 250 m (820 ft) | 300 Mbps | 100 Mbps |

> **Note:** DSL modems are **not interchangeable**.
> - ADSL modem: unlikely to support VDSL
> - VDSL modem: usually supports ADSL

---

## Fiber to the Premises (FTTP)
- Provider's **fiber runs all the way to the customer's building**
- Full fiber connection
- Built as a **Passive Optical Network (PON)**

### How a PON Works
1. **OLT** (Optical Line Terminal) at the provider
2. **Single fiber cable** runs to a **splitter**
3. Splitter sends each subscriber's traffic down a **shorter fiber**
4. **ONT** (Optical Network Terminal) at the customer's premises

### ONT (Optical Network Terminal)
- **Converts the optical signal to an electrical signal**
- Connects to the customer's router by:
  - **RJ45 copper patch cord**, or
  - Can have the **router built into the same device**

| ONT Port | Connects To |
|----------|-------------|
| **PON port** | External fiber cable |
| **LAN ports** | Local routers/computers via RJ45 patch cords |

---

## Quick Comparison

| Type | Fiber Goes To | Last Section | Notes |
|------|---------------|--------------|-------|
| **FTTC** | Street cabinet | Copper (VDSL) | Faster than ADSL, but short range |
| **FTTP** | Customer's building | Fiber | Full fiber, uses PON + ONT |

---

## Quick Summary
- **FTTx** = projects that bring fiber closer to the customer
- **FTTC** = fiber to a cabinet, copper the rest of the way, uses **VDSL**
- **VDSL** = faster than other DSL but **shorter range**
- ADSL modems usually **cannot** do VDSL; VDSL modems usually can do ADSL
- **FTTP** = fiber all the way to the building using a **PON**
- PON chain: **OLT -> splitter -> ONT**
- **ONT** converts light to electrical, connects to router via **RJ45**
