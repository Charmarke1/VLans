# VLANs

![Cisco switch with three vlan](E046E633-A3B8-49C0-8852-C8503ADE62D0.png)

## Overview:

**A VLAN (Virtual Local Area Network)** is a logical grouping of devices on a network, designed to create separate broadcast domains without requiring separate physical networks.

- **Purpose:**

VLANs help segment a larger network into smaller, isolated groups, which enhances security, reduces congestion by limiting broadcast traffic, and simplifies network management.

- **How It Works:**

Even if devices are connected to the same physical switch, assigning them to different VLANs means they “live” in different network spaces. This logical separation ensures that broadcast traffic stays within each VLAN.

- **Benefits:**
   - **Improved Security:** Limits the spread of sensitive information and isolates potential threats.
   - **Efficient Traffic Management:** Reduces network congestion by confining broadcast traffic.
   - **Simplified Administration:** Enables easier network reconfiguration and management without physical changes.

- Implementation:
VLANs are typically implemented using managed switches that support VLAN configuration. Traffic between VLANs (when necessary) is handled by a router or a Layer 3 switch through a process known as inter-VLAN routing.

 ## Network Environment
You're building a VLAN-based network in Cisco Packet Tracer using:

🖧 Devices
- 1 Router – Handles inter-VLAN routing using Router-on-a-Stick.

- 1 24-Port Switch – Connects all devices and assigns VLANs.

- 9 PCs – Divided into 3 VLANs (3 PCs per VLAN).

🧩 VLAN Configuration

- VLAN 10 – Assigned to the first 3 PCs.

- VLAN 20 – Assigned to the next 3 PCs.

- VLAN 30 – Assigned to the last 3 PCs.

Each group is isolated at Layer 2 but will be able to communicate through the router.
|

### 🔁 Trunking
A trunk link is configured between the switch and router (e.g., Switch fa0/1 to Router g0/0).

This trunk carries traffic for all VLANs, using 802.1Q tagging.

The router uses sub-interfaces (like g0/0.10, g0/0.20, g0/0.30) for each VLAN and handles inter-VLAN routing.

🔗 Connectivity
PCs connect to the switch via access ports assigned to their respective VLANs.

The switch forwards traffic to the router through the trunk port.

The router processes and routes traffic between VLANs as needed.

🎯 Purpose
Demonstrate VLAN segmentation to separate traffic.

Enable inter-VLAN routing using a single physical router interface (Router-on-a-Stick).

Practice switchport configuration, VLAN setup, trunking, and basic IP addressing.

