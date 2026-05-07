# ospf# 🌐 OSPF Lab

## 📌 Overview
This lab demonstrates the configuration and verification of the OSPF (Open Shortest Path First) routing protocol between multiple routers using dynamic routing.

The lab focuses on how routers:
- Exchange routing information automatically 🔄
- Build neighbor relationships 🤝
- Learn routes dynamically 📡

---

# 🎯 Objectives

✅ Configure OSPF on Cisco routers  
✅ Advertise networks using OSPF  
✅ Establish OSPF neighbor adjacency  
✅ Verify routing tables and OSPF states  
✅ Test connectivity between networks  

---

# 🛠️ Technologies Used

- 🖥️ Cisco Packet Tracer / GNS3
- 🌐 Cisco Routers
- 📡 OSPF Protocol
- 🔢 IPv4 Addressing
- 💻 Cisco CLI

---

# 🗺️ Network Topology
PC1 ----- R1 ----- R2 ----- R3 ----- PC2

---

# 📍 IP Addressing Table

| Device | Interface | IP Address |
|---|---|---|
| R1 | G0/0 | 192.168.1.1/24 |
| R1 | G0/1 | 10.0.12.1/30 |
| R2 | G0/0 | 10.0.12.2/30 |
| R2 | G0/1 | 10.0.23.1/30 |
| R3 | G0/0 | 10.0.23.2/30 |
| R3 | G0/1 | 192.168.3.1/24 |

---

# ⚙️ OSPF Configuration

## 🔹 Router R1
enable
configure terminal

router ospf 1
network 192.168.1.0 0.0.0.255 area 0
network 10.0.12.0 0.0.0.3 area 0

---

## 🔹 Router R2
enable
configure terminal

router ospf 1
network 10.0.12.0 0.0.0.3 area 0
network 10.0.23.0 0.0.0.3 area 0

---

## 🔹 Router R3
enable
configure terminal

router ospf 1
network 10.0.23.0 0.0.0.3 area 0
network 192.168.3.0 0.0.0.255 area 0

---

# 🔍 Verification Commands

## 👥 Check OSPF Neighbors
show ip ospf neighbor

## 📋 Check Routing Table
show ip route

## 🗄️ Check OSPF Database
show ip ospf database

---

# 📶 Connectivity Test

Use ping to verify communication between routers and PCs.

Example:
ping 192.168.3.1

✅ Successful replies indicate that OSPF routing is working correctly.

---

# 📊 Results

- ✅ OSPF neighbors established successfully
- ✅ Dynamic routes learned automatically
- ✅ Full connectivity achieved between all networks

---

# 📚 Key Concepts Learned

📌 Dynamic Routing  
📌 OSPF Areas  
📌 Wildcard Masks  
📌 Neighbor Adjacency  
📌 Route Advertisement  
📌 Routing Table Verification  

---

# 👩‍💻 Author

Nada Ashraf

## 🔗 GitHub
Add your GitHub profile link here.
