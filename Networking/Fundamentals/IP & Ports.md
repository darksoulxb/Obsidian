---
tags:
  - "#NAT"
  - IP
  - Port
creation_date: 2026-11-04
---

---
# [[IP]]
- IP stands for internet protocol.
- IP is sort of like a identification number for devices accessing the network.
- It consists of **character/digit count in text:** Between 7 and 12 digits
- **Total length (bits):** 32 bits

- **Number of decimal sections (octets):** 4 sets of numbers

- **Range per section:** 0 to 255

[More info on IP Address](https://www.geeksforgeeks.org/computer-science-fundamentals/what-is-an-ip-address/)

## [[Global IP]]

- Global IP refers to the entirety of network as in [[LAN]] etc.
- It's referred as *192.168.1.0* 
- This is where the Router sits.

# [[NAT]]

- **NAT (Network Address Translation)** is a process used by routers to translate multiple private, local IP addresses into a single public IP address, allowing all devices on a local network to share one connection to the internet.
- That's how [[IP]] is assigned from Tier 1 provider to ISP to 


# [[Port Numbers]]

A **port number** is a 16-bit numerical identifier (ranging from `0` to `65535`) that directs network traffic to the correct specific application, process, or service running on a device. 

> [!info] The Apartment Analogy
> If an [[IP Address]] is like the street address of a large apartment building (delivering the data to the right computer), the **port number** is the specific apartment number (delivering the data to the exact program that requested it).

Without port numbers, your computer would not know whether incoming network data is meant for a web browser, an SSH terminal, a multiplayer game server, or a torrent client. 

## The Three Port Ranges

*   **Well-Known Ports (`0`–`1023`):** Reserved for core system services and universally standardized protocols. On Linux, you typically need root privileges to bind an application to these ports.
    *   `22`: [[SSH]] (Secure Shell)
    *   `80`: HTTP (Unencrypted web traffic)
    *   `443`: HTTPS (Secure web traffic)

*   **Registered Ports (`1024`–`49151`):** Assigned to specific software applications, games, and vendor services. They can usually be used by standard user applications without elevated permissions.
    *   `3306`: MySQL databases
    *   `8080`: Common alternative for web servers or [[Docker]] containers
    *   `25565`: Default Minecraft server port
*   **Dynamic / Ephemeral Ports (`49152`–`65535`):** Temporary ports automatically assigned by your operating system when you make an outbound connection.

## Socket Formatting 

The standard format for combining an IP address and a port number (technically called a **socket** or **endpoint**) is to separate them with a colon (`:`).

*   **IPv4 Syntax:** `IP_Address:Port`
    *   *Example:* `192.168.1.50:8080`
*   **IPv6 Syntax:** `[IPv6_Address]:Port` (Brackets prevent confusion with the IPv6 colons)
    *   *Example:* `[2001:db8:85a3::8a2e:370:7334]:443`





---
ip
global ip
-modem uses dhcp protocol
-NAT(network accesses transmitter)
------------------------------- 
port numbers 
IP number:Port Number
HTTP = 80
MongoDB = 2707
SQL = 1433 
reserved ports = 0~1023
application = 1024 ~ 49152
remaining can be used