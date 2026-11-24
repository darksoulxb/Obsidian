---
aliases:
  - Port
  - Ports
  - Well-Known Ports
tags:
  - networking/fundamentals
  - networking/ports
creation_date: 2026-11-04
source: scrib2
up: "[[Networking MOC]]"
---

# Port Numbers

A **port number** is a 16-bit identifier (`0`–`65535`) that directs traffic to the correct application, process, or service on a device.

> [!info] The Apartment Analogy
> The [[IP Address|IP address]] is the street address of a big apartment building (gets data to the right computer). The **port** is the apartment number (gets it to the exact program).

Without ports, your computer couldn't tell whether incoming data is for a browser, an SSH terminal, a game server, or a torrent client.

## The three ranges
- **Well-known (`0`–`1023`)**: reserved for core system services. On Linux, binding needs root.
  - `22` SSH · `80` HTTP · `443` HTTPS
- **Registered (`1024`–`49151`)**: assigned to specific software. Usable without elevated permissions.
  - `3306` MySQL · `8080` alt web/Docker · `25565` Minecraft
- **Dynamic / ephemeral (`49152`–`65535`)**: temporary ports your OS assigns to outbound connections. See [[Ephemeral Ports]].

> [!warning] Corrections
> Scrib had the registered range ending at `49152` (it's `49151`) and MongoDB as `2707` (default is **`27017`**).

## Common ports
| Port | Service | Transport |
| --- | --- | --- |
| 20/21 | FTP | TCP |
| 22 | SSH | TCP |
| 23 | Telnet | TCP |
| 25 / 587 | SMTP | TCP |
| 53 | DNS | UDP (TCP for large) |
| 67/68 | DHCP | UDP |
| 80 | HTTP | TCP |
| 110 | POP3 | TCP |
| 143 | IMAP | TCP |
| 443 | HTTPS | TCP |
| 1433 | MS SQL Server | TCP |
| 3306 | MySQL | TCP |
| 5900 | VNC | TCP |
| 27017 | MongoDB | TCP |

More in [[Protocols Overview]].

## Socket formatting
Combine IP and port with a colon (a **socket** / endpoint):
- IPv4: `IP:Port` → `192.168.1.50:8080`
- IPv6: `[IPv6]:Port` → `[2001:db8:85a3::8a2e:370:7334]:443` (brackets avoid clashing with IPv6 colons)

## Linux check
```bash
ss -tulpn      # what's listening, and which process owns it
```

Related: [[Processes Threads Sockets]] · [[NAT]] · [[TCP-IP Transport Layer]]
