# OSI Model

**Date Completed:** June 29 2025
**Status:** ✅ Completed

---

## 🧠 Key Concepts Learned

- The OSI Model is a conceptual framework for understanding how data moves through a network in 7 layers.
- The 7 layers of the OSI Model are:
  1. **Physical** – raw bits (e.g., cables, switches)
  2. **Data Link** – MAC addresses, switches, Ethernet
  3. **Network** – IP addresses, routing (e.g., routers)
  4. **Transport** – TCP/UDP, ports
  5. **Session** – opening, managing, and closing sessions
  6. **Presentation** – encryption, encoding, compression
  7. **Application** – end-user interfaces like HTTP, DNS, etc.
- Each layer serves the one above and is served by the one below.

---

## 🛠️ Tools & Techniques Used

- N/A – This was a conceptual room without direct tool usage
- Learned to categorize common protocols by OSI layer:
  - HTTP, DNS – Application layer
  - TCP/UDP – Transport layer
  - IP – Network layer
  - MAC – Data Link layer

---

## 📝 Notes

- **Mnemonic for layers (top to bottom):**  
  _All People Seem To Need Data Processing_  
  _(Application, Presentation, Session, Transport, Network, Data Link, Physical)_

- **Encapsulation:** When data is passed from one layer to another, it is wrapped with protocol-specific headers (and sometimes trailers) for that layer.

- **Real-world examples:**
  - Browsing a website involves HTTP (Application) → TCP (Transport) → IP (Network) → Ethernet (Data Link) → Electrical signal (Physical)

---
