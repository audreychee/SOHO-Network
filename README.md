# 🖧 SOHO VLAN-Based Network Simulation (Cisco Packet Tracer)

This project simulates a secure and segmented SOHO (Small Office/Home Office) network using **Cisco Packet Tracer**, designed to demonstrate CCNA-level networking skills including **VLANs**, **DHCP**, **Telnet remote management**, **router-on-a-stick**, and **wireless integration**.

---

## 📌 Features

- 🔄 Inter-VLAN routing using router subinterfaces
- 📡 Wireless access via separate Access Points for each department
- 🧩 VLAN segmentation:
  - VLAN 10 – Admin
  - VLAN 20 – Sales
  - VLAN 30 – Tech Support
  - VLAN 99 – Management (remote access)
- 📥 DHCP configured per VLAN
- 🔐 Remote Telnet access to router and switch
- 🖨️ Static IP printers per department
- 💻 Wireless and wired client support

---


Each VLAN is mapped to its own subnet with routing handled via subinterfaces on the router. Telnet is enabled for remote CLI access via the Management VLAN.

---

## 📋 Subnet Table

| VLAN | Name        | Subnet             | Gateway IP     | DHCP Range                  | Static IPs (Example)        |
|------|-------------|--------------------|----------------|-----------------------------|-----------------------------|
| 10   | Admin       | 192.168.10.0/24    | 192.168.10.1   | 192.168.10.2 – 192.168.10.100 | AP: 192.168.10.251, Printer: .200 |
| 20   | Sales       | 192.168.20.0/24    | 192.168.20.1   | 192.168.20.2 – 192.168.20.100 | AP: 192.168.20.251, Printer: .200 |
| 30   | Tech        | 192.168.30.0/24    | 192.168.30.1   | 192.168.30.2 – 192.168.30.100 | AP: 192.168.30.251, Printer: .200 |
| 99   | Management  | 192.168.99.0/24    | 192.168.99.1   | *(No DHCP)*                 | Router: .1, Switch: .2       |

---

## ⚙️ Configuration Files

All configurations are available in the [`config`](./config/) folder, including:

- `MainSwitch_Config.txt`
- `MainRouter_Config.txt`
- `Subnet_Table.md`

> You can also open the full topology in Cisco Packet Tracer via the `.pkt` file provided in this repo.

---

## 🧪 Test Cases

- ✅ Clients in each VLAN receive IPs via DHCP
- ✅ Wireless devices can connect and access gateway
- ✅ Telnet access from any VLAN to the router and switch (via VLAN 99)
- ✅ VLANs are isolated unless routed through the router
- ✅ Static printers reachable from same VLAN PCs

---

## 💡 How to Run

1. Open the `.pkt` file in Cisco Packet Tracer (v8.x or higher).
2. Power on all devices.
3. Use PCs to test DHCP and connectivity.
4. Try `telnet 192.168.99.1` from any PC to remotely access the router.

---

## 📂 Files

| File Name                 | Description                                |
|---------------------------|--------------------------------------------|
| `SOHO_Network.pkt`        | Main Cisco Packet Tracer topology file     |
| `configs.txt`             | CLI config script                          |
| `README.md`               | This documentation file                    |

---

## 🛠️ Tools Used

- Cisco Packet Tracer 8.x
- Cisco 2960 Switch
- Cisco ISR 4321 Router
- Access Points, PCs, Printers
- Telnet & DHCP services

---

## 👤 Author

**Audrey Vanessa Chee Wan Tai**  
Bachelor of Computer Science, Swinburne University  

---

