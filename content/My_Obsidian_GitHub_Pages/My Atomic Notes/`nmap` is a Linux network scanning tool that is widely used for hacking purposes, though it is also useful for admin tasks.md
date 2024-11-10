---
created on: 2024-11-07
last modified on: 2024-11-07
aliases:
  - using nmap
tags:
  - codesnippet
  - kalilinux
  - hacking
  - tools
  - linux
---

---
[^1]
> [!tip]
> `nmap` in general should be run as a `poweruser` because then it doesn't need to have to wait for the RST signal that comes from a closed port made during the [[Transmission Control Protocol|TCP 3-Way Handshake]]

# Main `nmap` scanning techniques:
```sh
 -sS/sT/sA/sW/sM: TCP SYN/Connect()/ACK/Window/Maimon scans
 -sU: UDP Scan
 -sN/sF/sX: TCP Null, FIN, and Xmas scans
 --scanflags <flags>: Customize TCP scan flags
 -sI <zombie host[:probeport]>: Idle scan
 -sY/sZ: SCTP INIT/COOKIE-ECHO scans
 -sO: IP protocol scan
 -b <FTP relay host>: FTP bounce scan
```
# Listing all targets to scan  (Scan and List)
```sh
sudo nmap -sL 10.0.1.0/24
```
# Listing and pinging the target (Scan and Ping)
```sh
# This sends an [[Internet Control Message Protocol|ICMP]] packet to the target, effectively pinging it.
sudo nmap -sP 10.0.1.147
```
# Scan all open ports of a given address
```sh
sudo nmap -p- 10.0.1.147
```
# Scanning port of a given address
```sh
# Scan port 2323 for IP address 10.0.1.147
sudo nmap -p2323 10.0.1.147
```
# Scanning network with versions of the open ports
```sh
sudo nmap -sV 10.0.1.147
```
# "Loudest" and "Quietest" network scan by `nmap`
```sh
# The Loudest network scan. This will make the [[Intrusion Detection System|IDS]] of the targetted system notice that you had tried to scan the ports of the address
sudo nmap -A 10.0.1.147

# The quietest network scan. This will only check if the port is open, as it leaves without sending back an ACK signal, after receiving the SYN/ACK signal from the target (signalling that it's open)
sudo nmap -sS 10.0.1.147
```
# Scanning a network for to find a (web) server
```sh
# The following will make an attempt to connect to each of the 256 address under 10.7.1.0-255, and will try out the port 80 (http) and 443 (https)
sudo nmap -sT -p 80,443 10.7.1.0/24
```

# Using Scripts when running `nmap`[^2]

> [!note] Scripts for `nmap`
> There are a total of 13 scripts for `nmap` currently listed on [NSE Categories](https://nmap.org/nsedoc/categories/). Each category has their own specific script, for example the `broadcast` category, has `broadcast-hid-discoveryd`, `broadcast-listener`. Otherwise, you just put in one of the 13 categories, and it will run all the scripts under its category for you

```sh
sudo nmap --script <script-name-here/category-name-here> 10.7.1.3
```

---

# See also
[[`grep` is a popular command line utility in bash that is used to find plain text in a line inside files, or output from a command.|using grep]]
# References
[^1]: [nmap: A Practical guide](https://www.youtube.com/watch?v=fMdei5VbJMc)
[^2]: [Nmap Tutorial to find Network Vulnerabilities](https://www.youtube.com/watch?v=4t4kBkMsDbQ)