**Chapter Title:**
Chapter 24 Ethernet Media Access Controller (EMAC)

**Section Header:**
GoBack

**Body Text with List Items and Descriptions for Each Item in the List:**

1. **MII_TX_CLK:** TX clock signal.
   - This signal provides the reference timing for TX data transmission.

2. **MII_TXD[3:0]:**
   - Transmit data signal in groups of four, syn-driven by the MAC sub-layer,
   - and valid only when MII_TX_EN signal is valid (MII_TXD[0] is the lowest significant bit
   - and MII_TXD[3] is the highest significant bit).
   - When the signal MII_TX_EN is pulled low, sending data does not have any effect on the PHY.

3. **MII_TX_EN:**
   - Transmit data enable signal.
   - This signal indicates that the MAC is currently sending nibbles (4 bits) for the MII.
   - This signal must be synchronized with the first nibble of the header (MII_TX_CLK)
   - and must be synchronized when all nibbles to be transmitted are sent to the MII.

4. **MII_RX_CLK:**
   - RX clock signal.
   - This signal provides the reference timing for RX data transmission.
   - The frequencies are divided into two types:
     1. 2.5 MHz at the data transmission rate of 10 Mbit/s,
     2. and 25 MHz at 100 Mbit/s.

5. **MII_RXD[3:0]:**
   - Receive data signal in groups of four, syn-driven by the PHY.
   - This is valid only when
   - The highest significant bit (MII_RXD[0] is the lowest significant bit and MI_RXD[3] is the highest 
   - When MII_RX_DV is disabled and MII_RX_ER is enabled,
   - represents specific information from the PHY.

6. **MII_RX_DV:**
   - Receive valid signal.
   - This signal indicates that the PHY is currently receiving
   - recovered and decoded nibble that will be transmitted to the MII (MIll).
   - The signal must be synchronized with 
   - the first nibble of the received frame (MIll_RX_CLK) and remain synchronized till the last nibble of the 
   - recovered frame.
   - This signal must be disabled before the first clock cycle following the last nibble. In
   - order to receive the frame correctly, MII_RX_DV signal must cover the frame to be received over the time range,
   - starting no later than when the SFD field appears.

7. **MII_CRS:**
   - Carrier sense signal.
   - When the transmitting or receiving medium is in the non-idle state (the
   - signal is enabled by the PHY).
   - When the transmitting or receiving medium is in the idle state, 
   - The signal must be disabled by the PHY. MII must ensure that the MIll_CRS signal remains valid under conflicting conditions.
   - This signal does not need to be synchronized with TX and RX clocks (in full-duplex mode,
   - this signal is insignificant).

8. **MII_COL:**
   - Collision detection signal.

9. **MII_RX_ER:**
   - Receive error signal
   - The signal must remain for one or more cycles 
   - to indicate that an error has been detected somewhere in the frame (MIll_RX_CLK)

10. **MDIO and MDC:**
    - Management Data Input/Output and Management Data Clock.
    - Two signals constitute a serial bus defined for Ethernet family of IEEE 802.3 standards, 
    - used to transfer control
    - data information between the MAC sublayer.

**Subsection Title with Subsection Content Description in Markdown Format:**

### **24.6.1.2 MII Clock**
- In MIll mode,
   There are two directions of clock (Tx and Rx clocks) 
   The interface between MIll and the PHY.
   - MII_TX_CLK is used to synchronize TX data, while
   - MII_RX_CLK is used for synchronizing RX data.

**Footer:**

Espressif Systems

471 ESP32 TRM (Version 5.6)

Submit Documentation Feedback