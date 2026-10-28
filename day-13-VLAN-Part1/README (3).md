# Practice Day 13 : VLAN Part 1

## Objective
To assign VLANs in the given netwrok

## Tools used
Cisco Packet Tracer

## Task Given 
1. Configure the correct IP address/subnet mask on each PC.
    Set the gateway address as the LAST USABLE address of the subnet.
2. Make three connections between R1 and SW1.
    Configure one interface on R1 for each VLAN.
    Make sure the IP addresses are the gateway address you configured on the PCs.
3. Configure SW1's interfaces in the proper VLANs.
    Remember the interfaces that connect to R1!
    Name the VLANs
     (Engeering, HR, Sales)
4. Ping between the PCs to check connectivity.
    Send a broadcast ping from a PC (ping the subnet broadcast address), and see which PCs devices receive the broadcast (use Packet Tracer's 'Simulation Mode')

## Performing the task 
Step : 1
PC1 
IP address : 10.0.0.1/26
Subnet mask : 255.255.255.192
Last Usable address : 10.0.0.62

PC2
IP address : 10.0.0.2/26
Subnet mask : 255.255.255.192
Last Usable address : 10.0.0.62

PC3
IP address : 10.0.0.65/26
Subnet mask : 255.255.255.192
Last Usable address : 10.0.0.126

PC4
IP address : 10.0.0.66/26
Subnet mask : 255.255.255.192
Last Usable address : 10.0.0.126

PC5
IP address : 10.0.0.129/26
Subnet mask : 255.255.255.192
Last Usable address : 10.0.0.190

PC6
IP address : 10.0.0.130/26
Subnet mask : 255.255.255.192
Last Usable address : 10.0.0.190

Step 2 : 
Cabling: three straight-through cables from R1 (G0/0, G0/1, G0/2) to SW1 (G0/1, G1/1, G2/
Providing IP address for the interfaces 
Router g0/0 : ip address 10.0.0.62 255.255.255.192
Router g0/1 : ip address 10.0.0.126 255.255.255.192
Router g0/2 : ip address 10.0.0.190 255.255.255.192

Step 3 : 
Configuring the VLANs
interface range f3/1, f4/1, g0/1
switchport mode access
switchport access vlan 10
exit
same way for all the interfaces

Step 4 : 
Pinging from the PCs
ping 10.0.0.129 from PC1

Step 5 :
Checked the packet flow in the Simulation mode


## Conclusion
All the Pings were successfull
The Broadcast packets were delivered only inside the vlan and not between the vlans this provides more efficiency and security in the networks


## Author

Jothika D


