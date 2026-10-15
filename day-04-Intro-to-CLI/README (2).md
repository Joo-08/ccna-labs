# CCNA Day 4 Lab: Basic Device Security Commands
## Objective

Use Packet Tracer CLI to get familiar with the commands used to configure the Cisco devices

## Tools Used

- Cisco Packet Tracer
- CLI of the cisco devices

---

## Task :
1. Change the hostnames of the router and switch to the appropriate names (R1, SW1)
     ##Use the 'hostname' command in global configuration mode##

2.  Configure an unencrypted enable password of 'CCNA' on both devices

3. Exit back to user EXEC mode and test the password

4.  View the password in the running configuration

5. Ensure that the current password, and all future passwords, are encrypted

6. View the password in the running configuration

7. Configure a more secure, encrypted enable password of 'Cisco' on both devices

8. Exit back to user EXEC mode and then return to privileged EXEC mode.
    Which password do you have to use?

9. View the passwords in the running configuration.
     What encryption type number is used for the encrypted 'enable password'? Ans : 5
     What encryption type number is used for the encrypted 'enable secret'?  Ans : 7

10. Save the running configuration to the startup configuration

### used Commands in CLI 

1. enable - to enter user exec mode
2. configure terminal - to enable the password configuration
3. enable password 'password' - to configure password 
4. service password-encryption - to encrypt the password provided before MD7 encryption
5. enable secret 'newpassword' - to encrypt the password MD5 encryption
6. show running-config - to view the running-config file 
7. write memory - to save the running-config into startup-config 
8. show startup-config - to view the startup-config file 

## Conclusion

CLI made it easy to configure the details of the device using the commands  

## Tools

- Cisco Packet Tracer

## Author

Jothika D


