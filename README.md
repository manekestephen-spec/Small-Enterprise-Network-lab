# Small-Enterprise-Network-lab
Cisco Enterprise Network Lab built in Packet Tracer, featuring VLANs, inter-VLAN routing, EtherChannel, SSH, DHCP, and server services.

##Project Overview
This project simulates a small enterprise network using Cisco Packet Tracer. The lab focuses on network segmentation, secure device management, inter-VLAN communication, and basic network services and security.

## Network Technologies
- VLANs
- Router-on-a-Stick (ROAS)
- 802.1Q trunking
- EtherChannel / LACP
- SSH
- DHCP
- DNS
- Web Server
- FTP Server
- STP / PortFast / BPDU Guard
- Native VLAN 99
- Port Scurity
- ACLs
- NAT

## VLANs and IP Addressing
| VLAN | Name | Network | Purpose |
|---|---|---|---|
| 10 | SALES | 192.168.10.0/24 | Sales users |
| 20 | IT | 192.168.20.0/24 | IT users |
| 30 | MANGEMENT| 192.168.30.0/24 | General users |
| 40 | SERVER | 192.168.40.0/24 | Network servers |
| 99 | NETMANAGEMENT | 192.168.99.0/24 | Network management |

## Management
VLAN 99 is used as the dedicated Network management and native VLAN.
Switches are managed using SSH with management IP addresses assigned to their VLAN 99 SVIs.

## Servers
The server VLAN contains:
- DNS Server — 192.168.40.2
- Web Server — 192.168.40.3
- FTP Server — 192.168.40.4

## Security
The lab includes:
- SSH for remote switch management
- Local user authentication
- Enable secret
- PortFast
- BPDU Guard
- VLAN segmentation
- Port Security
- ACLs

## Troubleshooting
During testing, VLAN 99 management traffic could not reach the router.
The issue was identified as a native VLAN mismatch between the switch trunk and router.
The switch was configured with VLAN 99 as the native VLAN, while the router was not configured to treat VLAN 99 as native.
The issue was resolved by configuring VLAN 99 as the native VLAN on both sides of the trunk.

## Files
Completed and tested in Cisco Packet Tracer.

##Topology 
<img width="1752" height="732" alt="image" src="https://github.com/user-attachments/assets/c5cf705a-597a-49ce-9c8c-5604b666fa37" />

##Packet Tracer.pkt file

## Device configurations
[GITHUB DOCUMENTATION.docx](https://github.com/user-attachments/files/32352147/GITHUB.DOCUMENTATION.docx)



