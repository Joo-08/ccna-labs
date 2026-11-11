# Practice Day 16 : DTP(Dynamic Trunking Protocol) VTP(VLAN Trunking Protocol)

## Objective
To get Familiar with the DTP and VTP


## Tools used
Cisco Packet Tracer

## Task Given 
1. Configure the switchports connecting switches as trunk ports.
    Disable DTP on the ports.
    Confirm the administrative and operational mode of each interface.
2. Configure SW1 in VTP domain CCNA.
    Create VLANs 10, 20, and 30 on SW1.
    Have SW2 and SW3 added VLANs 10, 20, and 30?
3. Configure SW2 in VTP transparent mode.
    Add VLAN40 to SW2.
    Is VLAN40 added to the VLAN database of SW1/SW3?
4. Configure SW3 in VTP client mode.
    Try to configure VLAN50 on SW3.  Is it added?
5. Configure all switchports connected to hosts in the correct VLAN.
    Manually configure them as access ports.
    Is DTP still enabled on the switchports?


## Steps in Performing the task 
Step 1 : 1. Configure the switchports connecting switches as trunk ports.Disable DTP on the ports.Confirm the administrative and operational mode of each interface.
The trunk ports are 
So the trunk ports are:
SW1: G0/1
SW2: G0/1 and G0/2
SW3: G0/1
Since the ports are in negotiate mode let us configure them in trunk mode using the following commands 
1.enable : to enter into the user prev mode 
2. configure terminal : to be able to make changes in the interfaces 
3.interface g0/0 : configure the g0/0 interface 
4.switchport mode trunk : to change the mode to trunk 
5.switchport nonnegotiate - to turnoff negotiation (Disables the DTP)
6.show interface g0/1 switchport : To Confirm administrative and operational mode

Step 2 : Configure SW1 in VTP domain CCNA.Create VLANs 10, 20, and 30 on SW1. Have SW2 and SW3 added VLANs 10, 20, and 30?
In SW1
1.vtp mode server - to switch to mode vtp server
2.vtp domain CCNA - to assign domain name 
3.vtp version 2 - to assign version to the vtp from version 1,2,3
4.vlan 10 - creating vlan 
5.name VLAN10 - naming the vlan as VLAN 10 
In SW2 and SW3
1.vtp mode client - to switch to mode vtp client so that they can learn from the server 
2.vtp domain CCNA - to assign domain name 
3.vtp version 2 - to assign version to the vtp from version 1,2,3

1.show vtp status - to check the vtp details in the switch 

# Answer : Yes SW2 and SW3 has VLAN 10,20 and 30 due to the vtp 

Step 3 : Configure SW2 in VTP transparent mode.Add VLAN40 to SW2.Is VLAN40 added to the VLAN database of SW1/SW3?
1.vtp mode transparent - to switch to transparent mode
2.vlan 40 - to create a new vlan
3.name VLAN40 -to name the vlan as VLAN40 
4.show vtp status - to check the vtp status in the switch
5.show vlan brief - to check the vlans in a switch 

# Answer : SW2 and SW3 does not have the VLAN40 because in tranparent mode the switch does not advertise its own VLAN with other switches

Step 4 : Configure SW3 in VTP client mode.Try to configure VLAN50 on SW3.  Is it added?
1.vtp mode client - to switch to client mode
2.vlan 50 - to create a new vlan
3.name VLAN50 -to name the vlan as VLAN50 
4.show vtp status - to check the vtp status in the switch
5.show vlan brief - to check the vlans in a switch 

VTP VLAN configuration not allowed when device is in CLIENT mode.
# Answer vtp client cannot add vlan so the vlan 50 is not added

Step 5 : Configure all switchports connected to hosts in the correct VLAN. Manually configure them as access ports. Is DTP still enabled on the switchports?
In SW1
enable
configure terminal
interface range f0/1 - 2
 switchport mode access
 switchport access vlan 10
interface f0/3
 switchport mode access
 switchport access vlan 20
end
In SW2
enable
configure terminal
interface range f0/1 - 2
 switchport mode access
 switchport access vlan 40
end
In SW3
enable
configure terminal
interface range f0/1 - 3
 switchport mode access
 switchport access vlan 30
interface f0/4
 switchport mode access
 switchport access vlan 20
end

show vlan brief - verify the vlans and the ports in the switch
show interfaces f0/1 switchport - to check the layer 2 settings for the particular port 

# Answer No Setting a port to switchport mode access turns DTP off on that port
   
## Conclusion
All the Pings were successfull
The PCs were able to communicate with the eachother in other vlans too and to the internet


## Author

Jothika D


