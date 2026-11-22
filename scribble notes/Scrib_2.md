

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