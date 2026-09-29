
## Overview
- Used where wired broadband (DSL/fiber) isn't available
  - Common in **rural areas** or **older buildings**
- Options: **Geostationary satellite**, **LEO satellite**, or **WISP**

---

## Geostationary Orbital Satellite Internet

### Basics
- Uses a **satellite-based microwave radio system**
- Covers **huge geographic areas**
- Typical speeds: **2-6 Mbps up / 30 Mbps down**

### Latency Problem
- Geostationary satellites orbit **very high** -> signal travels **thousands of extra miles**
- Causes **high latency**

| Connection Type | Typical RTT |
|------------------|-------------|
| DSL | 10-20 ms |
| Geostationary Satellite | 600-800 ms |

> **RTT** = Round Trip Time (two-way latency: time for a signal to go out and a response to come back)

- High latency = problem for **real-time apps**: video calls, VoIP, online gaming

### Equipment
- ISP installs a **VSAT** (Very Small Aperture Terminal) dish at customer site
- Dish aligned with the **geostationary satellite** (fixed position above equator)
  - Northern hemisphere -> dish points **south**
- Since satellite doesn't move relative to dish -> **no realignment needed**
- Dish connects via **coax cable** to a **DVB-S modem** (Digital Video Broadcast Satellite)

---

## Low Earth Orbit (LEO) Satellite Internet

### Basics
- Uses an **array/constellation of satellites** in low orbit
- Better performance than geostationary:

| Metric | LEO Satellite |
|--------|----------------|
| Bandwidth | ~5-220 Mbps |
| Latency (RTT) | 25-60 ms |

### Tradeoff
- LEO satellites **move relative to Earth**
- Customer antenna may need to **realign periodically**
  - Some use a **motor** to track satellites
  - Uses **phased array** technology to switch satellites without much mechanical movement
- Antenna needs a **clear view of the whole sky**

### Newer Systems
- Some newer providers use a **flat panel antenna** (no motor needed)
- User just points panel using an **app**
- Goal: **global coverage** from a single provider
- Uses **multiple satellite constellations** for seamless coverage

---

## Wireless Internet Service Providers (WISP)

### Basics
- Uses **ground-based, long-range, fixed wireless** tech
- WISP installs/maintains a **directional antenna** as a bridge between customer and provider
- May use:
  - Wi-Fi-type networking, OR
  - Proprietary equipment
  - Licensed or unlicensed frequency bands

### Pros/Cons
- **Lower latency** than satellite (often)
- **Con:** Maintaining a clear **line of sight** between antennas can be difficult
- If using **unlicensed bands** -> risk of **interference**

---

## Note: Weather Impact
- **All microwave radio links** (satellite + WISP) can be affected by:
  - Snow
  - Rain
  - High winds
  - Solar flares

---

## Quick Comparison Table

| Type | Latency | Speed | Movement Needed | Best For |
|------|---------|-------|-------------------|----------|
| Geostationary Satellite | High (600-800ms) | 2-6 Mbps up / 30 Mbps down | None (fixed) | Wide remote coverage, non-real-time use |
| LEO Satellite | Low (25-60ms) | 5-220 Mbps | Some (motor or phased array) | Modern rural broadband |
| WISP | Low-ish | Varies | Fixed antenna alignment | Rural/fixed wireless bridge |
