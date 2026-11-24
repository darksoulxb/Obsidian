

ip
global ip
-modem uses dhcp protocol
-NAT(network accesses transmitter)
-------------------------------
# -port numbers [IP number:Port Number]
HTTP = 80
MongoDB = 2707
SQL = 1433
reserved ports = 0~1023
application = 1024 ~ 49152
remaining can be used

speeds:
1 mbps = 1000000 bits/s
1 gbps = etc

upload = sending data
download = reciving data
===================================
internet traffic

guided way- set path via cable etc
unguided way - changes frequently like wifi and Bluetooth type shi

---------------

physical connections: optical cables, corial cables.

wireless: Bluetooth,wifi,mobile networks etc.
-------------------------
Whole Internet Basically

LAN[Local Area Network]:
small network of internet with ethernet,wifi etc.

MAN[metropolis area network]:
wide area of internet connectivity for bigger bodies such as cities and such.

WAN[wide are network]:
wide area of internet connectivity for counties using optical fiber
cables and such.

wan types:
1.SoNet(Synchronous Optical Network):
2.Frame Relay:
----------------------------
Modem,Router,ISP
 

===================================

Topologies:

1.Bus

2.Ring

3.Star

4.tree (combination of star and bus)

5. Mesh
expensive.
scalability issue.
-----------------------
=================================
*Structure of the network*

*OSI MODEL[open systems internet]:*

7 main layers:

1.Applicaion layer
2.Presentation layer
3.session layer
4.Transport layer
5.Network layer
6.Data Link layer
7.Physical layer


1.Application
implemented in software like software and browser.

2.Presentation
sent from application layer to presentation layer
translates the raw data captured from application layer which is in form of words and numbers and converts it into machine language which can be processed.In binary basically translation,compression encoding and encryption, abstraction.(ssl protocol)

3.Session layer
Its primary role is to establish, manage, synchronize, and terminate connections—or "sessions"—between two communicating applications across a network.
divided to small chunks known as segments

sequence number used to coordinate segments
session establishment

session maintance - checkpoint to check for errors

session termination

4. transport layer
It's part is to transfer data from one


-flow control - control the amount of data to send speeds basically
-data control
-congestion control

*TCP*
*UDP*

5.Network Layer:
It's responsible for transmitting for the received segments from one computer to another that's located in a different network
 -router lives here


*function:*

-logical addressing: Ip packet
-Routing protocol: moving data to destination
-load balancing:


                ---- transmits to datalink layer----
6.DataLink layer:

allows to directly communicate with the computer
- receives data packets from network layer containing Ip  address of both the sender and the receiver

1)logical addressing
2)physical addressing(mac address)

7.Physical Layer:
wires and stuff


===============================================================================

TCP/IP MODEL:

Layers:

Application
Transport
Network
Data Link
Physical

Application Layer:
Users interact
applications and browsers etc.
Where and which devices
protocols
client - server architecture

Server : A system that is responsible for hosting applications

How servers work:

CLIENT------request----->server
      <------response----

server: a system that controls whole
client : service receiver

(2.) peer 2 peer:

decentralized network, a machine can be both host and a client on a network sorta how torrents work
---
got router and stuff
------------
PROTOCOLS:

web protocols:

*TCP/IP:
HTTP:
DHCP:
FTP:
SMTP:
pop3 & iMac:
SSH:
VNC:
UDP:
-- Telnet: port 23

-------------------
Program: WhatsApp
Process:--->sending message/recording video
has multiple jobs

Thread: has single operation as a time

Sockets: A socket is a virtual "plug" that allows two programs to send messages to each other over a network or the internet.

ports: Port number defines which application is using network it sorta works like IP addresses but for on machine thing. (like how Ip operates on a network for communication and identification).

Ephemeral ports:
""
An ephemeral port is a temporary, short-lived port number that your operating system automatically assigns to a client application when it makes an outbound network connection.

If a server's well-known port (like port 443 for a web server) is a public hotline, the ephemeral port is the caller ID or a temporary "burner" phone number your computer uses so the server knows where to send the response.

""
: A temp port number to establish multiple point of connections with a single server simultaneously for sending and receiving different sets of data packets

---
#HTTP:
application layer protocol
 -get requests etc etc
HTTP uses TCP protocol
Stateless protocol

LAYERS IN HTTP:
Application layer: Http
Transport Layer: TCP

|the architecture:
|
|CLIENT------request----->server
|     <------response----
|


HTTP METHODS:

Get
Post method
Put
Delete

STATUS/ERROR CODES:
within 100: info category
200: success
300: redirection
400: client error
500:server error

---------
Cookies:
unique string
stored locally on browser
-- third party cookies:
cookies set for URLs that you didn't/wouldn't visit.

=======================

HOW EMAIL WORKS??
Application layer:

