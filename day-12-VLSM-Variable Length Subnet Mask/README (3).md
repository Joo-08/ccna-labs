# Practice Day 12 : VLSM Variable Length Subnet Masks

## Objective
To solve the given task in the packet tracer

## Tools used
Cisco Packet Tracer

## Task Given 
(network diagram is attached in the screenshot)
Subnet the 192.168.5.0/24 network to provide sufficient addressing for each LAN.
(Also, the point-to-point connection between R1 and R2).

Assign the first usable address to the PC in each LAN.

Assign the last usable address to the router's interface in each LAN.

Configure static routes on each router so that all PCs can ping eachother.

## Performing the task 
Step 1 : Dividing the Network(192.168.5.0/24) into four subnets 
According to the steps of the VLSM we should first solve network with maximum hosts so 
->LAN 2
192.168.5.0/24 and 64 Hosts
  1.Network Address : 192.168.5.0/25
  2.Broadcast Address :192.168.5.127/25
  3.First usable Address : 192.168.5.1/25
  4.Last usable Address : 192.168.5.126/25
  5.Number of Hosts : 128-2 = 126
->LAN 1
192.168.5.128 and 45 Hosts
  1.Network Address : 192.168.5.128/26
  2.Broadcast Address :192.168.5.191/26

  3.First usable Address : 192.168.5.129/26
  
  4.Last usable Address : 192.168.5.190/26
  5.Number of Hosts : 64-2 = 62
->LAN 3
192.168.5.192 and 14 Hosts
  1.Network Address : 192.168.5.192/28
  2.Broadcast Address :192.168.5.207/28
  3.First usable Address : 192.168.5.193/28
  4.Last usable Address : 192.168.5.206/28
  5.Number of Hosts : 16-2 = 14
->LAN 4
192.168.5.208 and 9 Hosts
  1.Network Address : 192.168.5.208/28
  2.Broadcast Address :192.168.5.223/28
  3.First usable Address : 192.168.5.209/28
  4.Last usable Address : 192.168.5.222/28
  5.Number of Hosts : 16-2 = 14
->Point to Point from R1 to R2 
192.168.5.224 and 2 hosts
1.Network Address : 192.168.5.224/30
  2.Broadcast Address :192.168.5.227/30
  3.First usable Address : 192.168.5.225/30
  4.Last usable Address : 192.168.5.226/30
  5.Number of Hosts : 4-2 = 2







## Conclusion
Got to know about the Class B Subnetting


## Author

Jothika D


