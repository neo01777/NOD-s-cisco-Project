# Network Devices Configuration Guide

## Routers

Routers serve to connect different networks, routing data packets from one network to another based on their IP addresses. Below are key aspects of router configuration:

### 1. Interfaces
Configure IP addresses and subnet masks for each interface that connects to different segments of the network. Common interfaces include:

- **LAN Interface**: Connects to the local area network.
- **WAN Interface**: Connects to wide area networks, such as the internet.
- **Management Interface**: Used for administrative access to the router.

### 2. Routing Protocols
Set up routing protocols to facilitate the dynamic learning and sharing of routing information among routers, or configure static routes for fixed traffic paths. Key protocols include:

- **Dynamic Routing Protocols**: Such as DHCP and OSPF, which automatically share routing information.
- **Static Routes**: Manually defined paths for traffic between networks.

### 3. Access Control Lists (ACLs)
Implement ACLs to control what traffic can enter or leave the network through the router, enhancing overall security. ACLs can specify rules for both inbound and outbound traffic.

---

## Switches

Switches connect devices within the same network and utilize MAC addresses to forward data to the appropriate destination. Key aspects of switch configuration include:

### 1. Port Configuration
Assign ports to specific VLANs (Virtual Local Area Networks) to segment network traffic effectively. Configuration tasks include:

- **VLAN Assignment**: Designate ports for specific VLANs to isolate traffic.
- **Port Speeds**: Configure the speed of each port.
- **Duplex Modes**: Set up half-duplex or full-duplex modes as required.

### 2. VLANs
Define VLANs to segment the network into smaller, isolated groups. This practice helps improve network performance and enhances security.

### 3. Port Security
Configure port security features to control access at the port level. This may include:

- **MAC Address Limitation**: Restrict the number of MAC addresses that can connect to a specific port.
- **MAC Address Filtering**: Allow access only to specified MAC addresses, enhancing security.

---
