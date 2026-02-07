# InterVLAN-Routing-ACL-Lab
# MultiVLAN-Router-On-A-Stick-Lab

## Overview
This repository contains a Cisco Packet Tracer lab demonstrating **inter-VLAN routing** using a **Router-on-a-Stick** configuration. It includes multiple VLANs, trunking between switches, and an **isolated VLAN** with ACLs to control traffic.

The lab simulates a small corporate network with Admin, Sales, IT, Management, and isolated PCs, showing how VLANs can segment network traffic and how ACLs enforce security policies.

---

## Topology

**Devices:**
- **Router0** – Inter-VLAN routing (Router-on-a-Stick)
- **SW0** – Connects Admin, Sales, IT, and one isolated PC
- **SW1** – Connects Management, Sales, and one isolated PC
- **PCs** – Connected to switches according to VLANs

**VLANs and Subnets:**

| VLAN | Name       | Subnet           | SW0 PCs        | SW1 PCs   |
|------|------------|----------------|----------------|-----------|
| 10   | Admin      | 192.168.10.0/24 | Admin1, Admin2 | -         |
| 20   | Sales      | 192.168.20.0/24 | Sales1, Sales2 | Sales3    |
| 30   | IT         | 192.168.30.0/24 | IT1, IT2       | -         |
| 50   | Isolated   | 192.168.50.0/24 | Isolated1      | Isolated2 |
| 99   | Management | 192.168.99.0/24 | -              | MGMT      |

---

## Connectivity

**Trunk ports:**
- SW0 ↔ Router0 → all VLANs
- SW0 ↔ SW1 → all VLANs

**Router subinterfaces:**
