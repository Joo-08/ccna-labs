# CCNA Day 9 Lab: TrobleShooting Static Routing
## Objective

Use Packet Tracer to get familiar with the Troble shooting of the routers to make ping work

## Tools Used

- Cisco Packet Tracer
- Command Prompt
- CLI

---

## Task :
PC1 and PC2 are unable to ping eachother.

There is one misconfiguration on each router.

Find and fix the misconfigurations.

You have successfully completed the lab when PC1 and PC2 can ping eachother.


### used Commands in CLI or Command Prompt 
1.ip route 'ip route' 'netmask' 'next-hop' - to provide the routing details in the routing table
2.show ip interfaces brief - to check for the informations related to the interfaces of the router 
3.show ip route - to check the informations related to the routing in the routing table of the router
4.no ip route 'ip route' 'netmask' 'next-hop' - to disable the routing info configured in the routing table
5.show running config | include ip route - include configurations that has ip route in them 
6. ping 'ip-address' - to ping to the other PC


## Conclusion
PC1 was  able to sucessfully ping PC2
Got to know about troble shooting the routers and PCs involved in the ping 

## Tools

- Cisco Packet Tracer

## Author

Jothika D


