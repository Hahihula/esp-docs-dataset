**Chapter Title:**
- Chapter 24 Ethernet Media Access Controller (EMAC)

**GoBack Link:** 
- GoBack

**Section Titles and Content:**

1. **MII_RXER input error**
   - The maximum frame size depends on the frame type:
     - The maximum size of untagged frames = 1518 bytes
     - The maximum size of VLAN frames = 1522 bytes

2. **24.5 EMAC_MTL (MAC Transaction Layer)**
   - Description: 
     - MAC Transaction Layer provides FIFO memory to buffer and regulates the frames between application system memory and the MAC.
     - Enables data transmission between application clock domain and MAC clock domains
     - MTL layer has two data paths, Transmit path and Receive path. Data path is 32-bit wide with simple FIFO protocol.

3. **24.6 PHY Interface**
   - Description:
     - DMA and Host driver communicate through Control and Status Registers (CSR) and Descriptor lists.
     - For details refer to Register Summary and Linked List Descriptors

4. **24.6.1 MII (Media Independent Interface)**
   - Definition: 
     - Media Independent Interface defines interconnection between MAC sublayers and PHYs at data transmission rate of 10 Mbit/s and 100 Mbit/s.

5. **24.6.1.1 Interface Signals Between MII and PHY**
   - Description:
     - Interface signals shown in Figure 24.6-1.
   - Image: 
     - A diagram labeled "Figure 24.6-1. MII Interface" showing connections between EMAC, ESP32, RMIIF, TX CLK, RX CLK, TXD[3:0], RXD[3:0], RX DV, External PHY.

**Footer Information:** 
- MIll Interface Signal Description:
- Espressif Systems
- Page Number and Document Version Info (470)
- Submit Documentation Feedback Link

**Note**: The image contains a diagram with labels indicating connections between different components such as EMAC, ESP32, RMIIF, TX CLK, RX CLK, TXD[3:0], RXD[3:0], RX DV, and External PHY.