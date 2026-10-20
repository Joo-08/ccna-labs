# CCNA Day 7 Lab: Switch Interfaces and Router
## Objective

Use Packet Tracer to get familiar with the interfaces of the Switch and Router
## Tools Used

- Cisco Packet Tracer
- Command Prompt
- CLI

---

## Task :
 Configure the hostname of R1, SW1, and SW2

2. Configure the appropriate IP addresses on R1, PC1, PC2, PC3, PC4

3. Manually configure the speed and duplex on interfaces connected to other 
    networking devices (not end hosts)

4. Configure appropriate descriptions on each interface

5. Disable interfaces which are not connected to other devices

6. Save the configurations

### used Commands in CLI or Command Prompt 

1.hostname 'hostname' - to resolve the hostname of the devices(R1,SW1,SW2)
2.ip address 'ip-address' 'subnet-mask'
3.configure terminal - to enter into configuration mode 
4.interface 'interface-id' - to enter into the particular interface
5.speed 'speed' - to specify the speed 
6.duplex 'duplex' - to specify the duplex
7.show interface 'interface-is' - to check the status of a interface in a router
8.show interface status - to check the status of a all the interfaces in a switch 
9.description 'description' - to provide the description or an interface 
10.interface range fa0/1-24 - to configure interfaces from 1 to 24 
11.shutdown - to make the other interfaces disable 
12.write memory - to save the configurations in each device 


## Process of Configuring
1.Configure IP address to g0/0 interface 
  ->assign IP address based on the network diagram 
  ->also define the subnet maske using the command
2.Configure IP addresses on PC's
  ->Uses the IP configuration window to assign static IP address and subnet mask as per the network diagram


## Conclusion

Got to know about the interfaces of switch and routers and providing them description and configuring them 

## Tools

- Cisco Packet Tracer

## Author

Jothika D


