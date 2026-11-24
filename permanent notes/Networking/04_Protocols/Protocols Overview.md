---
aliases:
  - Protocols
  - Web Protocols
tags:
  - networking/protocols
creation_date: 2026-11-24
source: scrib2
up: "[[Networking MOC]]"
---

# Protocols Overview

| Protocol | Layer | Port | Transport | Purpose | Note |
| --- | --- | --- | --- | --- | --- |
| **TCP/IP** | suite | — | — | The whole protocol family | [[TCP-IP Model]] |
| **[[HTTP]]** | App | 80 / 443 (HTTPS) | TCP | Web | [[HTTP]] |
| **DHCP** | App | 67/68 | UDP | Auto-assigns IPs | #status/todo |
| **FTP** | App | 20/21 | TCP | File transfer | #status/todo |
| **SMTP** | App | 25 / 587 | TCP | Sending email | [[Email Protocols]] |
| **POP3** | App | 110 | TCP | Receiving email (download) | [[Email Protocols]] |
| **IMAP** | App | 143 | TCP | Receiving email (sync) | [[Email Protocols]] |
| **SSH** | App | 22 | TCP | Encrypted remote shell | #status/todo |
| **VNC** | App | 5900 | TCP | Remote desktop | #status/todo |
| **Telnet** | App | 23 | TCP | Remote shell, **plaintext**, use SSH | #status/todo |
| **[[DNS]]** | App | 53 | UDP (+TCP) | Name → IP | [[DNS]] |
| **[[TCP]]** | Transport | — | — | Reliable delivery | [[TCP]] |
| **[[UDP]]** | Transport | — | — | Fast, best-effort | [[UDP]] |

> [!warning] Fixed from scrib
> "pop3 & iMac" → **POP3 & IMAP**. TCP and UDP are transport protocols, not "web protocols". TCP/IP is the suite, not one protocol.
