# Practice Day 17 : STP(Spanning Tree Protocol) Part 2 

## Objective
To get familiar with the STP process and CLI configurations of STP process


## Tools used
Cisco Packet Tracer

## Task Given 
1. Use the CLI to check the current STP topology.  What is the current root bridge?
    What is the STP role/state of each port on each switch?

2. Configure SW1 as the primary root for VLAN1 and the secondary root for VLAN2.
    Configure SW2 and the primary root for VLAN2 and the secondary root for VLAN1.
    What is the STP role/state of each port on each switch now?

3. Increase the VLAN1 cost of SW4's F0/2 interface to 100.
    Does SW4 select a different root port?  Why/why not?

4. Increase the VLAN1 port priority of SW1's F0/1 to 240.
    Does SW3 select a different root port?  Why/why not?

5. Configure PortFast and BPDU Guard on the F0/3 interfaces of SW3/SW4.
 


## Steps in Performing the task 
Step 1 : 
1.show spanning-tree - shows the information about the SPT for each vlan seperately 
The output of this command shows the root bridge details and the STP role/state of each port in the switch

Step 2 :
1.spanning-tree vlan 'vlan-number' root primary - to make the switch as primary root bridge for the particular vlan 
2.spanning-tree vlan 'vlan-number' root secondary - to make the switch as secondary root bridge for the particular vlan 
3.show spanning-tree - to verify the details after assigning the root bridges manually 
Since we changed the root bridge for vlans each vlan in the same switch may have diff status to ports now 

Step 3 :
1.show spanning-tree vlan 1 - to view info about the spanning tree for a particular vlan 
In SW4 f0/2 is the root port
2.int f0/2 - to enter into the interface 
3.span vlan 1 cost 100 - increasing the cost to 100 
After changing the cost the f0/2 port has become blocking and f0/1 has become the root port 

Step 4 :
1.do show spanning-tree vlan 1 -  to view info about the spanning tree for a particular vlan 
f0/1 is the root port 
2.interface f0/1 in SW1 
3.span vlan 1 port priority 240 - to change the port-priority 
After changing the priority though it will not affect the SW3's root port selection because the sender port id is the last tie breaker 
so SW3 doesnot have a diff root port

Step 5 :
1.interface f0/3 - to enter into the interface
2.spanning-tree portfast - to enable portfast in switch
3.spanning-tree bpduguard enable - to enable bpdu guard in a switch
After enabling the bpduguard if the switch interface it connected to other switch by mistake it shutdowns the entire interface and if again you connect it 
to the PC it will remain in the shutdown state until you provide a ni shutdown command 


   
## Conclusion
Got a overview about the CLI details that is represented in switches for the STP



## Author

Jothika D


