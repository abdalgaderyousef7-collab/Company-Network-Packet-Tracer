# Company Network - Cisco Packet Tracer

## Project Overview

This project is a complete enterprise network simulation developed using Cisco Packet Tracer.

The network is designed to simulate a real company environment with multiple departments, VLANs, Layer 3 switching, redundancy, routing, network security, and server connectivity.

## Network Topology

The network consists of:

- CORE-SW1
- DSW1
- DSW2
- ASW-F1
- ASW-F2
- ASW-F3
- ASW-F4
- ServerSW
- End devices
- Servers

## VLANs

| VLAN | Purpose |
|------|---------|
| 10 | Department 1 |
| 20 | Department 2 |
| 30 | Department 3 |
| 40 | Department 4 |
| 50 | Department 5 |
| 60 | Department 6 |
| 70 | Department 7 |
| 99 | Management |
| 999 | Native / Unused VLAN |

## Technologies Implemented

- VLAN
- Access Ports
- Trunking
- Native VLAN
- Inter-VLAN Routing
- Static Routing
- OSPF
- DHCP
- NAT / PAT
- Access Control Lists (ACL)
- Port Security
- STP / RSTP
- EtherChannel
- LACP
- Layer 3 Switching
- Network Redundancy
- Management VLAN
- Unused Port Security

## Switching and Redundancy

The network uses multiple distribution switches and a core switch to provide redundancy and improve network availability.

EtherChannel using LACP is configured between the switching infrastructure.

STP is used to prevent Layer 2 loops and provide controlled path selection.

## Network Security

The project includes several network security mechanisms:

- Port Security
- Sticky MAC Addresses
- Port Security Violation Modes
- Unused VLAN
- Disabled unused ports
- Extended ACLs
- Management VLAN

## Routing

Routing is implemented using Layer 3 switches and routers where required.

OSPF is used for dynamic routing between Layer 3 network devices.

Static routes are also configured where appropriate.

## DHCP

DHCP is configured to automatically provide IP addressing information to end devices.

DHCP provides:

- IP Address
- Subnet Mask
- Default Gateway
- DNS Server

## NAT

NAT/PAT is configured to allow internal private networks to communicate with external networks.

## Access Control Lists

Extended ACLs are used to control traffic between specific networks and services.

Example:

- Restricting HTTP/HTTPS traffic
- Controlling SSH access
- Controlling DNS traffic
- Allowing required network traffic

## Testing

The network was tested using:

- Ping
- Traceroute
- VLAN verification
- Trunk verification
- EtherChannel verification
- STP verification
- Routing table verification
- DHCP verification
- ACL testing
- Port Security testing

## Project File

The main Packet Tracer project is:

`Company-Network.pkt`

Open the file using Cisco Packet Tracer.

## Skills Demonstrated

This project demonstrates practical knowledge of:

- Cisco switching
- Cisco routing
- VLAN design
- Network segmentation
- Layer 2 redundancy
- Layer 3 routing
- Network security
- Troubleshooting
- Enterprise network design
- Cisco IOS configuration

## Author

Abdalgader Yousef Ahmed Abdalgader

IT Graduate | Aspiring Network Engineer

## Tools

- Cisco Packet Tracer
- Cisco IOS
