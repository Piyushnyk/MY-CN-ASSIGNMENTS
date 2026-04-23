Objective: To configure a basic enterprise network in Cisco Packet Tracer with two routers, two LANs, centralized DHCP server, and RIPv2 routing.

Topology:

2 Routers connected with a serial WAN link
2 Switches (one per LAN)
2 PCs on each LAN
1 DHCP Server located in LAN1
IP Addressing:

LAN1 Network: 192.168.1.0/24

Router1 G0/0: 192.168.1.1
DHCP Server: 192.168.1.2
PCs: DHCP
LAN2 Network: 192.168.2.0/24

Router2 G0/0: 192.168.2.1
PCs: DHCP
WAN Network: 10.0.0.0/8

Router1 S0/0/0: 10.0.0.1
Router2 S0/0/0: 10.0.0.2
Configuration Steps:

Built the topology with routers, switches, PCs, and server.
Connected LAN devices using straight-through cables.
Connected routers using serial DCE cable.
Configured IP addresses on router interfaces.
Enabled all interfaces using "no shutdown".
Configured RIPv2 on both routers:
version 2
no auto-summary
added respective network statements.
Configured DHCP server with two pools:
LAN1 pool (192.168.1.0/24)
LAN2 pool (192.168.2.0/24)
Configured DHCP relay on Router2 using: ip helper-address 192.168.1.2
Set all PCs to obtain IP address automatically (DHCP).
Verified routing using "show ip route".
Verified connectivity using ping from LAN1 PC to LAN2 PC.
Verification: Successful ping from a PC in LAN1 to a PC in LAN2 confirmed end-to-end connectivity.
