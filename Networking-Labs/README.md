# Networking-Labs

# Enterprise Secure Network Simulation

## 📌 Project Overview
This project showcases the design and implementation of a scalable, enterprise-grade network infrastructure built using **Cisco Packet Tracer**. The core objective was to architect a secure environment featuring department-level segmentation, optimized inter-VLAN routing, and centralized resource hosting.

## 🏗️ Technical Architecture
The infrastructure follows a hierarchical design model to ensure modularity and ease of maintenance:

* **Core/Distribution Layer:** Centralized intelligence via **Cisco 3650 Multilayer Switch**, handling Inter-VLAN routing and SVI management.
* **Access Layer:** Layer 2 connectivity using **Cisco 2960 Switches**, enforcing security zones at the edge.
* **Server Farm:** A hardened, dedicated segment hosting organizational critical services (Secure Web Portal and FTP Server).
* **Edge Layer:** **Cisco 2911 Router** acting as the network gateway, facilitating external connectivity via simulated cloud services.

## 📋 Network Addressing Scheme
| Device | Role | IP Address |
| :--- | :--- | :--- |
| **Router0** | Edge Gateway | 10.0.0.1 |
| **Multilayer Switch0** | Core Switch / Uplink | 10.0.0.2 |
| **VLAN 10** | Management | 192.168.10.1 (GW) |
| **VLAN 20** | Staff | 192.168.20.1 (GW) |
| **VLAN 30** | Guest | 192.168.30.1 (GW) |
| **Server0** | Web/FTP Services | 192.168.10.10 |

## 🚀 Key Implementation Features
- **Network Segmentation:** Achieved via VLANs to isolate traffic and minimize broadcast domains.
- **Inter-VLAN Routing:** Configured SVI interfaces on the L3 switch for efficient layer-3 communication.
- **Service Deployment:** Successfully hosted and verified internal FTP and HTTP services for operational testing.
- **Connectivity:** Integrated cloud-based simulation for end-to-end routing verification.

## 🛡️ Security & Verification
- **Access Control:** Implemented VLAN isolation to prevent unauthorized cross-departmental access.
- **Testing:** Connectivity verified using `ping` and `traceroute` across all VLAN segments.
- **Resource Verification:** Successful retrieval of hosted web pages and FTP files from client workstations.

## 👤 Author
**Abdul Rehman Ahmed**
[LinkedIn Profile](https://www.linkedin.com/in/abdulrehman-ahmed) | [Portfolio](https://github.com/abdulrehman-oss)
