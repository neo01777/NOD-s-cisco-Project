# NOD-s-cisco-Project

# **Computer Playground Network Project**

Welcome to the **Computer Playground Network** project! This project demonstrates how to build a scalable, secure, and organized computer network for different groups of users, using Cisco Packet Tracer.

### **Project Overview**

In this project, we designed a network with four different groups:
- **Management/Secretariat** (5 computers + servers)
- **Study Group** (8 computers)
- **Production Group** (10 computers)
- **Support Group** (2 sectors, 10 computers each)

We used a combination of routers, switches, VLANs, and servers to make sure that each group stays organized and can communicate efficiently.

---

## **Network Design Summary**

### **1. Separation of Groups Using VLANs**
We created four distinct **VLANs** (Virtual Local Area Networks) to separate traffic for each group. Each VLAN acts like a fenced-off area, so computers in different groups stay organized and don’t interfere with each other.

- **Management/Secretariat**: VLAN 10 (IP Range: 192.168.10.0/24)
- **Study Group**: VLAN 20 (IP Range: 192.168.20.0/24)
- **Production Group**: VLAN 30 (IP Range: 192.168.30.0/24)
- **Support Group**: VLAN 40 (IP Range: 192.168.40.0/24)

### **2. Main Router Setup**
The **main router** acts like the front door of the network. It connects the different VLANs and allows them to communicate when needed. We used **sub-interfaces** to give each VLAN its own "virtual door" to pass through.

### **3. Servers Configuration**
We set up three important servers in the Management/Secretariat group:
- **DHCP Server**: Automatically assigns IP addresses to computers in all groups.
- **DNS Server**: Helps computers find each other by name (like a directory).
- **iSCSI Storage Server**: Stores important files and resources for the network.

### **4. Distribution Switches**
To organize the network, we used two **distribution (aggregation) switches**:
- **Aggregation Switch A**: Handles the Study and Production groups.
- **Aggregation Switch B**: Manages the Support groups.

These switches help gather and send traffic from the individual groups to the main router, keeping everything organized and easy to manage.

---

## **How Everything Works**

1. **VLANs** keep the groups separated, ensuring that only computers in the same group can talk to each other easily.
2. The **router** lets computers in different VLANs communicate when needed.
3. The **servers** provide essential services like automatic IP address assignment (DHCP), helping computers find each other (DNS), and storing files (Storage).
4. **Distribution switches** make sure that traffic from the different groups gets routed correctly and efficiently.
5. Everything is organized in a way that allows the network to grow easily and remain manageable.

---

## **IP Address Overview**

| VLAN Group          | IP Range          | Default Gateway    |
|---------------------|-------------------|--------------------|
| Management/Secretariat | 192.168.10.0/24  | 192.168.10.254     |
| Study Group         | 192.168.20.0/24    | 192.168.20.254     |
| Production Group    | 192.168.30.0/24    | 192.168.30.254     |
| Support Group       | 192.168.40.0/24    | 192.168.40.254     |

---

## **Challenges Faced**

- **Router Port Limitations**: Initially, we didn’t have enough physical ports on the router for all the groups, so we used **sub-interfaces** to create virtual connections.
- **VLAN Setup**: Setting up and managing the VLANs took some trial and error to ensure that the groups stayed separated and communicated properly.
- **Routing Traffic**: We had to carefully configure the router and switches to make sure that traffic flowed smoothly between the groups.

---

## **How to Use This Project**

1. **Download the Project File**: Clone or download the Packet Tracer file from this repository.
2. **Open Cisco Packet Tracer**: Load the file into Cisco Packet Tracer.
3. **Explore the Network**: Check out how the different VLANs are set up and how the router connects them.
4. **Test Communication**: Use the **ping** command between different computers to see how they communicate within their VLANs and across VLANs via the router.

---

## **Contributors**

- **Colin** - Network Design and Configuration
- **younes** - Network Design and Configuration
- **Rayane** - Network Design and Configuration

---

## **Future Improvements**

- **Scalability**: The network can easily be expanded by adding more VLANs and groups.
- **Enhanced Security**: We could add firewalls or advanced access control lists (ACLs) to improve security between VLANs.
- **Monitoring**: Adding monitoring tools to track network performance and usage.

---

