# **NOD's Project**

Welcome to the NOD's project! This project demonstrates how to build a scalable, secure, and organized computer network for different groups of users, using Cisco Packet Tracer.

### **Project Overview**

In this project, we designed a network with four different groups:
- **Management/Secretariat** (5 computers + servers)
- **Study Group** (8 computers)
- **Production Group** (10 computers)
- **Support Group** (2 sectors, 10 computers each)

We used a combination of routers, switches, VLANs, and servers to make sure that each group stays organized and can communicate efficiently.
![alt text](https://github.com/neo01777/NOD-s-cisco-Project/blob/main/08.%20Contents/workplace%20overview.png)

---

## **Network Design Summary**
**[Overview](https://github.com/neo01777/NOD-s-cisco-Project/tree/main/01.%20Overview)**
- Short overview of the project

**[IP Table](https://github.com/neo01777/NOD-s-cisco-Project/tree/main/02.%20IP%20Table)**
- Table of all assigned IP addresses

**[Network Device](https://github.com/neo01777/NOD-s-cisco-Project/tree/main/03.%20Network%20Devices)**
- Routers
- Switches
  
**[Security and Purpose](https://github.com/neo01777/NOD-s-cisco-Project/tree/main/04.%20Security%20and%20purposes)**
- Cable Management
- VLAN
- Acces List
- Cross-Departmental Redundancy
- Radius Authentication
  
**[Cost Efficiency and Scalability](https://github.com/neo01777/NOD-s-cisco-Project/tree/main/05.%20Scalability%20and%20cost%20efficiency)**


## **How Everything Works**

1. **VLANs** keep the groups separated, ensuring that only computers in the same group can talk to each other easily.
2. The **router** lets computers in different VLANs communicate when needed.
3. The **servers** provide essential services like automatic IP address assignment (DHCP), helping computers find each other (DNS), and storing files (Storage).
4. **Distribution switches** make sure that traffic from the different groups gets routed correctly and efficiently.
5. Everything is organized in a way that allows the network to grow easily and remain manageable.

---

## **Challenges Faced**

- **Router Port Limitations**: Initially, we didn’t have enough physical ports on the router for all the groups, so we used **sub-interfaces** to create virtual connections.
- **VLAN Setup**: Setting up and managing the VLANs took some trial and error to ensure that the groups stayed separated and communicated properly.
- **Routing Traffic**: We had to carefully configure the router and switches to make sure that traffic flowed smoothly between the groups.
- **DHCP server**: We had a problem with our DHCP server when we were not using ip address helper that defines the address of a remote DHCP server or DHCP relay agent.
   Up to eight addresses can be defined. The DHCP relay agent forwards DHCP client requests to all defined servers.
---

## **How to Use This Project**

1. **Download the Project File**: Clone or download the Packet Tracer file from this repository.
2. **Open Cisco Packet Tracer**: Load the file into Cisco Packet Tracer.
3. **Explore the Network**: Check out how the different VLANs are set up and how the router connects them.
4. **Test Communication**: Use the **ping** command between different computers to see how they communicate within their VLANs and across VLANs via the router.

---

## **Contributors**

- **Rayane** - Network Design, Configuration and documentation
- **Younes** - Network Design, Configuration and documentation
- **Colin** - Network Design, Configuration and documentation

---

## **Future Improvements**

- **Scalability**: The network can easily be expanded by adding more VLANs and groups.
- **Enhanced Security**: We could add firewalls or advanced access control lists (ACLs) to improve security between VLANs.
- **Monitoring**: Adding monitoring tools to track network performance and usage.

---

