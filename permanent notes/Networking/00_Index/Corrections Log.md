---
tags:
  - networking/meta
creation_date: 2026-11-24
up: "[[Networking MOC]]"
---

# Corrections Log

Factual fixes made while merging `Scrib_2` into the vault. Original text is preserved in `_Archive/original-notes/`.

| Was | Now | Where |
| --- | --- | --- |
| NAT = "network accesses transmitter" | Network **Address** Translation | [[NAT]] |
| OSI = "open systems internet" | Open Systems **Interconnection** | [[OSI]] |
| Global IP = `192.168.1.0` | `192.168.x.x` is private; global IP comes from the ISP | [[IP Address]] |
| Registered ports `1024–49152` | `1024–49151` | [[Port Numbers]] |
| MongoDB `2707` | `27017` | [[Port Numbers]] |
| IP is "7–12 digits" | 4–12 digits, 7–15 characters with dots | [[IP Address]] |
| "cordial cables", "wide are network", "counties" | coaxial, wide area, countries | [[Internet Traffic]], [[Network Types]] |
| Segments / sequence numbers under Session layer | Belong to the Transport layer | [[Session layer]] |
| "Logical addressing" under Data Link | Network layer (IP); L2 is MAC only | [[Data Link layer]] |
| OSI.md "Layer 1 (Application)" | Layer 7 | [[OSI]] |
| "pop3 & iMac" | POP3 & IMAP | [[Protocols Overview]] |
| UDP data = `2^16 − 8 = 65,536` | max 65,527 bytes of data | [[UDP]] |
| "Congestion layer" | Congestion *control* at the transport and network layers | [[Congestion Control]] |
| Process = "sending message/recording video" | Those are threads; the process is the running app | [[Processes Threads Sockets]] |
| "TLD / Root servers" as one thing | Root → TLD → Authoritative | [[DNS]] |
