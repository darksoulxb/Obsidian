---
aliases:
  - Program
  - Process
  - Thread
  - Socket
  - Sockets
tags:
  - networking/tcpip
  - networking/sockets
creation_date: 2026-11-24
source: scrib2
up: "[[TCP-IP Model]]"
---

# Processes, Threads, Sockets

## Program → Process → Thread
- **Program**: code on disk (WhatsApp, installed).
- **Process**: a running instance of a program, with its own memory.
- **Thread**: one unit of execution inside a process. Does a single operation at a time. A process can have many (sending a message, recording video, syncing).

> [!warning] Correction
> Scrib said the *process* is "sending message/recording video". Those are jobs/threads. The process is the running WhatsApp itself.

## Socket
A **socket** is a virtual "plug" that lets two programs send messages over a network. Technically it's an endpoint: **IP + [[Port Numbers|port]]**.

A [[TCP]] connection is uniquely identified by:
`(protocol, src IP, src port, dst IP, dst port)`

That's why many clients can hit one server on port 443 simultaneously.

## Port
The port number says *which application* on the machine is using the network. Like an IP address, but for apps inside one host. IP identifies the machine on the network, the port identifies the program on the machine.

Linux: `ss -tnp` lists sockets with their owning process.

Related: [[Ephemeral Ports]]
