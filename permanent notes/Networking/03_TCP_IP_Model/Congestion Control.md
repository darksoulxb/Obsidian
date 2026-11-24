---
aliases:
  - Congestion
  - Flow Control
tags:
  - networking/tcpip
  - networking/transport
creation_date: 2026-11-24
source: scrib2
up: "[[TCP-IP Transport Layer]]"
---

# Congestion Control

Stops senders from overloading the network. Handled at two levels:

| Level | How |
| --- | --- |
| **[[Transport layer]]** | End hosts slow down; [[TCP]] has congestion control algorithms built in |
| **[[Network layer]]** | Routers manage queues, drop or mark packets |

> [!warning] Don't mix these up
> **Flow control** protects the *receiver* (don't send faster than it can read). **Congestion control** protects the *network* (don't send faster than the path can carry).

Scrib mentioned "congestion layer", which should read *congestion control* at the transport and network layers.

## TCP algorithms
Slow start → congestion avoidance → fast retransmit/recovery. Variants: Reno, CUBIC, BBR.

```bash
sysctl net.ipv4.tcp_congestion_control   # Linux: which one you're using
```
