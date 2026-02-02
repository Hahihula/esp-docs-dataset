**Chapter Title:**
Chapter 24 Ethernet Media Access Controller (EMAC)

**Section Header:**
Register 24.19. EMACFC_REG (0x1018)

**Field Description and Values Table:**
- PAUSE_TIME [reserved]
- PLT, UPFD, RFCE, TFCE

**Text Content with Descriptions of Fields in the Register:**

**PAUSE_TIME**
This field holds the value to be used in the Pause Time field in the transmit control frame. If the Pause Time bits is configured to be double-synchronized to the MII clock domain, then consecutive writes to this register should be performed only after at least four clock cycles in the destination clock domain.

**PLT (Pause Timer)**
This field configures the threshold of the Pause timer automatic retransmission of the Pause frame. The threshold values should always less than the Pause Time configured in Bits[31:16]. For example, if PT = 100H (256 slot-times), and PLT = 01, then a second Pause frame is automatically transmitted at 228 (256-28) slot times after the first Pause frame is transmitted. The following list provides the threshold values for different values: (R/W)

- **2'b00:** The threshold is Pause time minus 4 slot times (PT-4 slot times).
- **2'b01:** The threshold is Pause time minus 28 slot times (PT-28 slot times).
- **2'b10:** The threshold is Pause time minus 144 slot times (PT-144 slot times).
- **2'b11:** The threshold is Pause time minus 256 slot times (PT-256 slot times). The slot time is defined as the time taken to transmit 512 bits (64 bytes) on the MII interface.

**UPFD**
A pause frame is processed when it has the unique multicast address specified in the IEEE Std 802.3. When this bit set, the MAC can also detect Pause frames with unicast address of the station. This unicast address should be as specified in the EMACADDRO High Register and EMACADDRO Low Register. When this bit is reset, the MAC only detects Pause frames with unique multicast address.

**RFCE**
When this bit set, when the MAC decodes the received Pause frame and disables its transmitter for a specified (Pause) time. When this bit is reset, the decode function of the Pause frame is disabled.
(R/W)

**TFCE**
In the full-duplex mode, when this bit is set, the MAC enables the flow control operation to transmit Pause frames. When this bit is reset, the flow control operation in the MAC is disabled and the MAC does not transmit any Pause frames. In the half-duplex mode, when this bit is set, the MAC enables the backpressure operation. When this bit is reset, the backpressure feature is disabled.
(R/W)

**Footer:**
Continued on the next page...

**Document Footer Information:**
Espressif Systems
506 ESP32 TRM (Version 5.6)
Submit Documentation Feedback