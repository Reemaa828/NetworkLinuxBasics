# What info can be extracted from `ip`❓
to show details about all Network Interfaces including down networks.
- **Interface Details:**
    - Name (e.g., eth0, wlan0)
    - Link type (Ethernet, Wi-Fi)
    - MAC address
    - IP address
    - Subnet mask
    - Interface flags (UP, RUNNING, etc.)
- **Link Management:**
    - Bring interface up/down
    - Set MAC address
    - Manage link speed and duplex mode
- **Route Management:**
    - View and manipulate routing tables
    - Add, delete, or modify routes
- **Address Management:**
    - Assign and manage IP addresses (static or DHCP)


# Important Usages
## `ip a` to show Interfaces
![[Pasted image 20240714052753.png]]

## `ip a add <ip address> dev <interface>` to assign ip address to a specific Interface
![[Pasted image 20240714055531.png]]
## - `ip a del <ip address> dev <interface>` to delete assigned ip address to a specific Interface

## `ip route` to display routing table
![[Pasted image 20240714055749.png]]

## - `ip link set <inteface> up|down` to connect/disconnect

## `ip monitor` Monitor and display the state of devices, addresses, and routes continuously.
![[Pasted image 20240714063220.png]]

## - `ip route add <ip address> via <gateway> dev <interface` to add a route to route table


## - `ip link set <ip address> mtu 1500` to set maximum transmission unit