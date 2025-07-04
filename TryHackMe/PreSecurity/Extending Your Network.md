# Extending Your Network

**Date Completed:** July 3 2025

## Key Concepts Learned

- How port forwarding exposes services from a private network to the public Internet
- The role and types of firewalls in network security
- Basics of VPNs and why they’re used for privacy, security, and remote connectivity
- How routers and switches function and differ in a network
- Introduction to VLANs and layer 2 vs. layer 3 switches

## Tools/Commands Introduced

- No CLI tools used; this room focused on conceptual and visual learning
- Learned how firewalls inspect packets and how VPNs form encrypted tunnels

## Notes

### Port Forwarding

- Configured at the router to make services (like a web server on port 80) accessible from outside the private network
- Enables devices on the Internet to access internal services using the network’s public IP and a specified port
- Port forwarding opens specific ports, while firewalls determine whether traffic is allowed across them

### Firewalls 101

- Firewalls control which traffic is allowed to enter or exit a network
- Operate primarily at OSI layers 3 and 4 (Network and Transport layers)
- **Stateful firewalls**: Track full connections and make dynamic decisions; more secure but resource-intensive
- **Stateless firewalls**: Apply static rules to each individual packet; faster but less flexible

### VPN Basics

- A Virtual Private Network (VPN) creates a secure, encrypted tunnel between devices across the Internet
- Benefits include:
  - Secure access between remote offices or networks
  - Encryption for privacy, especially on public Wi-Fi
  - Anonymity by hiding user activity from ISPs or surveillance
- VPN Technologies:
  - **PPP**: Handles authentication and encryption, but is not routable on its own
  - **PPTP**: Allows PPP traffic to travel across the Internet; easy to set up but weak encryption
  - **IPSec**: Uses the Internet Protocol framework to provide strong encryption; more complex to set up

### LAN Networking Devices

**Router**

- Connects multiple networks and forwards packets between them
- Makes routing decisions based on factors like shortest path, reliability, and medium type
- Operates at OSI Layer 3

**Switch**

- Connects multiple devices within the same network
- Layer 2 switches forward frames using MAC addresses
- Layer 3 switches can route packets using IP addresses, similar to a router

**VLAN (Virtual LAN)**

- Allows logical segmentation of devices on the same physical switch
- Devices in separate VLANs can access the Internet but are isolated from each other internally
- Improves network security and traffic control

## Summary Reflection

This room helped solidify my understanding of how networks expand beyond local environments. I learned the difference between a router and a switch, and how VPNs ensure secure remote access. The distinction between stateful and stateless firewalls was particularly useful, and it tied together previous lessons about protocols, ports, and data control.
