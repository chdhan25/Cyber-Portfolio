# Packets & Frames

**Date Completed:** July 2 2025

## Key Concepts Learned

- The difference between **packets** and **frames**
- **Encapsulation and decapsulation** in network communication
- The structure of **TCP** and **UDP** headers
- The **TCP Three-Way Handshake** and **connection teardown**
- How **UDP** works as a connectionless protocol
- The role of **ports** in identifying services

## Tools/Commands Introduced

- No direct commands — conceptual and visual room
- Used interactive diagrams and packet analysis simulations

## Notes

### 🧩 What Are Packets and Frames?

- **Packet:** Data unit at the **Network layer** (contains IP info)
- **Frame:** Data unit at the **Data Link layer** (no IP info, contains MAC addresses)
- **Encapsulation:** Data gets wrapped in headers as it travels down OSI layers
- **Decapsulation:** Headers are removed as data moves up the receiving device’s OSI layers
- Example: A file is split into packets (e.g., cat image) and reassembled on the receiving end

### 🔁 TCP/IP – The Three-Way Handshake

- **TCP** is connection-oriented and reliable
- Steps:
  1. `SYN` – Client initiates connection
  2. `SYN/ACK` – Server responds
  3. `ACK` – Client confirms, connection is established
- **TCP Closing a Connection:** Uses `FIN`, `ACK`, and optionally `RST` if something goes wrong
- **TCP Header Fields:**
  - Source/Destination Port
  - Source/Destination IP
  - Sequence & Acknowledgement Numbers
  - Checksum (used to ensure data integrity)
  - Flags (like SYN, ACK, FIN)

### 🌐 UDP/IP

- **UDP** is connectionless, faster, but doesn’t guarantee delivery
- Used in apps like video calls, gaming, or DNS
- No handshakes or acknowledgements
- Shared headers with TCP: TTL, IP addresses, source/destination ports
- **Less overhead**, **no data recovery** if packets are lost

### 🔢 Ports 101

- **Ports identify services** on a device
- Common examples:
  - `80`: HTTP
  - `443`: HTTPS
  - `53`: DNS
  - `22`: SSH
- **Port Ranges:**
  - `0–1023`: Well-known ports
  - `1024–49151`: Registered
  - `49152–65535`: Dynamic/private

## Summary Reflection

This room tied together a lot of earlier concepts like the OSI Model and built on them with real-world protocol behavior. I now clearly understand how data is structured with headers at different layers, and how TCP and UDP differ in reliability and use cases. The Three-Way Handshake makes sense now, and the interactive visuals helped me visualize how data is sent, verified, or lost in transit.
