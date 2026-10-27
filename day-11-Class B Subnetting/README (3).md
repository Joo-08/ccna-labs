# Practice Day 11 : Class B Subnetting

## Objective
To solve the given questions in the day 11 video

## Question 1
You have been given the 172.30.0.0/16 network. Your company requires 100 subnets with at least 500 hosts per subnet. What prefix length should you use?
Soln: gn 172.30.0.0/16
if we borrow 1 bit - 2 subnetworks(/17) .......
if we boorow 6 bits - 64 subnetworks(/22)
if we borrow 7 bits - 128 subnets(/23)
for /23 prefix length the number of hosts are = 2ⁿ − 2
n = number of hosts per subnet 
n = 9 (since 23 are network bit 32-23=9)
the number of host = 512-2 = 510 (this satisfies the 500 hosts)

Ans : for 100 subnets the prefix length is /23

## Question 2
Which Subnet does the host 172.21.111.201/20 belong to 
Soln : gn 172.21.111.201
in binary it is represented as 
   172      21       111        201    /20
10101100.00010101.0110 | 1111.11001001

10101100.00010101.0110 | 0000.00000000
172        21         96          0

Ans : 172.21.96.0

## Question 3
What is the broadcast address of the network 192.168.91.78/26 belongs to?
Soln : gn 192.168.91.78/26
in binary it is represented as 
   192      168      91       78          /26
11000000.10101000.01011011.01 | 001110

11000000.10101000.01011011.01 | 111111   /26
  192       168      91      127 

Ans : 192.168.91.127

## Question 4
You divide the 172.16.0.0/16 network into 4 subnets of equal size. Identify the network and broadcast addresses of the second subnet.
Soln : gn 172.16.0.0/16
to get 4 subnets we have to borrow 2 bits so the network becomes 172.16.0.0/18
  172        16         0        0 
10101100.00010000.00 | 000000.00000000. the subnet mask is 255.255.192.0 

The First Subnet is 172.16.0.0
The Second Subnet is  172.16.64.0
The Third Subnet is  172.16.128.0
The Fourth Subnet is  172.16.192.0

The Network address of Subnet 2 is 172.16.64.0
The Broadcast address of Subnet 2 is 172.16.127.255

## Question 5
You divide the 172.30.0.0/16 network into subnets of 1000 hosts each. How many subnets are you able to make?
Soln : gn 172.30.0.0/16
if we borrow 1 bit - 2 subnetworks(/17) no of hosts : 32,766 ....
if we borrow 6 bits - 64 subnetwroks(/22) no of hosts : 1,022

So from this we can make 64 subnets each with 1022 hosts.

Ans : 64 Subnets

## Conclusion
Got to know about the Class B Subnetting


## Author

Jothika D


