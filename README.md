This project simulates a small office network created using Cisco Packet Tracer.

The main objective was to practice basic networking concepts, including IPv4 addressing, subnet masks, default gateways, switch connectivity, router configuration and network segmentation
# Network Topology 

The network consists of:

1 Router

2 Switch

3 PCs

1 Server

<img width="1920" height="1032" alt="Image" src="https://github.com/user-attachments/assets/a0af6a07-e666-44b9-8f99-845e8b21778e" />" 

# Network addresses:

Switch 1 : 192.168.10.0 /24 - router interface 192.168.10.1

Switch 2 : 192.168.20.0 /24 - router interface 192.168.20.1



## IP Addressing

### Device|     	 IPv4 Address	  |      Subnet Mask  	|     Default Gateway

#### Router|	 192.168.10.1	 | 255.255.255.0  |            	—

#### Router|	 192.168.20.1	 | 255.255.255.0  |            	—

#### PC1	  |   192.168.10.10 | 255.255.255.0 | 	192.168.10.1

#### PC2	  |  192.168.10.11 |	255.255.255.0	|  192.168.10.1

#### PC3   |   192.168.20.5  | 255.255.255.0 |  192.168.20.1

#### Server	 192.168.20.2  | 255.255.255.0	 | 192.168.20.1



## Configuration

The router interface that was connected to the switch 1 was configured with:

interface gigabitEthernet 0/0

ip address 192.168.10.1 255.255.255.0

no shutdown

The router interface connected to the switch 2 was configured with:

interface gigabitEthernet 0/1

ip address 192.168.20.1 255.255.255.0

no shutdown

The PCs and server were configured with static IPv4 addresses.

## Connectivity was tested using the ping command.

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

#### The tests successfully demonstrated connectivity between the devices on the local network.
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

## Future versions of this lab may include:

DHCP

DNS

VLANs

Access control

Firewall configuration

Security troubleshooting

## Tools

Cisco Packet Tracer

Cisco IOS CLI

Windows Command Prompt




# screenshots/

##### pc1-ip-config

<img width="1000" height="520" alt="Image" src="https://github.com/user-attachments/assets/1109a3cd-159b-4a60-8980-6b763dc7a865" />

#### router-interface-config

<img width="1920" height="1032" alt="Image" src="https://github.com/user-attachments/assets/b272a922-5d2c-43dc-bde6-cfb1ce298a59" />

#### server-ping-router 

<img width="1920" height="1032" alt="Image" src="https://github.com/user-attachments/assets/5fc7caa4-3a7a-4622-8bfc-13713714ab03" />
