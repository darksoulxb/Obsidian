---
aliases:
  - Checksums
tags:
  - networking/tcpip
  - networking/transport
creation_date: 2026-11-24
source: scrib2
up: "[[TCP-IP Transport Layer]]"
---

# Checksum

- **Purpose:** error detection (was the data corrupted in transit?).
- **How:** sender calculates a sum over the packet's bytes and puts it in the header. Receiver recalculates and compares. Different = flagged as an error.
- **On failure:** the corrupted packet is silently discarded.
- **Used in:** IPv4 (header only), [[TCP]], [[UDP]], ICMP.

> [!note]
> It's a simple 16-bit sum, not a cryptographic hash. It catches accidental corruption, not tampering.

## Works with timers
Bad checksum → receiver drops packet → no `ACK` sent → sender's retransmission [[Timers|timer]] expires → packet is resent.
