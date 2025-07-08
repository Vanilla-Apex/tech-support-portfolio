# 📊 Network Lab Log: Practicing Subnetting and IP Planning in Packet Tracer

## 🎯 Purpose

To practice subnetting and IP planning using Cisco Packet Tracer for small network labs, aligned with CompTIA Network+ objectives.

---

## 🗂️ Lab Overview

- Designed a small office network with:
  - 1 Router
  - 2 Switches
  - 4 PCs (2 on each subnet)

- Subnet Plan:
  - Subnet A: 192.168.10.0/24
  - Subnet B: 192.168.20.0/24

---

## 🪜 Steps Taken

1️⃣ Designed the topology in Packet Tracer  
2️⃣ Assigned static IP addresses to each PC  
3️⃣ Configured router interfaces for each subnet:
```
Router> enable
Router# configure terminal
Router(config)# interface FastEthernet0/0
Router(config-if)# ip address 192.168.10.1 255.255.255.0
Router(config-if)# no shutdown
Router(config)# interface FastEthernet0/1
Router(config-if)# ip address 192.168.20.1 255.255.255.0
Router(config-if)# no shutdown
```
4️⃣ Set default gateways on each PC  
5️⃣ Verified connectivity using `ping` between subnets

---

## ✅ Outcome

- Successfully designed and implemented a two-subnet network in Packet Tracer
- Confirmed cross-subnet connectivity and correct IP planning

---

## 💡 Skills Practiced

- Subnetting
- IP address planning
- Router interface configuration
- Troubleshooting network connectivity
