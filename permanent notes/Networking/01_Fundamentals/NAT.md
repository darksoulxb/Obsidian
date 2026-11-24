---
aliases:
  - Network Address Translation
  - PAT
tags:
  - networking/fundamentals
  - networking/addressing
creation_date: 2026-11-04
source: scrib2
up: "[[Networking MOC]]"
---

# NAT

**NAT = Network Address Translation.** The router translates many private [[IP Address|IP addresses]] into **one public IP**, so every device on the LAN shares a single internet connection.

> [!warning] Correction
> Scrib expanded it as "network accesses transmitter". It is **Network Address Translation**.

## How it keeps connections apart
The router keeps a translation table that uses **[[Port Numbers|port numbers]]** to tell devices apart (this variant is called PAT / NAPT):

| Inside (private) | Outside (public) |
| --- | --- |
| `192.168.1.50:51000` | `49.x.x.x:40001` |
| `192.168.1.51:51000` | `49.x.x.x:40002` |

Replies come back to the public IP + port, and the router maps them to the right device.

## Why it exists
- IPv4 has only ~4.3 billion addresses, so NAT stretches them.
- Side effect: outsiders can't open connections into your LAN unless you set up port forwarding.

Related: [[Network Devices]] · [[Ephemeral Ports]]
