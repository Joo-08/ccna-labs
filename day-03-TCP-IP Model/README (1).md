# CCNA Day 3 Lab: Packet Tracer Simulation Mode and OSI Layers

## Objective

Use Packet Tracer's **Simulation mode** to analyze network traffic and identify which OSI model layers are used by each device. Then generate Layer 7 (Application) traffic by releasing and renewing PC1's IP address through DHCP.

## Tools Used

- Cisco Packet Tracer
- Simulation mode

---

## Task 1 : Analyze Traffic with Simulation Mode

### Steps

1. Switch from **Realtime** to **Simulation** mode (bottom-right corner).
2. Press **Capture / Forward** to step through each event.




## Task 2: Release and Renew PC1's IP Address (Layer 7 Traffic)

### Steps

1. Stay in **Simulation mode**.
2. Open **PC1 → Desktop → Command Prompt**.
3. Run:
   ```
   ipconfig /release
   ipconfig /renew
   ```
4. Return to the main window and press **Capture / Forward** repeatedly.
5. Click each DHCP packet and review the **OSI Model** tab.

---

## Conclusion

Simulation mode shows how data moves through the network and which OSI layers each device handles. 

## Tools

- Cisco Packet Tracer

## Author

Jothika D
