# CCNA Lab 03 – Inter-VLAN Routing with Layer 3 Switch (SVI)

## 🧠 Objective
Establish communication between two VLANs using a Layer 3 Switch and Switch Virtual Interfaces (SVIs), without a separate router.

## 🧱 Topology
- 1x Layer 3 Switch  
- 2x PCs (PC1 and PC2)  
- VLAN 10: PC1  
- VLAN 20: PC2  

## 🛠️ Configuration Summary
- VLAN 10 and VLAN 20 created on the switch
- Ports assigned to respective VLANs in access mode
- SVIs created and assigned IPs:
  - VLAN 10 SVI: 192.168.10.1/24
  - VLAN 20 SVI: 192.168.20.1/24
- PC1 IP: 192.168.10.10/24, Gateway: 192.168.10.1  
- PC2 IP: 192.168.20.10/24, Gateway: 192.168.20.1  

## ✅ Results
- Initial pings failed due to ARP learning delay  
- After retry, successful ping from PC2 to PC1:
  - 4 packets sent, 4 received, 0% loss
  - TTL = 127 confirms Layer 3 reachability  

## 📸 Screenshots
![image](https://github.com/user-attachments/assets/05a1cbe9-e5c0-44ed-8090-a2769d095f2c)


## 💡 Notes
- SVIs must be enabled (`no shutdown`)
- Layer 3 Switch must have routing enabled (`ip routing`)
- Always check that ports are assigned correctly to VLANs

## 📂 Files
- `.pkt` Packet Tracer file
- This README
- Screenshot of successful ping test

## 🧩 Optional Extensions
- Add third VLAN and another PC  
- Test ACLs to restrict VLAN communication  
- Add DHCP relay to dynamically assign IPs
