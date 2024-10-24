
# Security Features in Cisco Packet Tracer

## 1. Access Control Lists (ACLs)
**Purpose**: ACLs are used to filter network traffic based on IP addresses, protocols, or ports. They can permit or deny traffic to and from network devices.

**CLI Command**:  

`Router(config)# access-list [number] [permit/deny] [protocol] [source] [wildcard mask] [destination] [wildcard mask]`  

## 2. DHCP Snooping

**Purpose**: DHCP Snooping is a security feature that helps prevent rogue DHCP servers from distributing IP addresses and ensures that only trusted DHCP servers are allowed to respond to DHCP requests.

**CLI Commands**:  

`Switch(config)# ip dhcp snooping`  
`Switch(config)# ip dhcp snooping vlan [vlan-id]`  
`Switch(config)# interface [interface-id]`  
`Switch(config-if)# ip dhcp snooping trust`  

## 3. Dynamic ARP Inspection (DAI)

**Purpose**: DAI helps prevent ARP spoofing attacks by validating ARP packets against a trusted binding table, ensuring that only legitimate ARP messages are processed.

**CLI Commands**:  

`Switch(config)# ip arp inspection vlan [vlan-id]`  
`Switch(config)# interface [interface-id]`  
`Switch(config-if)# ip arp inspection trust`  

## 4. Port Security

**Purpose**: Port Security restricts the number of valid MAC addresses on a port, preventing unauthorized devices from connecting to the network.

**CLI Commands**:  

`Switch(config)# interface [interface-id]`  
`Switch(config-if)# switchport port-security`  
`Switch(config-if)# switchport port-security maximum [number]`  
`Switch(config-if)# switchport port-security violation [protect | restrict | shutdown]`  
`Switch(config-if)# switchport port-security mac-address [mac-address]`  

## 5. VLAN Access Control Lists (VACLs)

**Purpose**: VACLs provide a method of filtering traffic on a VLAN basis, controlling traffic flow between VLANs.

**CLI Command**:  

`Switch(config)# ip access-list extended [name]`  
`Switch(config-ext-nacl)# [permit/deny] [protocol] [source] [wildcard] [destination] [wildcard]`  
`Switch(config)# vlan access-map [name] [sequence number]`  
`Switch(config-access-map)# match ip address [access-list number]`  
`Switch(config-access-map)# action [forward | drop]`  

## 6. IP Source Guard

**Purpose**: IP Source Guard restricts IP traffic on untrusted ports based on the DHCP snooping binding table, preventing IP spoofing attacks.

**CLI Command**:  

`Switch(config)# interface [interface-id]`  
`Switch(config-if)# ip verify source`  

## 7. Secure Shell (SSH) Access

**Purpose**: SSH provides a secure, encrypted method to access network devices remotely, enhancing security compared to traditional Telnet.

**CLI Commands**:  

`Router(config)# hostname [router-name]`  
`Router(config)# ip domain-name [domain-name]`  
`Router(config)# crypto key generate rsa`  
`Router(config)# line vty 0 4`  
`Router(config-line)# transport input ssh`  
`Router(config-line)# login local`  


## 8. Authentication, Authorization, and Accounting (AAA)

**Purpose**: AAA is a framework for controlling access to network resources by defining who can access the network (Authentication), what they can do (Authorization), and logging their activities (Accounting).

**CLI Commands**:  

`Router(config)# aaa new-model`  
`Router(config)# aaa authentication login [name] local`  
`Router(config)# aaa authorization exec [name] local`  
`Router(config)# aaa accounting exec [name] start-stop`  

## 9. Network Time Protocol (NTP)

**Purpose**: NTP is used to synchronize the clocks of network devices to ensure time-sensitive logs and events are recorded accurately.

**CLI Command**:  

`Router(config)# ntp server [ip-address]`  

## 10. Firewall and Access Control Policies

**Purpose**: Configuring firewall policies allows for the management of incoming and outgoing traffic based on defined security rules.

**CLI Commands** (using Cisco IOS Firewall):  

`Router(config)# ip access-list extended [name]`  
`Router(config-ext-nacl)# permit | deny [protocol] [source] [wildcard] [destination] [wildcard]`  
`Router(config)# interface [interface-id]`  
`Router(config-if)# ip access-group [name] in | out`  

## 11. Intrusion Prevention System (IPS)

**Purpose**: An IPS monitors network traffic for suspicious activity and can take action to block or prevent potential attacks.

**CLI Commands**:  

`Router(config)# ip ips signature-definition [name]`  
`Router(config)# ip ips interface [interface-id]`  
`Router(config)# ip ips inline`  

## 12. VPN Configuration

**Purpose**: VPNs create secure connections over the internet, allowing remote users to access the network securely.

**CLI Commands** (for IPsec VPN):  

`Router(config)# crypto isakmp policy [priority]`  
`Router(config-isakmp)# authentication pre-share`  
`Router(config-isakmp)# key [key-string] address [peer-ip-address]`  
`Router(config)# crypto ipsec transform-set [name] esp-aes esp-sha-hmac`  
`Router(config)# crypto map [map-name] [sequence-number] ipsec-isakmp`  
`Router(config-crypto-map)# set peer [peer-ip-address]`  
`Router(config-crypto-map)# set transform-set [name]`  
`Router(config-crypto-map)# match address [access-list-number]`  
`Router(config)# interface [interface-id]`  
`Router(config-if)# crypto map [map-name]`  


### RADIUS Authentication

RADIUS (Remote Authentication Dial-In User Service) is used to link network access control with a centralized authentication system. Key advantages of this approach include:

**Centralized User Control:** RADIUS enables secure management of user access to devices and services via a single authentication point.

**AAA Framework:** Configuring RADIUS in simulations allows users to dive into the fundamentals of Authentication, Authorization, and Accounting (AAA).

**Improved Network Security:** By centralizing authentication, only authorized users are granted access to network resources, thus strengthening security.

This hands-on experience with RADIUS authentication provides valuable insight into managing secure access in real-world networks, equipping users with the necessary skills to implement strong security protocols.
