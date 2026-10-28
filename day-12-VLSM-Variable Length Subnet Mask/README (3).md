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

Step 2 : Assigning first usable addresses to the PC in each LAN
PC1 : 192.168.5.129/26

PC2 : 192.168.5.1/25

PC3 : 192.168.5.193/28

PC4 : 192.168.5.209/28

Step 3 : Assigning Last usable addresses to the Router interface in each LAN

Router 1 g0/0  : 192.168.5.190/26
Router 1 g0/1  : 192.168.5.126/25
Router 1 g0/0/0 :  192.168.5.225/30

Router 2 g0/0 : 192.168.5.206/28
Router 2 g0/1 : 192.168.5.222/28
Router 2 g0/0/0 : 192.168.5.226/30

Step 4 : Configuring Static Routes (next hop)

R1 (next hop is R2's link address 192.168.5.226)
R1(config)#ip route 192.168.5.192 255.255.255.240 192.168.5.226
R1(config)#ip route 192.168.5.208 255.255.255.240 192.168.5.226

R2 (next hop is R1's link address 192.168.5.225)
R2(config)#ip route 192.168.5.0 255.255.255.128 192.168.5.225
R2(config)#ip route 192.168.5.128 255.255.255.192 192.168.5.225

Step 4 : Ping from one network to the other 
ping from pc1 to pc3 ping 192.168.5.193
ping from pc1 to pc4 ping 192.168.5.209
ping from pc3 to pc1 ping 192.168.5.129
ping from pc3 to pc2 ping 192.168.5.1

## Conclusion
All the Pings were successfull
Got to know about the VLSM 


## Author

Jothika D


