# CCNA Day 8 Lab: Static Routing
## Objective

Use Packet Tracer to get familiar with the Static routing

## Tools Used

- Cisco Packet Tracer
- Command Prompt
- CLI

---

## Task :
All devices have NO pre-configurations:

1. Configure the PCs and routers according to the network diagram (hostnames, IP addresses, etc.)
    Remember to configure the gateway on the PCs.
    (You don't have to configure the switches)

2. Configure static routes on the routers to enable PC1 to successfully ping PC2.

### used Commands in CLI or Command Prompt 

1.hostname 'hostname' - to resolve the hostname of the devices(R1,SW1,SW2)
2.configure terminal - to enter into configuration mode 
3.interface 'interface-id' - to enter into the particular interface
4.ip address 'ip-address' 'subnet-mask' - to configure ip address in the devices 
5.no shut - to enable the connectivity of devices
6.ip route 'ip route' 'netmask' 'next-hop' - to provide the routing details in the routing table
7.show ip interfaces brief - to check for the informations related to the interfaces of the router 
8.show ip route - to check the informations related to the routing in the routing table of the router
9.ping 'ip-address' - to ping to the other PC

## Process of Configuring
1.Configure IP address to g0/0 interface 
  ->assign IP address based on the network diagram 
  ->also define the subnet maske using the command
2.Configure IP addresses on PC's
  ->Uses the IP configuration window to assign static IP address and subnet mask as per the network diagram


## Conclusion
PC1 was  able to sucessfully ping PC2
Got to know about configuring of ip addresses in Devices and static routes in routers

## Tools

- Cisco Packet Tracer

## Author

Jothika D


