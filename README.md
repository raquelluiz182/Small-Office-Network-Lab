This project simulates a small office network created using Cisco Packet Tracer.

The main objective was to practice basic networking concepts, including IPv4 addressing, subnet masks, default gateways, switch connectivity, router configuration and network segmentation.
nd 
Network Topology

The network consists of:
1 Router
2 Switch
3 PCs
1 Server


Network addresses:
Switch 1 : 192.168.10.0 /24 - router interface 192.168.10.1
Switch 2 : 192.168.20.0 /24 - router interface 192.168.20.1



IP Addressing
Device	 IPv4 Address	  Subnet Mask  	 Default Gateway
Router	 192.168.10.1	  255.255.255.0     	—
PC1	     192.168.10.10	255.255.255.0  	192.168.10.1
PC2	     192.168.10.11	255.255.255.0	  192.168.10.1
PC3      192.168.20.5   255.255.255.0   192.168.20.1
Server	 192.168.20.2   255.255.255.0	  192.168.20.1



Configuration

One of the router interface connected to one of the switchs was configured with:

interface gigabitEthernet 0/0
ip address 192.168.10.1 255.255.255.0
no shutdown

The other router interface connected to the other switch was configured with:
interface gigabitEthernet 0/1
ip address 192.168.20.1 255.255.255.0
no shutdown

The PCs and server were configured with static IPv4 addresses.

Connectivity was tested using the ping command.
PC1 → PC2
ping 192.168.10.11
PC1 → Server
ping 192.168.20.2
PC1 → Router
ping 192.168.10.1
PC3 → PC1
ping 192.168.10.10
Server → Router
ping 192.168.20.1

The tests successfully demonstrated connectivity between the devices on the local network.
What I Learned
Through this project, I practiced:

IPv4 addressing
Subnet masks
Default gateways
LAN configuration
Switch connectivity
Basic Cisco IOS commands
Connectivity testing
Future Improvements

Future versions of this lab may include:
DHCP
DNS
VLANs
Access control
Firewall configuration
Security troubleshooting

Tools
Cisco Packet Tracer
Cisco IOS CLI
Windows Command Prompt
