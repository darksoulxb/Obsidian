---
tags: [networking, index, moc]
date: 2026-11-04
---
# Computer Networking

This is the main dashboard for networking studies. 

## 01. Fundamentals
*   [[Network Topologies]] - Star, Mesh, Ring, etc.
*   [[IP_Addressing_and_Subnetting]] - IPv4, IPv6, and CIDR math
*   [[MAC_Addresses]] - Hardware addressing

## 02. The OSI Model
*   [[L1_Physical_Layer]] - Cables, hubs, bits
*   [[L2_Data_Link_Layer]] - Frames, MAC, switches
*   [[L3_Network_Layer]] - Packets, IP, routers
*   [[L4_Transport_Layer]] - Segments, TCP/UDP
*   [[L7_Application_Layer]] - HTTP, DNS, DHCP

## 03. Core Protocols
*   [[TCP_vs_UDP]] - Reliability vs. Speed
*   [[DNS_Resolution]] - How URLs become IPs
*   [[DHCP_Process]] - DORA process for getting an IP
*   [[HTTP_and_HTTPS]] - Web traffic and SSL/TLS

## 04. Practical Labs
*   [[Virtual_Private_Networks]] - Tunneling and routing
*   [[Container_Networking]] - Bridge vs Host networking
*   [[Wake_on_LAN]] - Remote boot setup
*   [[File_Sharing_Protocols]] - SMB sharing ports
  
  ---
* Networking/
├── 00_Networking_Master_Index.md (Your entry point)
├── 01_Fundamentals/
│   ├── Network_Topologies.md
│   ├── IP_Addressing_and_Subnetting.md
│   └── MAC_Addresses.md
├── 02_OSI_Model/
│   ├── L1_Physical_Layer.md
│   ├── L2_Data_Link_Layer.md
│   ├── L3_Network_Layer.md
│   ├── L4_Transport_Layer.md
│   └── L7_Application_Layer.md
├── 03_Protocols/
│   ├── TCP_vs_UDP.md
│   ├── DNS_Resolution.md
│   ├── DHCP_Process.md
│   └── HTTP_and_HTTPS.md
└── 04_Practical_Labs/
    ├── Tailscale_VPN_Routing.md
    ├── Docker_Container_Networks.md
    ├── Wake_on_LAN_Magic_Packets.md
    └── Samba_Port_Configuration.md
    
---


Networking/
├── 01-Fundamentals/
│   ├── IP & Ports.md
│   ├── Connections & Traffic.md
│   └── Network Hardware.md
├── 02-Network-Scales/
│   └── LAN-MAN-WAN.md
├── 03-Topologies/
│   └── Network Topologies.md
└── 04-OSI-Model/
    └── OSI Model.md

---------------
- [ ] First, understand the [OSI](https://www.reddit.com/search/?q=OSI+model+networking&cId=2e23a439-d14e-42fc-932a-89ecf01a2cb8&iId=2e799d4b-3e7a-42a1-b752-a442956ad042). Memorize that bad boy, write lines if you have to. Test yourself later by pairing protocols with the OSI model (";Probably Didn't Need Those Stupid Packets, Anyway" is my favorite acronym)
    
- [ ] Understand how it can be used for troubleshooting (start at the bottom and work your way up. Is the cable plugged in is always a good first step)
    
- [ ] Learn how IPv4 addresses work (Public IPs, Private IPs, subnets, routing tables, NAT)
    
- [ ] Learn how MAC addresses work (ARP tables, switches, DHCP)
    
- [ ] Learn about routers
    
- [ ] Learn about switches
    
- [ ] Learn the difference between routers and switches (L2 vs L3 OSI)
    
- [ ] Learn about TCP and UDP (TCP = ALL the data will be received correctly, in order. UDP = All data will be sent, but it may not arrive, or it may arrive mangled, and that's OK)
    
- [ ] Learn a little about VLANs (TBH I need to brush up on these)
    
- [ ] Learn about DHCP (Static IPs vs Dynamic, IP reservations)
    
- [ ] Learn about DNS (A records, CNAME records, MX records, NS records, SRV records)
    
- [ ] Learn about IPv6 (Unfortunately, not extremely useful right now. Most companies are IPv4 only)
    
- [ ] Learn about VPNs (WireGuard is an excellent one to get started with, and will probably be the standard going forward. IPSec / OpenVPN if you want a challenge)
    
- [ ] Learn a bit how the "greater" internet works (BGP, carriers, IP blocks, IANA). You probably won't need to worry about these technologies / groups, but they're useful background knowledge
    
-  Do some practical work
    
- Examples:
    
- [ ] Set up a WireGuard VPN server. Connect some clients to it. Ping the server from a client. Ping another client from a client
    
- [ ] Set up a DHCP server. Get a device to connect to it (You can use your home router for this. At least mess with the settings a bit)
    
- [ ] Buy a domain name. Point an A record to your home's public IP, or to a cloud server you control with a public IP. Configure SSH on the server, and do the necessary networking to SSH to your server using the domain name. For example, you may need to port forward on your router if your using your home public IP
    
- [ ] Configure mail for your custom domain. Send yourself some email. I recommend Zoho for a free email provider with your own domain.
    
- [ ] Secure your email using DMARC / SPF.
    
- [ ] Make a ";hello world" website. Secure it (HTTPS) using LetsEncrypt.
    
- [ ] Set up a Pi-Hole DNS server for your home network (use a VM if you don't have a pi). Understand, generally, how it works.