# SOHO VLAN-Based Network Simulation

A comprehensive network simulation demonstrating enterprise-grade VLAN segmentation, inter-VLAN routing, and wireless integration using Cisco Packet Tracer. This project showcases CCNA-level networking concepts including router-on-a-stick configuration, DHCP services, and remote management capabilities.

## Overview

This Small Office/Home Office (SOHO) network simulation implements a secure, segmented network infrastructure designed for a multi-department organization. The topology demonstrates best practices in network design, security, and management through VLAN implementation and proper subnet allocation.

## Network Architecture

### Core Features

- **Inter-VLAN Routing**: Router-on-a-stick configuration using subinterfaces
- **Wireless Integration**: Dedicated access points for each department
- **Network Segmentation**: Four distinct VLANs for organizational separation
- **Dynamic IP Assignment**: DHCP pools configured per VLAN
- **Remote Management**: Telnet access for network administration
- **Print Services**: Static IP printers deployed per department
- **Hybrid Connectivity**: Support for both wired and wireless clients

### VLAN Structure

| VLAN ID | Department | Purpose | Subnet | Gateway |
|---------|------------|---------|---------|---------|
| 10 | Admin | Administrative operations | 192.168.10.0/24 | 192.168.10.1 |
| 20 | Sales | Sales department operations | 192.168.20.0/24 | 192.168.20.1 |
| 30 | Tech Support | Technical support services | 192.168.30.0/24 | 192.168.30.1 |
| 99 | Management | Network management and monitoring | 192.168.99.0/24 | 192.168.99.1 |

## IP Address Allocation

### DHCP Ranges
- **Admin VLAN (10)**: 192.168.10.2 - 192.168.10.100
- **Sales VLAN (20)**: 192.168.20.2 - 192.168.20.100
- **Tech Support VLAN (30)**: 192.168.30.2 - 192.168.30.100
- **Management VLAN (99)**: Static assignment only

### Static IP Assignments
- **Access Points**: .251 in respective VLAN subnets
- **Printers**: .200 in respective VLAN subnets
- **Network Infrastructure**: 
  - Router: 192.168.99.1
  - Switch: 192.168.99.2

## Technical Implementation

### Equipment Used
- **Router**: Cisco ISR 4321 with subinterface configuration
- **Switch**: Cisco Catalyst 2960 with VLAN support
- **Wireless**: Access points with VLAN tagging capability
- **End Devices**: PCs, laptops, and network printers

### Key Configurations
- **Trunking**: 802.1Q VLAN tagging between router and switch
- **DHCP**: Centralized DHCP server on router with per-VLAN pools
- **Security**: VLAN isolation with controlled inter-VLAN routing
- **Management**: Telnet access via dedicated management VLAN

## Testing and Validation

### Connectivity Tests
- ✅ DHCP IP assignment verification for all VLANs
- ✅ Wireless device connectivity and internet access
- ✅ Inter-VLAN communication through router
- ✅ VLAN isolation and security verification
- ✅ Remote management access via Telnet
- ✅ Printer accessibility within respective VLANs

### Performance Metrics
- Network segmentation effectiveness
- DHCP lease assignment success rate
- Wireless connectivity stability
- Remote management accessibility

## Getting Started

### Prerequisites
- Cisco Packet Tracer 8.x or higher
- Basic understanding of networking concepts
- Familiarity with Cisco CLI commands

### Installation and Setup
1. Download and open `SOHO Network.pkt` in Cisco Packet Tracer
2. Power on all network devices in sequence:
   - Router first
   - Switch second
   - Access points and end devices last
3. Allow DHCP services to initialize (30-60 seconds)
4. Verify connectivity using built-in PC tools

### Testing the Network
```bash
# Test DHCP assignment
ipconfig /all

# Test inter-VLAN connectivity
ping 192.168.20.1

# Test remote management
telnet 192.168.99.1
```

## Configuration Files

All device configurations are documented in the `configs.txt` file, including:
- Complete switch VLAN configuration
- Router subinterface setup
- DHCP pool configurations
- Security and access control settings

## Project Structure

```
SOHO-Network-Simulation/
├── README.md                 # Project documentation
├── SOHO Network.pkt         # Cisco Packet Tracer topology
├── configs.txt              # Device configuration scripts
└── .gitignore              # Git ignore rules
```

## Learning Objectives

This simulation demonstrates proficiency in:
- VLAN design and implementation
- Inter-VLAN routing configuration
- DHCP service deployment
- Network security through segmentation
- Wireless network integration
- Remote network management
- Cisco CLI configuration

## Future Enhancements

Potential improvements and extensions:
- Implementation of Access Control Lists (ACLs)
- Network Address Translation (NAT) for internet connectivity
- Enhanced security with port security features
- Quality of Service (QoS) configuration
- Network monitoring and logging capabilities

## Author

**Audrey Vanessa Chee Wan Tai**  
Bachelor of Computer Science  
Swinburne University of Technology

---

*This project demonstrates practical application of networking concepts learned in CCNA coursework and serves as a foundation for advanced network design and implementation.*