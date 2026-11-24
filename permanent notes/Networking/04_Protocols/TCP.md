---
aliases:
  - Transmission Control Protocol
tags:
  - networking/protocols
  - networking/transport
creation_date: 2026-11-24
source: scrib2
up: "[[Protocols Overview]]"
---

# TCP

**Transmission Control Protocol.** Transport-layer protocol for **reliable, ordered** delivery.

- The application layer hands over lots of raw data. TCP **divides it into chunks** and adds headers.
- Also collects data coming up from the [[Network layer]].

## Features
- **Connection-oriented** ([[TCP 3-Way Handshake]])
- **Error control**: [[Checksum]] + [[Timers]] + retransmission
- **Ordering** via sequence numbers
- **Flow + [[Congestion Control]]**
- **Full duplex**: both sides send and receive at the same time (file transfer both ways)

## Takes care of
- Data that doesn't arrive (retransmit)
- Keeping order using sequence numbers

## TCP vs UDP
| | TCP | [[UDP]] |
| --- | --- | --- |
| Connection | Yes | No |
| Reliable | Yes | No |
| Ordered | Yes | No |
| Speed | Slower | Faster |
| Used by | HTTP, SSH, email | DNS, gaming, calls |
