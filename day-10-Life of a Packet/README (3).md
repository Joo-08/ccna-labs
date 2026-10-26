# CCNA Day 10 Lab: Life of a Packet 
## Objective

Use Packet Tracer to get familiar with the Troble shooting of the routers to make ping work

## Tools Used

- Cisco Packet Tracer
- Command Prompt
- CLI

---

### used Commands in CLI or Command Prompt 
1.ipconfig /all - to get the mac address of the PC1
2.ping - to ping the PC4
3.show interface interface-id - to get the MAC address of the specific interface in a router

## Task 1 :
1. PC1 pings PC4.  
Identify the src/dst MAC address at each specified point in the route to PC4.
Identify the MAC address by the device and interface (ie. the MAC of R1 G0/0)
A. Source/Destination MAC at PC1 → SW1 segment
B. Source/Destination MAC at SW1 → R1 segment
C. Source/Destination MAC at R1 → R2 segment
D. Source/Destination MAC at R2 → R3 segment
E. Source/Destination MAC at R3 → SW2 segment
F. Source/Destination MAC at SW2 → PC4 segment

Use the CLI and Packet Tracer's simulation mode to verify your answers.
(Before you enter simulation mode, ping once to complete ARP/the MAC learning process.)

## Solution 
A. Source - 00D0.BA11.1111 Destination - 0000.01AA.AAAA
B. Source - 00D0.BA11.1111 Destination - 0000.01AA.AAAA
C. Source - 0000.01BB.BBBB Destination - 0000.01CC.CCCC
D. Source - 0000.01DD.DDDD Destination - 0000.01EE.EEEE
E. Source - 0000.01EF.FFFF Destination - 000C.8544.4444
F. Source - 0000.01EF.FFFF Destination - 000C.8544.4444

## Task 2 :
2. PC1 pings PC3.
Identify the src/dst MAC address at each specified point in the route to PC3.
Identify the MAC address by the device and interface (ie. the MAC of R1 G0/0)
A. Source/Destination MAC at PC1 → SW1
B. Source/Destination MAC at SW1 → PC3

Use the CLI and Packet Tracer's simulation mode to verify your answers.
(Before you enter simulation mode, ping once to complete ARP/the MAC learning process.)

## Solution
A. Source - 0D00.BA11.1111(PC1) Destination - 0010.1133.3333(PC3)
B. Source - 0D00.BA11.1111(PC1) Destination - 0010.1133.3333(PC#)


## Conclusion
Got to know about the life cycle of the packet during ping 



## Tools

- Cisco Packet Tracer

## Author

Jothika D


