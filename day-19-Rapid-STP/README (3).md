# Practice Day 19 : Rapid STP(Spanning Tree Protocol) 

## Objective
To get familiar with the Rapid STP process and CLI configurations of Rapid STP process


## Tools used
Cisco Packet Tracer

## Task Given 
1. Which switch is the root bridge?
    Use the CLI to examine the port role/state of each interface on the root.
    What appears different than what you have learned about the root bridge?
    What is the cause of this?

2. Without using the CLI, determine the port role/state of each remaining switch interface.
    Use the CLI to confirm.

3. Manually configure the appropriate RSTP link type on each interface.
    What do you think is the correct link type for SW1's F0/24?

 


## Steps in Performing the task 
Step 1 :
1.By analyzing the network diagram it is clear that SW1 is the root bridge(since SW1 has lowest bridge ID)
2.To ensure it run show spanning-tree in the SW1 
3.The details in the root ID and bridge ID are same which means SW1 is indeed the root bridge 
4.The role/status of each interface has to be designated since it is connected to the root bridge 
5.But in the CLI the fa 0/3 interface is represented as blocking and non designated port 
6.Because fa 0/3 interface acts as a  backup port because it receives superior BPDU from another interface on the same switch

Step 2 :
Switch	Interface	Role	          State	
SW1     (Root)	    F0/1	          Designated	
	    F0/2	    Designated	      Forwarding	
	    F0/3	    Backup	          Discarding	
	    F0/24	    Designated	      Forwarding	
SW2	    F0/1	    Root	          Forwarding	
	    G0/1	    Alternate	      Discarding	
	    F0/2	    Designated	      Forwarding	
	    F0/23	    Designated	      Forwarding	
	    F0/24	    Designated	      Forwarding	
SW3	    F0/2	    Root	          Forwarding	
	    G0/1	    Designated	      Forwarding	
	    F0/1	    Designated	      Forwarding	
	    F0/24	    Designated	      Forwarding	
SW4	    F0/1	    Root	          Forwarding	
	    F0/2	    Alternate	      Discarding
	    F0/24	    Designated	      Forwarding	

Step 3 :
1.spanning-tree link-type 'linktype'
    Full duplex is point-to-point and half duplex is shared.
    1.point to point 
    2.edge
    3.shared
2.using the above command the link types can be defined 
3.the correct link type for SW1's F0/24 is shared because it is connected to the hub 



   
## Conclusion
Got a overview about the CLI details that is represented in switches for the Rapid STP



## Author

Jothika D


