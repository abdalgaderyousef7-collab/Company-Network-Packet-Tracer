# Enterprise Company Network

### Cisco Packet Tracer Network Simulation

![Cisco Packet Tracer](https://img.shields.io/badge/Cisco%20Packet%20Tracer-Network%20Simulation-blue)
![Networking](https://img.shields.io/badge/Focus-Networking-green)
![CCNA](https://img.shields.io/badge/Level-CCNA-orange)

## Project Overview

This project is an enterprise company network simulation developed using **Cisco Packet Tracer**.

The network was designed to simulate a real-world company environment using a hierarchical network architecture with **Core, Distribution, and Access layers**.

The project focuses on practical implementation of Cisco switching, routing, VLAN segmentation, redundancy, network security, DHCP, NAT, ACLs, and troubleshooting.

---

## Network Architecture

The network follows a hierarchical design:

```text
                    ┌───────────────┐
                    │   CORE-SW1    │
                    │  Core Layer   │
                    └───────┬───────┘
                            │
                ┌───────────┴───────────┐
                │                       │
         ┌──────▼──────┐         ┌──────▼──────┐
         │    DSW1     │         │    DSW2     │
         │ Distribution│         │ Distribution│
         └──────┬──────┘         └──────┬──────┘
                │                       │
        ┌───────┼────────┐       ┌──────┼───────┐
        │       │        │       │      │       │
      ASW-F1  ASW-F2   ASW-F3  ASW-F4  ServerSW
        │       │        │       │      │
      PCs     PCs      PCs     PCs    Servers
```

The design provides:

* Network segmentation using VLANs
* Redundant switching paths
* Layer 2 loop prevention
* Inter-VLAN communication
* Centralized network management
* Improved scalability

---

## Devices

| Device      | Role               |
| ----------- | ------------------ |
| CORE-SW1    | Core Layer         |
| DSW1        | Distribution Layer |
| DSW2        | Distribution Layer |
| ASW-F1      | Access Layer       |
| ASW-F2      | Access Layer       |
| ASW-F3      | Access Layer       |
| ASW-F4      | Access Layer       |
| ServerSW    | Server Network     |
| End Devices | Client Network     |
| Servers     | Server Services    |

---

## VLAN Design

| VLAN | Purpose              |
| ---: | -------------------- |
|   10 | Department 1         |
|   20 | Department 2         |
|   30 | Department 3         |
|   40 | Department 4         |
|   50 | Department 5         |
|   60 | Department 6         |
|   70 | Department 7         |
|   99 | Management           |
|  999 | Native / Unused VLAN |

VLAN segmentation separates departments and reduces unnecessary broadcast traffic while providing a structured network design.

---

## Networking Technologies

### Switching

* VLAN configuration
* Access ports
* Trunk ports
* Native VLAN
* Inter-VLAN Routing
* Layer 3 Switching
* STP / RSTP
* EtherChannel
* LACP
* Port Security
* Sticky MAC addresses
* Unused port protection

### Routing

* Connected routes
* Static routing
* Dynamic routing
* OSPF
* Default routing

### Network Services

* DHCP
* DNS
* NAT
* PAT

### Security

* Extended ACLs
* Port Security
* Sticky MAC
* Port Security violation modes
* Management VLAN
* Unused VLAN
* Disabled unused ports

---

## EtherChannel

EtherChannel is implemented using **LACP** to combine multiple physical links into logical interfaces.

Example logical interfaces:

```text
Po2
Po3
```

This provides:

* Increased link capacity
* Link redundancy
* Simplified STP operation

---

## Spanning Tree Protocol

STP/RSTP is used to prevent Layer 2 switching loops.

The network is designed to provide controlled path selection and redundancy between the Core and Distribution layers.

STP verification was performed using:

```text
show spanning-tree
```

---

## Routing

Layer 3 switching is used to provide routing between VLANs and network segments.

OSPF is used for dynamic route exchange between Layer 3 devices.

Example verification commands:

```text
show ip route
show ip ospf neighbor
show ip protocols
```

---

## DHCP

DHCP provides automatic network configuration to client devices.

Clients receive:

* IP Address
* Subnet Mask
* Default Gateway
* DNS Server

DHCP operation was verified using:

```text
show ip dhcp binding
```

---

## Network Security

Several security mechanisms were implemented.

### Port Security

Port Security restricts unauthorized devices from connecting to protected switch ports.

The configuration includes:

* Sticky MAC addresses
* Maximum MAC address limits
* Violation modes
* Err-disabled behavior
* Unused port protection

Example verification:

```text
show port-security
show port-security interface
```

### Access Control Lists

Extended ACLs are used to control traffic between networks and specific services.

The project includes traffic filtering for services such as:

* HTTP
* HTTPS
* SSH
* DNS

ACL behavior was tested using connectivity and service-access tests.

---

## NAT / PAT

NAT/PAT is used to translate private internal addresses to external addresses.

This demonstrates how internal company networks can communicate with external networks while using private IPv4 addressing.

---

## Testing & Verification

The network was tested using Cisco IOS verification commands and end-to-end connectivity tests.

### Connectivity

```text
ping
traceroute
```

### VLAN

```text
show vlan brief
```

### Trunking

```text
show interfaces trunk
```

### EtherChannel

```text
show etherchannel summary
```

### STP

```text
show spanning-tree
```

### Routing

```text
show ip route
show ip ospf neighbor
```

### DHCP

```text
show ip dhcp binding
```

### Port Security

```text
show port-security
show port-security interface
```

The tests were used to verify VLAN connectivity, routing, redundancy, security policies, and network services.

---

## Troubleshooting

During development, the network was tested and troubleshooting was performed for common Cisco networking issues, including:

* VLAN configuration problems
* Trunk mismatches
* Native VLAN mismatches
* EtherChannel configuration issues
* STP path selection
* Routing problems
* ACL traffic restrictions
* Port Security violations
* Incorrect switchport modes

The troubleshooting process relied on Cisco IOS commands and systematic Layer 2 / Layer 3 verification.

---

## Project Structure

```text
Company-Network-Packet-Tracer/
│
├── Company-Network.pkt
└── README.md
```

The main `.pkt` file contains the complete Cisco Packet Tracer network simulation.

---

## How to Use

1. Install **Cisco Packet Tracer**.
2. Download or clone this repository.
3. Open:

```text
Company-Network.pkt
```

4. Explore the topology.
5. Access the Cisco IOS CLI on the network devices.
6. Use the verification commands documented above to inspect the configuration.

---

## Skills Demonstrated

This project demonstrates practical knowledge in:

* Cisco IOS
* Enterprise Network Design
* VLANs
* Trunking
* Inter-VLAN Routing
* Layer 2 Switching
* Layer 3 Switching
* OSPF
* Static Routing
* DHCP
* NAT / PAT
* ACLs
* STP / RSTP
* EtherChannel / LACP
* Port Security
* Network Troubleshooting
* Network Segmentation
* Redundancy

---

## Project Objective

The main objective of this project was to move from theoretical networking concepts to a practical enterprise network implementation.

The project was built to practice designing, configuring, testing, and troubleshooting a multi-VLAN Cisco network similar to a real company environment.

---

## Author

**Abdalgader Yousef Ahmed Abdalgader**

IT Graduate | Aspiring Network Engineer

### Focus

```text
Networking
Cisco
CCNA
Enterprise Network Design
Network Troubleshooting
```

---

## Tools

* Cisco Packet Tracer
* Cisco IOS
* Git
* GitHub
