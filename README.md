# Project 1 – Small Office Network with VLANs & Inter-VLAN Routing (Packet Tracer)

## 📌 Overview
This project simulates a small office network with multiple departments that require network segmentation while maintaining controlled communication between them.

The network uses **VLANs** for logical separation and **router-on-a-stick** to enable **inter-VLAN routing**. This project demonstrates **foundational CCNA networking skills** including switching, IP addressing, and basic routing.

---

## 🖧 Network Topology

### Logical Topology
```text
           Router
           Switch
| PCs | ── | PCs | ── | PCs | 
 (IT)      (Sales)    (Guest)
```

## 🗺️ VLAN & IP Addressing Scheme

### VLAN Design
| VLAN ID | Name  | Subnet |
|--------|-------|--------|
| 10 |  IT  | 192.168.10.0/24 |
| 20 | SALES | 192.168.20.0/24 |
| 30 | Guest | 192.168.30.0/24 |

### Default Gateways
| VLAN | Gateway |
|----|---------|
| IT | 192.168.10.1 |
| SALES | 192.168.20.1 |
| GUEST | 192.168.30.1 |

---

## ⚙️ Technologies Implemented

### 🔹 VLANs
- Logical separation of departments
- Improved security and traffic management

### 🔹 Trunking
- 802.1Q trunk between switch and router
- Allows multiple VLANs over a single physical link

### 🔹 Inter-VLAN Routing
- Router-on-a-stick configuration
- Subinterfaces used for each VLAN

---

## 🛠️ Configuration Summary

### Switch Configuration
- VLAN creation and naming
- Access port assignment per department
- Trunk port configuration to router

### Router Configuration
- Subinterfaces for each VLAN
- 802.1Q encapsulation
- Default gateway functionality for all VLANs

---

## ✅ Verification & Testing

The following tests were successfully performed:

- Devices within the same VLAN can communicate
- Devices in different VLANs can communicate via router
- Default gateways reachable from all hosts

### Verification Commands
```plaintext
show vlan brief
show interfaces trunk
show ip route
ping
