
![](image/2.png)

### AS-IS Configuration:
- Setup: Each EV charger communicates directly with the server using a single wireless network channel.   
- Issues:    
  - Unstable Communication: The reliance on a single wireless communication channel is prone to instability.
  - Responsibility Shifting: There may be issues between the EV charger manufacturers and modem companies regarding responsibility for failures.

### TO-BE Configuration:
- Setup: EV chargers are clustered using RS-485 communication and are connected to the server via both wireless and wired channels (dual communication channels).   
- Improvements:    
  - Stable Communication: The introduction of a stable wired communication channel (RS-485) significantly improves reliability.   
  - Redundancy: The dual-channel setup ensures redundancy, with wireless communication serving as a backup and wired communication as the primary.   
  - Better Diagnosis: Wired communication allows for more effective diagnostic processes for the EV chargers.   


### Summary:
- AS-IS: Each EV charger has a single, potentially unstable RF (wireless) communication channel to the server.
- TO-BE: EV chargers are grouped via RS-485 (wired communication), with dual communication channels (wireless and wired) providing more stable and reliable communication.


### introduce additional device RTU
![](image/3.png)

- The RTU acts as an intermediary device between the EVSEs and the server, improving communication reliability.
- The RS485 communication line groups multiple EVSE devices, while the Ethernet connection ensures stable data transmission to the server.

This setup supports the dual communication channel strategy discussed in the previous diagram, where the RTU and RS485 communication ensure a stable wired communication path while still allowing for potential wireless redundancy.