# Network Configuration Documentation

## Overview
This document outlines the steps taken to configure a firewall in Cisco Packet Tracer, simulating a connection to an external network (internet) using a Cloud device.

## 1. **Firewall Configuration**

### a. **Configuring the Firewall Interfaces**
- **Inside Interface (LAN-facing)**:
  - Assigned an IP address in the internal subnet (e.g., `192.168.60.1`).
  
- **Outside Interface (WAN-facing)**:
  - Assigned a public or simulated external IP (e.g., `10.0.0.2`).

### **Setting Up Access Control Lists (ACLs)**
### Allow Outgoing Traffic from LAN to WAN


`access-list OUTSIDE extended permit ip 192.168.60.1 0.0.0.255 any`
*This rule allows internal devices to access the external network.*


### Block Incoming Traffic by Default

`access-list OUTSIDE extended deny ip any 192.168.60.1 255.255.255.0`
*This rule blocks unsolicited incoming traffic from external sources.*

### Apply ACLs to Interfaces

`access-group OUTSIDE in interface outside`

### Firewall Outside Interface Configuration
*Assigned an IP address to the outside interface of the firewall:*

`interface GigabitEthernet0/1`
`ip address 10.0.0.2 255.255.255.0`
`no shutdown`


