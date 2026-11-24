---
aliases:
  - TCP Timers
  - Sequence Numbers
tags:
  - networking/tcpip
  - networking/transport
creation_date: 2026-11-24
source: scrib2
up: "[[TCP-IP Transport Layer]]"
---

# Timers

- **Purpose:** loss detection, retransmission, and connection state management.
- **How:** a countdown starts on an event (e.g. sending a packet). If the expected `ACK` doesn't arrive before it expires, the sender acts, usually by retransmitting.

## Key TCP timers
| Timer | What it does |
| --- | --- |
| **Retransmission (RTO)** | Resends a packet if no `ACK` arrives |
| **Persistence** | Probes a zero-window receiver to avoid deadlock |
| **Keep-Alive** | Checks if an idle connection is still alive |
| **TIME_WAIT (2MSL)** | Holds a closed port briefly to catch delayed stray packets |

## Sequence numbers
They identify **which specific bytes** a timer is tracking, preventing confusion when packets are lost, delayed, or resent. See [[TCP 3-Way Handshake]].

Pairs with [[Checksum]].
