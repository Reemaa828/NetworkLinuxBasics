# What's `nmcli`❓
**nmcli** is the NetworkManager command-line interface. This is a very commonly used command line tool for analyzing, modifying, and troubleshooting network connections.

# Important Usage

## `nmcli con show`
![[Pasted image 20240714202539.png]]
## - `nmcli con modify <device> ip.method manual|auto ip.address <ip address> ip.gateway <gateway ip address> ` to modify NetworkManger device
## - `nmcli con down <device>` to disconnect device
## - `nmcli con up <device>` to connect device
## - `nmcli connection edit "Wired connection 1"` to use interactive shell to modify device