for sending: SMTP{simple mail transport protocol}
  for receiving: POP3

Transport layer:

TCP {lossless cuz you don't wanna loose any info}

sender ---> sender's smtp server(for a while as connection is yet to be established) ----> receiver smtp server ---> Receiver

when on same platform:

sender ----> smtp server ---> Receiver

----------------

pop {post office protocol}:


client ----authorise---> pop server
       <---Transaction---

--------------------

iMap {internet message access protocol}:

allows you to access from multiple devices basically syncs multiple devices together

=============================================
{part of [application layer] btw}
DNS {Domain Name System}:

Well it is used to find IP address of a website's server from a data base of DNS.

when you type www.google.com HTTP protocol is going to take that domain name it's going to use DNS and convert that URL into the IP address and after that it's gonna connect to the server.

Http will take that URL and it will try yo find it'd IP address and once the IP address has been found then it will connect to that server

SO TF DOES DNS DO?????

It's basically a directory/database service.

it has multiple levels and layers of servers to make it even more robust and resistant to any downtime.

parts of a domain:

mail.google.com



mail	Sub-domain
Google	Second-level domain
.com	top level domain

## all these have diff servers

Top Level Domain / Root DNS Servers:
consists of domains like:
.io , .org, .com

2.Second-level domain
"student".io , "commands".org,
--------------
WHAT HAPPENS WHEN YOU TYPE IN GOOGLE.COM

{checks in own computer} ----> [ISP] ----> {Root Server}

![[Pasted image 20261122175715.png]]



===========================================

# TCP/IP LAYER

2. Transport Layer

Transportation of the data from the network to application within the machine  

----------------------------
MULTIPLEXER

Multiplexer (transport layer multiplexer) passes info to de-multiplexer 

======================

data travels in packs and to know about it transport layer will attach these port numbers that's why it knows where the application's data is coming from.
Transport layer protocols:

- also takes care of congestion layer


Congestion layer types:

Transport layer:

Network layer:


-------
congestion control algorithms built in TCP

Checksum:

it's something that's calculated by amounta data you got, it flags of the calculated checksum is diff on the receiver's end with some error or smt.

Timers:

to know that data has been received it uses timer mechanism, the timer starts when the data is transmitted from one device to it's client, when the timer is expired and the expected ping isn't received by the device an action is triggered by the sender mostly error codes and stuff.

- Sequence numbers in timers
 Sequence numbers identify which specific bytes are being tracked by a timer, preventing confusion when packets are lost, delayed, or resent.




---
**Checksum**

* **Purpose:** Error detection (checks if data got corrupted in transit).
* **How it works:** Sender calculates a hash/sum of the packet's bytes and puts it in the header; receiver recalculates and matches it.
* **On failure:** Corrupted packet is silently discarded.
* **Used in:** IPv4, TCP, UDP, ICMP.

**Timers**

* **Purpose:** Loss detection, retransmission, and connection state management.
* **How it works:** Countdown clock started on an event (e.g., sending a packet); triggers an action when it expires.
* **Key TCP timers:**
* **Retransmission (RTO):** Resends packet if no `ACK` arrives.
* **Persistence:** Probes a zero-window receiver to avoid deadlock.
* **Keep-Alive:** Checks if an idle connection is still active.
* **TIME_WAIT (2MSL):** Holds a closed port briefly to catch delayed stray packets.



**How they work together:** Bad **checksum** --> receiver drops packet --> no `ACK` sent --> sender's **retransmission timer** expires --> packet is resent.

---

=================

Protocols

UDP - user datagram Protocol:

data may or may not be delivered 
Data may change
Data may not be in order
Connectionless protocol
uses checksums


UDP Packet:

every data packet has a port numbers such as source port number and destination port number in a packet (2bytes)
length of datagram (2bytes)
checksum (2bytes)
Data ()

Total size = 2^16 

everything except data is considered header since header consists of 8 bytes if data

2^16-8= 65,536 bytes of data in a single packet.

why we use it? 

It's significantly faster
video calling apps
DNS (it also uses udp) ---> UDP
Gaming

=========================================

TCP - Transmission Control Protocol

Transport Layer protocol
Application layer sends lots of raw data
Divides data to chunks to add headers etc
it also collects data from network layer
Congestion control

Takes Care of:

when data doesn't arrive
maintains the order of data using seq number

Features:

connection oriented 
error control
congestion control
Full Duplex (File transfer through two computers simultaneously)


3 - way handshake


A 3-way handshake is the three-step process TCP (Transmission Control Protocol) uses to establish a reliable, synchronized connection between two hosts before transmitting actual data.

![[Pasted image 20261124191019.png]]

          HTTPS REQUEST   
*Client* ---> *sequence number* ---> *Server* 

3:10:02
