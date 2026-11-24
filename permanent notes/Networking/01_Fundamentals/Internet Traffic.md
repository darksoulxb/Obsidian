---
aliases:
  - Traffic
  - Traffic Speeds
tags:
  - networking/fundamentals
  - networking/traffic
creation_date: 2026-11-06
source: scrib2
up: "[[Networking MOC]]"
---

# Internet Traffic

## Speed
Traffic speed = how much data moves per second. Default unit is **bits per second**.

| Unit | Bits per second |
| --- | --- |
| 1 Kbps | 10³ |
| 1 Mbps | 10⁶ (1,000,000) |
| 1 Gbps | 10⁹ |

> [!warning] Bits vs bytes
> ISPs sell **Mbps** (megabits). File sizes are in **MB** (megabytes). 8 bits = 1 byte, so a 100 Mbps line moves ~12.5 MB/s at best.

- **Upload** = sending data (client → server)
- **Download** = receiving data (server → client)

## Mediums
| Type | Meaning | Examples |
| --- | --- | --- |
| **Guided** | Fixed physical path | Optical fiber, coaxial, twisted pair |
| **Unguided** | Travels through air, path changes constantly | Wi-Fi, Bluetooth, mobile networks |

Physical connections = optical / coaxial cables. Wireless = Bluetooth, Wi-Fi, mobile.

The signal-level side of this lives in the [[Physical layer]].

## Related
- [[Network Types]] · [[Network Topologies]] · [[Network Devices]]
