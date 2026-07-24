# Date : 24.07.2026
## Ex.-No-2-Interconnecting-Two-LANs-Using-a-Router-Basic-Router-Configuration


# Objective
To configure a router to connect two separate LANs and enable communication between them using static IP addressing.
________________________________________
# Apparatus/Tools Required
•	Cisco Packet Tracer<br>
•	2 PCs<br>
•	2 Switches<br>
•	1 Router (e.g., 1841 or 2911)<br>
•	Straight-through cables<br>
________________________________________
# Network Topology Diagram
 Description:<br>
•	PC0 → Switch0 → Router (FastEthernet0/0)<br>
•	PC1 → Switch1 → Router (FastEthernet0/1)<br>
(Insert screenshot of your Packet Tracer setup here)<br>
________________________________________
# IP Addressing Table
Device	Interface	IP Address	Subnet Mask<br>
PC0	NIC	192.168.1.10	255.255.255.0<br>
PC1	NIC	192.168.2.10	255.255.255.0<br>
Router0	FastEthernet0/0	192.168.1.1	255.255.255.0<br>
Router0	FastEthernet0/1	192.168.2.1	255.255.255.0<br>
________________________________________
# Procedure
1.	Open Cisco Packet Tracer and add 2 PCs, 2 Switches, and 1 Router.
2.	Connect each PC to a switch, and each switch to the router using straight-through cables.
3.	Assign IP addresses to both PCs according to the IP table.
4.	Configure the router interfaces:
o	FastEthernet0/0 → 192.168.1.1
o	FastEthernet0/1 → 192.168.2.1
5.	Use no shutdown on both router interfaces to activate them.
6.	Set each PC’s default gateway:<br>
o	PC0 → 192.168.1.1<br>
o	PC1 → 192.168.2.1<br>
7.	Test connectivity using ping from PC0 to PC1.<br>
________________________________________
# Commands Used (Router CLI)
bash<br>
CopyEdit<br>
Router> enable<br>
Router# configure terminal<br>
Router(config)# interface fastethernet0/0<br>
Router(config-if)# ip address 192.168.1.1 255.255.255.0<br>
Router(config-if)# no shutdown<br>

Router(config)# interface fastethernet0/1<br>
Router(config-if)# ip address 192.168.2.1 255.255.255.0<br>
Router(config-if)# no shutdown<br>
________________________________________
# Output (Screenshots)
<img width="1917" height="1027" alt="Screenshot 2026-07-24 105317" src="https://github.com/user-attachments/assets/eb95d0f0-7b36-4fb2-ad09-868cd7377794" />
•	Router CLI configuration<br>
<img width="1917" height="1026" alt="Screenshot 2026-07-24 105405" src="https://github.com/user-attachments/assets/2d579618-8e12-4a66-a03c-65e82d0b41ac" />
•	IP configurations on PCs<br>
<img width="1916" height="1026" alt="Screenshot 2026-07-24 105337" src="https://github.com/user-attachments/assets/a71db53e-4986-4402-ab42-4daf41967d49" />
<img width="1917" height="1030" alt="Screenshot 2026-07-24 105351" src="https://github.com/user-attachments/assets/c7f721d9-0111-4431-a52c-b78bda351a53" />
•	Successful ping between PC0 and PC1<br>
<img width="1917" height="1025" alt="Screenshot 2026-07-24 105457" src="https://github.com/user-attachments/assets/f207dcb7-74f1-4bec-8f4a-50c7206eb9d4" />
<img width="1917" height="1026" alt="Screenshot 2026-07-24 105746" src="https://github.com/user-attachments/assets/feeebd3c-7c11-4903-9396-93e321f6297b" />

________________________________________
# Result
Successfully configured a router to connect two LANs. Communication between PC0 and PC1 across different networks was tested and verified.

