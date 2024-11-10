---
created on: 2024-08-14
last modified on: 2024-08-14
aliases:
  - TCP
  - TCP/IP
  - TCP 3-Way Handshake
  - TCP 3-Way handshake
tags:
  - networking
  - internet
  - cloudcomputing
---

---
# Definition
An internet communication protocol that allows two (or more) devices to form a connection and stream data, and complemented by [[Internet Protocol]], making it more commonly known as TCP/IP. It occurs in the [[TCP-IP Model#Transport|transport layer]]

It includes a set of instructions to organize the data for it to be sent across the network, as well as the [[Port (computer networking)|port]] number of the destination device. It is also *connection-oriented*, which means that the sender and receiver firstly need to establish and verify a connection based on agreed parameters (also known as "Handshake").

# How it works
1. Device sends a SYN (synchronize) signal to server
2. Server sends a SYN/ACK (synchronize/acknowledge) signal back to device
3. Device sends back an ACK signal
4. Connection established

---
# References
- https://www.coursera.org/learn/networks-and-network-security/lecture/7tr4o/the-tcp-ip-model
- https://en.wikipedia.org/wiki/Transmission_Control_Protocol
# See also
[[OSI Model#Transport]]
[[User Datagram Protocol]]

