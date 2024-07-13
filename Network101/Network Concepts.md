
___
## Why do i need to know Linux Networking ❓
Embedded systems usually have No Displays or minimal displays so we need to connect to remote machines or connect host machines to target if we want to :
- read logs
- for debugging purposes
- configure the target machine
- upload image
## MAC Addresses
It's usually hardcoded by manufacturer on [[Network Interface Card (NIC)]], it's also used as a way to connect devices within [[Topologies used in LANs| LANs]].
![[Pasted image 20240713154612.png]]

## IP Addresses
- Internet protocol address is a numeric label assigned to a device to connect to the internet. 
- IP address can define two things the network address and host address.
- it consists of 4 octets or 32 bits.
![[Pasted image 20240713160848.png]]

## Port Number
- It's a unique id for protocols on the internet or its address of the service within the device(server).
- Port numbers allow different applications on the same computer to share network resources simultaneously.
- port numbers allow targeting of specific services or applications within those devices.
- it's a 16 bit number.

![[Pasted image 20240713163446.png]]

## Subnet
- A network inside a network.
- Its a way to organize network into smaller networks.
- They share the same upper IP address and differ in the lower part.
- The upper IP address shared among devices within subnet form a subnet mask.
- It facilitate routing.
![[Pasted image 20240713165427.png]]
## IP Address Assignation 
- can be statically assigned manually or by a script.
- or dynamically assigned using DHCP server at boot time. 
>[!NOTE]
>- you don't need DHCP server if its [[Topologies used in LANs| point to point]]. 


## How is Routing done❓
 First it checks if destination IP is within the subnet or not
 1. Within subnet
    -   will deliver the data packets by MAC Addresses.
    -  we will need to know the MAC Address that corresponds to IP  Address of destination machine using arp
1. Outside subnet
    - this will deliver the data packets to the next hop based on routing table.

## Routing Table
The routing table is a table of routes that identifies the next hop based on Destination IP address.
![[Pasted image 20240713175307.png]]
- Destination address: this refers to the IP address of the destination network.
- Subnet mask/Netmask: this refers to the class or range of the destination address. It’s used to map the destination address to the right network.
- Gateway/Next Hop: this refers to the next IP address to which the packet is forwarded.
- Interface: this refers to the outgoing interface that connects to the destination.
## ARP Protocol (Address Resolution Protocol)
it's a table that maps IP addresses to MAC addresses within the subnet.
![[Pasted image 20240713182540.png]]

## NAT protocol (Network Address Translation)
NAT hides the internal network from the rest of the network.
NAT translates private IP addresses in an internal network to a public IP address before packets are sent to an external network.
- Reduce number of registered IP
- for security to prevent internal network from external network access.
![[Pasted image 20240713194425.png]]
## DNS server
It's a server that's responsible to convert the domain name to its IP address
![[Pasted image 20240713195547.png]]

## Gateway
It's a device that connects to the network, gateway are combined with router in a single device.
## Loop-back
Loopback (also written loop-back) is the routing of electronic signals or digital data streams back to their source without intentional processing or modification or routing.
Loopback can take the form of communication channels with only one communication endpoint. Any message transmitted by such a channel is immediately and only received by that same machine
## Special IP Addresses
1. Loop-Back/Localhost: 127.0.0.1
2. Gateway: x.x.x.1
3. Broadcast: x.x.255.255 (ends with ones)