---
aliases:
  - L2
  - MAC Address
tags:
  - networking/osi
  - networking/layer2
creation_date: 2026-11-06
source: scrib2
up: "[[OSI]]"
---

# Data Link layer (L2)

Delivers data between devices **directly connected on the same local network**.

- Receives packets from the [[Network layer]] (which carry sender and receiver IP addresses)
- Wraps them into **frames** and adds **physical addressing**: the **MAC address** of the next hop

> [!warning] Correction
> Scrib listed "1) logical addressing 2) physical addressing" here. Logical addressing (IP) is the [[Network layer]]. L2 only handles **physical (MAC)** addressing.

Switches operate here. Hands frames down to the [[Physical layer]].
