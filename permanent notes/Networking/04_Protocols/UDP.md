---
aliases:
  - User Datagram Protocol
tags:
  - networking/protocols
  - networking/transport
creation_date: 2026-11-24
source: scrib2
up: "[[Protocols Overview]]"
---

# UDP

**User Datagram Protocol.** Transport-layer, connectionless, no guarantees.

- Data may or may not be delivered
- May arrive **out of order**
- Connectionless (no handshake)
- Uses a [[Checksum]] to detect corruption

## Packet format
Header is **8 bytes** (4 fields × 2 bytes):

| Field | Size |
| --- | --- |
| Source port | 2 B |
| Destination port | 2 B |
| Length (header + data) | 2 B |
| Checksum | 2 B |
| Data | variable |

The length field is 16 bits, so the max datagram is `2¹⁶ − 1 = 65,535` bytes. Max data is **65,527** (65,507 over IPv4 after the 20-byte IP header).

> [!warning] Correction
> Scrib calculated `2^16 − 8 = 65,536`. The subtraction was wrong, and the real max is 65,527 bytes of data.

## Why use it
- Significantly **faster**, less overhead
- Video calls, gaming, live streaming
- [[DNS]]
- Modern HTTP/3 builds on it (QUIC)

Compare: [[TCP]]
