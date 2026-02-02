**Chapter Title:**
Chapter 24 Ethernet Media Access Controller (EMAC)

**Section Titles and Content:**

1. **24.3 MAC Interrupt Controller**
   - The MAC core can generate interrupts due to various events.
   - The interrupt register bits only indicate various interrupt events. To clear the interrupts, the corresponding status register and other registers must be read. An Interrupt Status Register describes the events that prompt the MAC core to generate interrupts. Each interrupt event can be prevented by setting the corresponding mask bit in the Interrupt Mask Register to 1. For example, if bit3 of the interrupt register is set high, it indicates that a magic packet or Wake-on-LAN frame has been received in Power-down mode. The PMT Control and Status register must be read to clear this interrupt event.

2. **24.4 MAC Address Filtering**
   - Address filtering will check the destination and source addresses of all received frames and report the address filtering status accordingly. For example, filtered frames can be identified either as multicast or broadcast.The address check, then, is based on the parameters selected by the application (Frame Filter Registers).
   - Physical (MAC) addresses are used for address checking during address filtering.

3. **24.4.1 Unicast Destination Address Filtering**
   - The MAC supports up to 8 MAC addresses for perfect filtering of unicast addresses. If a perfect filtering is selected (by resetting bit[1] in the Frame Filter Register), the MAC compares all 48 bits of the received unicast address with the programmed MAC address to determine if there is a match. By default, EMACADDRO is always enabled, and the other addresses (EMACADDDRO ~ EMACADDR7) are selected by a separate enable bit.
   - When the individual bytes of the other addresses (EMACADDDRO ~ EMACADDR7) are compared with the DA bytes received, the latter can be masked by setting the corresponding Mask Byte Control bit in the register to 1. This facilitates the DA group address filtering.

4. **24.4.2 Multicast Destination Address Filtering**
   - The MAC can be programmed to pass all multicast frames by setting the Pass All Multicast (PAM) bit in the Frame Filter Register to 1. If the PAM bit is reset, the MAC will filter multicast addresses, according to Bit[2] in the Frame Filter Register.
   - In perfect filtering mode, the multicast address is compared with the programmed MAC Destination Address Registers (EMACADDDRO ~ EMACADDR7). Group address filtering is also supported.

5. **24.4.3 Broadcast Address Filtering**
   - The MAC does not filter any broadcast frames in the default mode. However, if the MAC is programmed to reject all broadcast frames, which can happen by setting the Disable Broadcast Frames (DBF) bit in the Frame Filter Register to 1, all broadcast frames will be discarded.

6. **24.4.4 Unicast Source Address Filtering**
   - The MAC may also perform a perfect filtering based on the source address field of the received frame. By default, the Address Filtering Module (AFM) compares the Source Address (SA) field with the values

**Footer:**
Espressif Systems
Page number 467
Submit Documentation Feedback ESP32 TRM (Version 5.6)

(Note: The text in "GoBack" is not part of any section and appears to be a navigation link.)