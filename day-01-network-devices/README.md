# CCNA Day 01 Activity: Two-Branch Network with ASA Firewalls

A Cisco Packet Tracer lab that connects a **New York branch** and a **Tokyo branch** across a simulated Internet, with an ASA 5505 firewall protecting each site.


## LAB INSTRUCTIONS:

Create the network diagram displayed at 16:40 of the Day 1 video.

Use the following devices:

Cisco 2911 routers (x2)

Cisco 2960 switches (x2)

Cisco 5505 Firewalls (x2)

PCs (x2)

Servers (x2)

Use a Laptop as the ‘attacker’ in the diagram.

## Objectives

- Build the two-branch topology in Packet Tracer
- Use the correct cable type for each connection
- Bring up all interfaces so every link shows green
- Assign IP addressing to all devices
- Verify connectivity between the New York and Tokyo branches

## Setup Steps

1. Place all devices and connect them as shown in the topology.
2. Enable each router interface:
   ```
   Router> enable
   Router# configure terminal
   Router(config)# interface gig0/0
   Router(config-if)# no shutdown
   ```
3. Repeat `no shutdown` for every connected interface on Router0, The Internet, and Router1.

## Verification

```
show ip interface brief
```


## Troubleshooting

**Red triangle (link down):**

| Cause | Fix |
|---|---|
| Interface administratively down | Run `no shutdown` on the interface |
| Wrong cable type | Use straight-through for unlike devices, cross-over for like devices |
| Wrong ASA port | Check ports with `show interface ip brief` |
| Switch still converging | Wait 30 to 50 seconds for the port to turn green |

## Tools

- Cisco Packet Tracer

## Author

Jothika D

