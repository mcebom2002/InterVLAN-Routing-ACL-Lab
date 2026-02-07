# InterVLAN-Routing-ACL-Lab

## Overview
This repository contains a Cisco Packet Tracer lab demonstrating **inter-VLAN routing** using a **Router-on-a-Stick** configuration. It includes multiple VLANs, trunking between switches, and an **isolated VLAN** with ACLs to control traffic.

The lab simulates a small corporate network with Admin, Sales, IT, Management, and isolated PCs, showing how VLANs can segment network traffic and how ACLs enforce security policies.

---

## Topology
<img width="958" height="511" alt="Screenshot 2026-02-07 143812" src="https://github.com/user-attachments/assets/c31c2b18-21b3-4ecf-849a-9fab0c570018" />



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
gi0/0.10 - 192.168.10.1
gi0/0.20 - 192.168.20.1
gi0/0.30 - 192.168.30.1
gi0/0.50 - 192.168.50.1
gi0/0.99 - 192.168.99.1

ACL for VLAN50 Isolation:
<img width="746" height="165" alt="Screenshot 2026-02-07 145153" src="https://github.com/user-attachments/assets/26c43ed7-3f36-42c3-bd02-f05f02b06ea8" />
comunication within vlan
<img width="546" height="405" alt="Screenshot 2026-02-07 144449" src="https://github.com/user-attachments/assets/3c44e007-193f-449f-986f-c9126b2173b0" />
intervlan routing
<img width="483" height="257" alt="Screenshot 2026-02-07 144550" src="https://github.com/user-attachments/assets/fddd861b-6b35-4552-b905-c97b1e2ac635" />
vlan isolation
<img width="516" height="227" alt="Screenshot 2026-02-07 144648" src="https://github.com/user-attachments/assets/ca2aedec-8a00-4900-8792-7fc8b2d95d9b" />



