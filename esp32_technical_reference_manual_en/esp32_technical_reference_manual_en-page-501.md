**Chapter Title:**
Chapter 24 Ethernet Media Access Controller (EMAC)

**Section Header:**
Register 24.15. EMACONFIG_REG (0x1000) - GoBack

**Continuation Note:**
Continued from the previous page...

**Subsection with List and Description of Bits in Register:**

- **EMACINTERFRAMEGAP**: These bits control the minimum IFG between frames during transmission.
  - `3'b000`: 96 bit times
  - `3'b001`: 88 bit times
  - `3'b010`: 80 bit times
  - `3'b111`: 40 bit times. In the half-duplex mode, the minimum IFG can be configured only for 64 bit times (IFG = 100). Lower values are not considered.

- **EMACDISABLECRS**: When set high, this bit makes the MAC transmitter ignore the MII CRS signal during frame transmission in the half-duplex mode. This request results in no errors generated because of Loss of Carrier or No Carrier during such transmission. When this bit is low, the MAC transmitter generates such errors because of Carrier Sense and can even abort the transmissions.
  - (R/W)

- **EMACMII**: This bit selects the Ethernet line speed. It should be set to `1` for 10 or 100 Mbps operations. In 10 or 100 Mbps operations, this bit, along with FES(EMACFSPED) bit, it selects the exact linespeed. In the 10/100 Mbps-only operations, the bit is always `1`.
  - (R/W)

- **EMACFESPEED**: This bit selects the speed in the MII, RMII interface.
  - `0`: 10 Mbps
  - `1`: 100 Mbps
  - (R/W)

- **EMACRXOWN**: When this bit is set, the MAC disables the reception of frames when the TX_EN is asserted in the half-duplex mode. When this bit is reset, the MAC receives all packets that are given by the PHY while transmitting. This bit is not applicable if the MAC is operating in full-duplex mode.
  - (R/W)

- **EMACLOOPBACK**: When this bit is set, the MAC operates in the loopback mode MII. The MII Receive clock input (CLK_RX) is required for the loopback to work properly because the transmit clock is not looped-back internally.
  - (R/W)

- **EMACDUPLEX**: When this bit is set, the MAC operates in full-duplex mode where it can transmit and receive simultaneously. This bit is read only with default value of `1` in the full-duplex-mode.
  - (R/W)

- **EMACRXIPCOFFLOAD**: When this bit is set, the MAC calculates the 16-bit one’s complement sum of all received Ethernet frame payloads. It also checks whether the IPv4 Header checksum (assumed to be bytes `25/26` or `29/30` (VLAN-tagged) of the received Ethernet frame) is correct for the received frame and gives the status in the receive status word. The MAC also appends the 16-bit checksum calculated for the IP header data payload (bytes after the IPv4 header) and appends it to the Ethernet frame transferred to the application (when Type `2 COE` is deselected). When this bit is reset, this function is disabled.
  - (R/W)

**Continuation Note:**
Continued on the next page...

**Footer Information:**
Espressif Systems
Page number and document version:
501 ESP32 TRM (Version 5.6)
Submit Documentation Feedback