---
aliases:
  - TCP/IP
  - TCP/IP Model
  - Layers And Intro
tags:
  - networking/tcpip
creation_date: 2026-11-24
source: scrib2
up: "[[Networking MOC]]"
---

# TCP/IP Model

The practical model the internet actually runs on. Taught here as 5 layers.

| # | Layer | Role | OSI equivalent |
| --- | --- | --- | --- |
| 5 | **Application** | Users interact; apps, browsers, protocols, [[Client-Server and P2P\|architecture]] | [[Application layer\|L7]] + [[Presentation layer\|L6]] + [[Session layer\|L5]] |
| 4 | **Transport** | Process-to-process delivery, ports ([[TCP-IP Transport Layer]]) | [[Transport layer\|L4]] |
| 3 | **Network** | Addressing and routing ([[IP Address]]) | [[Network layer\|L3]] |
| 2 | **Data Link** | Local delivery, MAC | [[Data Link layer\|L2]] |
| 1 | **Physical** | Bits on the medium | [[Physical layer\|L1]] |

> [!note]
> The original RFC TCP/IP model has 4 layers (Application, Transport, Internet, Link). The 5-layer version splits Link into Data Link + Physical to line up with OSI.

## What's in this section
- [[Client-Server and P2P]]: application layer architecture
- [[TCP-IP Transport Layer]]: multiplexing, ports, reliability
- [[Checksum]] · [[Timers]] · [[Congestion Control]]
- [[Processes Threads Sockets]] · [[Ephemeral Ports]]
- Protocols: [[Protocols Overview]]

See also [[OSI]] for the 7-layer comparison.
