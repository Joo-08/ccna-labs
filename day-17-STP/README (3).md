# Practice Day 17 : STP(Spanning Tree Protocol)

## Objective
To get familiar with the STP and ports in the switch while configuring the STP


## Tools used
Cisco Packet Tracer

## Task Given 
*TURN OFF LINK LIGHTS IN PACKET TRACER FOR THIS LAB*
Options > Preferences > Show Link Lights
Which switch is the root bridge?
Identify the role (root/designated/non-designated) of each switch port:
SW1 F0/1:    F0/2:    F0/3:    F0/4:

SW2 F0/1:    F0/2:    F0/3:    G0/1:

SW3 F0/1:    F0/2:    F0/3:    G0/1:

SW4 G0/1:    G0/2:

Confirm your answers in the CLI (watch the video to learn how to do this)


## Steps in Performing the task 
Step 1 : Finding the root bridge
Root Bridge : SW3
since SW3 is the root bridge 
SW3 g0/1 , f0/3 , f0/1 , f0/2 are Designated Ports 

Step 2 : Finding the root port on each switch 
process of finding the root port
1.Add up the cost to reach the root through each port. 
2.If costs tie, pick the port whose neighbor has the lowest Bridge ID.
3.If it still ties, pick the port connected to the neighbor’s lowest port ID

for SW1 : f0/4 
for SW2 : g0/1
for SW4 : g0/2
and also SW4 g0/1 is Designated port because it connects to the root port in the SW2
and also SW1 f0/3 and SW2 f0/3 are Non designated as they aredirectly connected to root bridge

Step 3 : for the remaning collision domain 
SW2 f0/1 and SW2 f0/2 are Designated because their root cost is less than the root cost for SW1's f0/1 and f0/2

Step 4 : Confirming the answers in CLI 
1.show spanning-tree : provides details about the spanning tree protocol
2.show spanning-tree vlan-number : provides details about the spanning tree protocol for a single vlan
3.show spanning-tree detail : provides a detail view about the STP in switches for each port 
4.show spanning-tree summary : provides details about the STP and the vlans 

   
## Conclusion
The root bridge along with the root ports are verified against the CLI of packet tracer and it was correct.So our configured values are correct 


## Author

Jothika D


