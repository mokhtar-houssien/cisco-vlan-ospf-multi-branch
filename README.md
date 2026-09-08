# 🌐 Small Enterprise Network Lab (Multi-Branch Topology)

A comprehensive enterprise network simulation built using **Cisco Packet Tracer**, featuring multi-branch connectivity, VLAN segmentation, Trunking, and dynamic routing via **OSPF**.

---

## 🛠️ Project Architecture & Topologies

- **Routers:** 2 x Cisco 1841 (`Branch1-Router`, `Branch2-Router`) connected via a WAN serial link.
- **Switches:** 2 x Cisco 2900-24TT (`Branch1-Switch`, `Branch2-Switch`) configured with IEEE 802.1Q Trunking and Access ports.
- **End Devices:** 8 x PCs distributed across multiple VLANs.

---

## ⚙️ Implemented Configurations

1. **VLAN Segmentation & Inter-VLAN Routing:**
   - **Branch 1:** VLAN 10 (`192.168.10.0/24`), VLAN 20 (`192.168.20.0/24`) routed via Router-on-a-Stick (`FastEthernet0/0.10` & `FastEthernet0/0.20`).
   - **Branch 2:** VLAN 30 (`192.168.30.0/24`), VLAN 40 (`192.168.40.0/24`) routed via Router-on-a-Stick (`FastEthernet0/0.10` & `FastEthernet0/0.20`).

2. **WAN & Dynamic Routing (OSPF):**
   - Configured Serial interfaces (`Serial0/0/0`) with subnet `10.0.0.0/24`.
   - Enabled **OSPF Protocol** on both routers to dynamically exchange routing tables and ensure full end-to-end reachability.

3. **Security & Management:**
   - Configured secure hostnames and console access.
   - Saved running configurations (`startup-config`).

---

## 🧪 Testing & Troubleshooting
- Verified dynamic path discovery using `show ip route` (confirmed **`O`** routes).
- Tested inter-branch and intra-branch connectivity successfully using `ping`.

---
*Developed by **Mokhtar Houssien***
