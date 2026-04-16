# university-network-cisco-packet-tracer-na
Wireless University Network Simulation cisco packet tracer- MCA Project

# 🌐 Networking in University
### Wireless Campus Network Design using Cisco Packet Tracer

![Cisco Packet Tracer](https://img.shields.io/badge/Cisco-Packet%20Tracer-blue)
![Status](https://img.shields.io/badge/Status-Completed-green)
![MCA Project](https://img.shields.io/badge/MCA-Project%202024--26-orange)

---

## 📋 Project Overview

This project simulates a complete **Wireless University Campus Network** designed
using **Cisco Packet Tracer**. The network covers the entire university including
academic blocks, hostel areas, library, dome building, and IT consulting — all
connected wirelessly.

> Submitted to: University Institute of Computing, Chandigarh University, Mohali
> 
> Academic Year: 2024–26

---

## 👨‍💻 Team Members

| Name | UID |
|------|--------------|
| Hritik Chauhan | 24MCA20339 |
| Keshav Sharma | 24MCA20342 |

**Guide:** Ms. Damanpreet Kaur  
**HOD:** Dr. Amanpreet Kaur Sandhu

---

## 🎯 Objectives

- Design a wireless university network topology in Cisco Packet Tracer
- Implement DNS, Web (HTTP), and Email servers for university services
- Configure routers with RIP dynamic routing protocol
- Secure the network using console passwords and SSH protocol
- Simulate and verify network connectivity using ping tests

---

## 🏗️ Network Architecture

The network is divided into two main areas:

### Campus Area
- Academic Block 1 (AB1)
- Academic Block 2 (AB2)
- Dome Building
- Library
- IT Consulting
- Server Center

### Hostel Area
- Boys Block
- Girls Block

---

## 🖥️ Devices Used

| Device | Model | Quantity |
|--------|-------|----------|
| Router | Cisco 1941 | 3 |
| Switch | Cisco 2960-24TT | 3 |
| Email Server | Server-PT | 1 |
| DNS Server | Server-PT | 1 |
| Web Server (HTTP) | Server-PT | 1 |
| Wireless Access Point | AccessPoint-PT | 7 |
| PCs | PC-PT | 12 |
| Laptops | Laptop-PT | 10 |
| Smartphones | Smartphone-PT | 2 |

---

## 🌐 IP Address Configuration

### Routers

| Router | Interface | IP Address | Subnet Mask |
|--------|-----------|------------|-------------|
| Main Router | GigabitEthernet0/1 | 192.168.2.1 | 255.255.255.0 |
| Main Router | Serial0/1/0 | 10.0.0.1 | 255.0.0.0 |
| Main Router | Serial0/1/1 | 11.0.0.1 | 255.0.0.0 |
| College Router | GigabitEthernet0/0 | 192.168.1.1 | 255.255.255.0 |
| College Router | Serial0/1/0 | 11.0.0.2 | 255.0.0.0 |
| Hostel Router | GigabitEthernet0/0 | 192.168.3.1 | 255.255.255.0 |
| Hostel Router | Serial0/1/0 | 10.0.0.2 | 255.0.0.0 |

### Servers

| Server | IP Address | Gateway | DNS |
|--------|-----------|---------|-----|
| Email Server | 192.168.2.2 | 192.168.2.1 | 192.168.2.3 |
| DNS Server | 192.168.2.3 | 192.168.2.1 | 192.168.2.3 |
| Web Server | 192.168.2.4 | 192.168.2.1 | 192.168.2.3 |

### End Devices

| Area | IP Range | Gateway | DNS |
|------|----------|---------|-----|
| Campus (AB1, AB2, Dome, Library, ITC) | 192.168.1.2 – 192.168.1.17 | 192.168.1.1 | 192.168.2.3 |
| Hostel Boys Block | 192.168.3.6 – 192.168.3.9 | 192.168.3.1 | 192.168.2.3 |
| Hostel Girls Block | 192.168.3.2 – 192.168.3.5 | 192.168.3.1 | 192.168.2.3 |

---

## 📶 Wireless Access Points (SSIDs)

| SSID | Location | Security | Password |
|------|----------|----------|----------|
| muj_dome | Dome Building | WEP | 1234567890 |
| muj_library | Library | WEP | 1234567890 |
| muj_ITC | IT Consulting | WEP | 1234567890 |
| muj_AB1 | Academic Block 1 | WEP | 1234567890 |
| muj_AB2 | Academic Block 2 | WEP | 1234567890 |
| muj_boys | Boys Hostel Block | WEP | 1234567890 |
| muj_girls | Girls Hostel Block | WEP | 1234567890 |

---

## 🔒 Network Security

### Router Passwords

| Router | Console Password | SSH Password |
|--------|-----------------|--------------|
| Main Router | cisco | admin |
| College Router (Router1) | muj@123 | admin |
| Hostel Router (Router2) | muj@123 | admin |

### Security Features
- Console passwords on all routers
- SSH v2 configured for encrypted remote access
- WEP encryption on all wireless access points
- RSA 1024-bit key for SSH encryption

---

## 🔄 Routing Protocol

**RIP (Routing Information Protocol)** is configured on the Main Router with
the following network addresses:
- 10.0.0.0
- 11.0.0.0
- 192.168.1.0
- 192.168.2.0

---

## ✅ Testing & Results

### Ping Tests
| Test | Source | Destination | Result |
|------|--------|-------------|--------|
| Email Server | 192.168.3.4 | 192.168.2.2 | ✅ Success (0% loss) |
| DNS Server | 192.168.1.8 | 192.168.2.3 | ✅ Success (0% loss) |
| Web Server | 192.168.1.2 | 192.168.2.4 | ✅ Success (25% loss first packet only) |

### Service Tests
- ✅ Web Browser successfully accessed `http://192.168.2.4`
- ✅ Email successfully sent and received between hostel devices
- ✅ SSH remote access working between all routers
- ✅ Wireless devices connected to correct access points

---

## 🚀 How to Run This Project

### Requirements
- Cisco Packet Tracer (version 7.0 or above)
- Minimum 8GB RAM
- Any OS (Windows / Mac / Linux)

### Steps
1. Download and install **Cisco Packet Tracer** from
   [netacad.com](https://www.netacad.com)
   (free with Cisco NetAcad account)
2. Clone or download this repository
3. Open the `.pkt` file from the `packet-tracer-file/` folder
4. The complete network will load automatically
5. To test connectivity:
   - Click any PC → Desktop → Command Prompt
   - Type `ping 192.168.2.3` to ping DNS server
   - Type `ping 192.168.2.4` to ping Web server
6. To view simulation:
   - Click Simulation mode (bottom right stopwatch icon)
   - Press Play to watch packets travel

---

## 📸 Screenshots

### Complete Network Topology
![Topology](screenshots/complete-topology.png)

### Ping Test Results
![Ping Email](screenshots/ping-test-email-server.png)
![Ping DNS](screenshots/ping-test-dns-server.png)

### Simulation Mode
![Simulation](screenshots/simulation-mode.png)

### Web Server Access
![Web Browser](screenshots/web-browser-test.png)

### Email Communication
![Email](screenshots/email-received.png)

---

## 🔮 Future Improvements

- Upgrade WEP to **WPA2/WPA3** for stronger wireless security
- Add a **DHCP server** for automatic IP assignment
- Implement **VLANs** for better traffic segmentation
- Add a **Firewall** for perimeter security
- Expand network to cover more university buildings

---

## 📚 References

1. [Cisco Packet Tracer - Wikipedia](https://en.wikipedia.org/wiki/Packet_Tracer)
2. [What is a Server - Paessler](https://www.paessler.com/it-explained/server)
3. [SSH Configuration on Router](https://computernetworking747640215.wordpress.com/2018/07/05/secure-shell-sshconfiguration-on-a-switch-and-router-in-packet-tracer/)
4. [Benefits of Wireless Networking](https://www.cognoscape.com/benefits-going-wireless/)

---

## 📄 License

This project is submitted as an academic mini-project for
**MCA 2024-26, Chandigarh University**.
Free to use for educational and learning purposes.
