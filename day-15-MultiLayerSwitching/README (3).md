# Practice Day 15 : MultiLayerSwitching

## Objective
To configure the multilayer switching


## Tools used
Cisco Packet Tracer

## Task Given 
All devices are preconfigured from the end of Day 17's lab (SW2 has been replaced with a multilayer switch):
Hosts are in the correct VLANs.
SW1-SW2 are connected via trunk.
R1-SW2 are connected via ROAS.
1. Replace the ROAS configuration on R1-SW2 with a point-to-point Layer 3 connection.
    Use the IP addresses given in the network diagram.
    Configure a default route on SW2, with R1's G0/0 interface as the next hop.
2. Configure SVIs on SW2, one for each VLAN.
     Assign the last usable IP address of each subnet to the appropriate SVI.
3. Test inter-VLAN connectivity by pinging between VLANs.
4. Test connectivity to the Internet by pinging 1.1.1.1
    (Routes have already been configured on R1 and the Internet router)


## Steps in Performing the task 
Step : 1 Replacing the ROAS configuration on R1-SW2 
In Router 
1.no interface g0/0.10 ,no interface g0/0.20, no interface g0/0.30 - to remove the subinterfaces we created before
2.default interface g0/0 - to make it a default interface g0/0
3.show ip interface brief - to get a overview of the interfaces in the router
Providing IP address for the router 
1.interface g0/0 - to configure the interface 
2.ip address 'ipaddress' 'subnetmask' - to configure the address to the router's interface
configuring Default route on the Switch 2
Configuring Default gateway 
1.ip route 0.0.0.0 0.0.0.0 'nexthop-ipaddress' - to configure the nexthop for forwarding the traffic 

Step : 2 Configuring SVIs on SW2, one for each VLAN.
1.default interface g1/0/2 - to make it a default interface g1/0/2
2.ip routing - This enables the Layer 3 routing on the switch 
3.interface g1/0/2 - to access the interface g1/0/2
4.no switchport - This configures the interface as a router port 
5.show ip interface brief - to get a overview of the interfaces in the Switch
6.ip address 'ipaddress' 'subnetmask' - to configure the address to the router's interface
7.no shut - to make the interface active 
Configuring SVIs on the Switch interface 
1.interface vlan 10 - create a VLAN 
2.ip address 'last usable address' 'subnetmask' -to assign the address to the vlan
3.no shut - to make the interface to active status

Step 3 : Pinging the other Devices in the vlan and to the internet
1.ping 'ip address' - to check the reachablity of the other devices 
2.ping 1.1.1.1 - to check the connectivity to the internet


## Conclusion
All the Pings were successfull
The PCs were able to communicate with the eachother in other vlans too and to the internet


## Author

Jothika D


