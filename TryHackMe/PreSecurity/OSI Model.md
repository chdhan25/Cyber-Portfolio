# OSI Model

**Date Completed:** June 29 2025

## Key Concepts Learned

- The 7 layers of the OSI model and their functions
- Protocols and technologies associated with each layer
- The concept of encapsulation and how data moves through the network stack

## Tools/Commands Introduced

- No hands-on tools in this room
- Focus was on learning protocol placement (e.g., TCP, IP, MAC) and data flow

## Notes

- **OSI Model Layers (Top to Bottom):**

  1. **Application** – User-facing protocols like HTTP, DNS
  2. **Presentation** – Data encoding, encryption (e.g., SSL/TLS)
  3. **Session** – Establishing and managing sessions
  4. **Transport** – Responsible for end-to-end delivery (TCP/UDP)
  5. **Network** – Routing and IP addressing (e.g., IP, ICMP)
  6. **Data Link** – MAC addresses and frame delivery (e.g., Ethernet)
  7. **Physical** – Hardware layer (e.g., cables, NICs)

- **Mnemonic:** _All People Seem To Need Data Processing_

- **Encapsulation:** Each layer adds its own header (and sometimes trailer) as data moves down the stack

- **Real-world Example:**
  - Visiting a website involves:
    - Application: HTTP
    - Transport: TCP
    - Network: IP
    - Data Link: Ethernet
    - Physical: Electrical signal over wire
