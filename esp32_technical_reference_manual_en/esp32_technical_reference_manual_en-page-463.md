Title: Chapter 24 Ethernet Media Access Controller (EMAC)

Figure Caption:
- Figure 24.1-2. Ethernet Block Diagram

Body Text:

The Tx FIFO is flushed by software control.

Calculating the IPv4 header checksum, as well as the TCP, UDP, or ICMP checksum, and then inserting them into frames transmitted in store-and-forward mode.

Ethernet Block Diagram
- Figure 24.1-2 shows the block diagram of the Ethernet.
  
  Ethernet MAC consists of the MAC-layer configuration register module and three layers: EMAC_CORE (MAC Core Layer), EMAC_MTL (MAC Transition Layer), and EMAC_DMA (Direct Memory Access). Each of these three layers has two directions: Tx and Rx. They are connected to the system through the Advanced High-Performance Bus (AHB) and the Advanced Peripheral Bus (APB) on the chip. Off the chip, they communicate with the external PHY through the MII or RMII interfaces to establish an Ethernet connection.

Subtitle:
24.2 EMAC_CORE

Body Text:

The MAC supports many interfaces with the PHY chip. The PHY interface can be selected only once after reset. The MAC communicates with the application side (DMA side), using the MAC Transmit Interface (MTI), MAC Receive Interface (MRI) and the MAC Control Interface (MCI).

Subtitle:
24.2.1 Transmit Operation

Body Text:

A transmit operation is initiated when the MTL Application pushes in data at the time a response signal is asserted. When the SOF (start of frame) signal is detected, the MAC accepts the data and begins transmitting to the RMII or MII. The time required to transmit the frame data to the RMII or MII, after the application initiates transmission, varies, depending on delay factors like IFG delay, time to transmit Preamble or SFD (Start Frame Delimiter), and any back-off delays in half-duplex mode. Until then, the MAC does not accept the data received from MTL by de-asserting the ready signal.

After the EOF (end of frame) is transmitted to the MAC, the MAC completes the normal transmission and yields the Transmit Status to the MTL. If a normal collision (in half-duplex mode) occurs during transmission, the MAC makes valid the Transmit Status in the MTL. It then accepts and drops all further data until the next SOF is received.

Footer:
- Espresso Systems
- Page number: 463

Link:
- Submit Documentation Feedback