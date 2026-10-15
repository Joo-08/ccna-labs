# CCNA Day 5 Lab: Ethernet LAN switches, ARP , ICMP flow of messages 

## Objective

Use Packet Tracer to get familiar with the etherent LAN switching including the arp and mac addresses

## Tools Used

- Cisco Packet Tracer
- Command Prompt

---

## Task :
Both switches have an empty MAC address table, and all PCs have an empty ARP table.

1. If PC1 pings to PC3, what messages will be sent over the network,and which devices will receive them?

2. Send the ping and use Packet Tracer's 'simulation mode' to verify your answer.

3. Use pings to generate network traffic and allow the switches to learn the MAC addresses 
     of all PCs on the network.

4. Use 'show' commands on the switches to identify the MAC address of each PC.

5. Clear the dynamic MAC addresses from the MAC address table of each switch.

## Answer
1. If PC1 pings to PC3, what messages will be sent over the network,and which devices will receive them?
ARP Request (received by PC2, PC3, PC4)
ARP Reply (received by PC1)
ICMP Echo Request (received by PC3)
ICMP Echo Reply (received by PC1)

### used Commands in Command Prompt 

1. enable - to enter user exec mode
2. ping 'ip_address_of_the_PC' - to ping one PC from another PC
3. show mac address-table - to view the mac address table in a switch
4. clear mac address-table dynamic - to clear the dynamic mac addresses from the switch 

## Conclusion

Got to know an dunderstand the Ethernet lan switching and how arp and icmp works 

## Tools

- Cisco Packet Tracer

## Author

Jothika D


