# Lab 1: Network Traffic Analysis with Wireshark
Context: Completed as part of Year 1 University Assignment  
Tool Used: Wireshark  
Time to Complete: 45 minutes

---

## What I Did
- Captured live network traffic using Wireshark on an authorised university network.
- Applied display filters to isolate DNS, HTTP, and HTTPS/TLS traffic.
- Examined packet headers and payloads to compare encrypted vs unencrypted traffic.
- Used "Follow TCP/HTTP Stream" to view plaintext data transmitted over unencrypted connections.
- All work conducted within university lab guidelines — passive monitoring only, no traffic modified.

---

## Key Concepts Demonstrated

### 🌐 IP Addressing
![IP Addressing](IP.png)
Every packet shows Source IP and Destination IP addresses — unique identifiers for devices on a network.

### 🌐 DNS (Domain Name System)
![DNS](DNS.png)
DNS translates human-readable domain names into IP addresses. Queries and responses visible in the capture.

### 📊 Network Protocols
![Protocols](Protocols.png)
Multiple protocol types visible: TCP, HTTP, TLSv1.2, DNS. Each protocol serves a different purpose in network communication.

### 🚪 Ports & Services
![Ports](Ports.png)
Port numbers identify which service is being used — Port 80 = HTTP, Port 443 = HTTPS/TLS.

### 📡 TCP (Transmission Control Protocol)
![TCP](TCP.png)
TCP provides reliable, ordered delivery using sequence numbers and acknowledgements (ACK). Foundation of most internet traffic.

### 🔒 HTTPS / TLS Encryption
![HTTPS](HTTPS.png)
Encrypted traffic using TLS — payload appears as unreadable hexadecimal data. Protects data from interception.

---

## Additional Concepts — Understanding

###  SYN Flood
A denial-of-service attack exploiting the TCP three-way handshake. Attacker sends many SYN requests but never completes the handshake with an ACK. Server resources become exhausted and unresponsive to legitimate users.

###  ARP Spoofing
Attacker sends fake ARP announcements to link their MAC address to a legitimate IP address on the local network. Redirects traffic through the attacker — creating a Man-in-the-Middle attack.

---

## What I Learned
- How to capture, filter, and interpret network packets.
- The difference between unencrypted HTTP (plaintext readable) and encrypted HTTPS/TLS (data protected).
- How IP addresses, ports, and protocols work together to deliver data across networks.
- Common network attacks and how they appear in packet captures.
