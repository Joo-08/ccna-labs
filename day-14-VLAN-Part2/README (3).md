# Practice Day 14 : VLAN Part 2

## Objective
To assign trunk ports and test the connectivity using ping


## Tools used
Cisco Packet Tracer

## Task Given 
1. Configure the switch interfaces connected to PCs as access ports in the correct VLAN.

2. Configure the connection between SW1 and SW2 as a trunk, allowing only the necessary VLANs.
    Configure an unused VLAN as the native VLAN.
    **Make sure all necessary VLANs exist on each switch**

3. Configure the connection between SW2 and R1 using 'router on a stick'.
     Assign the last usable address of each subnet to R1's subinterfaces.

4. Test connectivity by pinging between PCs.  All PCs should be able to reach each other.


## Steps in Performing the task 
Step : 1 Configuring the switch interfaces connected to PCs as access ports in the correct VLAN.
Commands used in configuring
1.enable: Moves you from user EXEC mode into privileged EXEC mode 
2.interface range ‘range’: Selects multiple ports at once 
3.switchport mode access: Sets the selected ports as access ports, which carry traffic for a single VLAN and connect to end devices like PCs.
4.switchport access vlan ‘vlanid’: Assigns the selected access ports to the specified VLAN ID 
5.show vlan brief: Displays a summary of all VLANs, their names, and which ports belong to each.
6.name ‘vlanname’: Gives a descriptive name to a VLAN (used inside VLAN configuration mode, e.g., after vlan 10).

Step 2 Configuring the connection between SW1 and SW2 as a trunk, allowing only the necessary VLANs. Configuring an unused VLAN as the native VLAN.
Commands used in configuring 
1.interface ‘interface-id’: Selects a single port 
2.switchport mode trunk: Sets the port as a trunk, which carries traffic for multiple VLANs between switches (or to routers) using 802.1Q tagging.
3.switchport trunk allowed vlan ‘vlans’: Restricts which VLANs may cross the trunk (e.g., 10,20,30)
4.switchport trunk native vlan ‘nativevlan’: Sets the VLAN whose traffic travels untagged on the trunk (default is VLAN 1), and it must match on both ends of the link.
5.show interfaces trunk: Displays all active trunk ports along with their mode, encapsulation (802.1Q), status, native VLAN, and the allowed and active VLANs on each.

Step 3 Configuring the connection between SW2 and R1 using 'router on a stick'. Assign the last usable address of each subnet to R1's subinterfaces.
1.enable: Moves from user EXEC mode into privileged EXEC mode.
2.configure terminal: Enters global configuration mode to change the router’s settings.
3.interface g0/0: Selects the physical interface connected to SW2 (it gets no IP address).
4.no shutdown: Turns the selected interface on, since router interfaces are shut down by default.
5.exit: Leaves interface configuration mode and returns to global configuration mode.
6.interface g0/0.10: Creates a logical subinterface on g0/0 for VLAN 10.
7.encapsulation dot1q 10: Makes the subinterface handle 802.1Q tagged frames for VLAN 10 (enter this before the IP address).
8.ip address 'ipaddress' 'subnetmask': Assigns the VLAN’s gateway IP address to the subinterface.

Step 4 : Test connectivity by pinging between PCs.  All PCs should be able to reach each other.
1.ping 'pcaddres' : to test the connectivity by sepcifying the ip address


## Conclusion
All the Pings were successfull
The PCs were able to communicate with the eachother in other vlans too


## Author

Jothika D


