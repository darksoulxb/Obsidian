---
aliases:
  - L4
tags:
  - networking/osi
  - networking/layer4
creation_date: 2026-11-06
source: scrib2
up: "[[OSI]]"
---

# Transport layer (L4)

Moves data **end to end** between applications on two hosts. Uses [[Port Numbers|ports]] to say which application.

**Functions:**
- **Segmentation** of app data into chunks, with sequence numbers
- **Flow control**: how much data the receiver can take (speed matching)
- **Error control**: detect and recover from corrupted/lost data ([[Checksum]], [[Timers]])
- **[[Congestion Control]]**: don't flood the network

**Protocols:** [[TCP]] · [[UDP]]

Deep dive: [[TCP-IP Transport Layer]]

Next layer down: [[Network layer]]
