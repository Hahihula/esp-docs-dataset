

```markdown
Chapter 52 Ethernet Media Access Controller (EMAC) GoBack

- Discarding frames in cases of late collisions, excessive collisions, excessive deferrals, and underflow conditions
- Software control to flush TX FIFO

## 52.3 Ethernet MAC Architecture

Figure 52.3-1 shows the block diagram of the Ethernet MAC.

![Figure 52.3-1. Ethernet MAC Block Diagram](image_path)

Ethernet MAC consists of three layers: EMAC_CORE (MAC Core Layer), EMAC_MTL (MAC Transition Layer), and EMAC_DMA (Direct Memory Access). Each of these three layers has two directions: TX and RX. They are connected to the system through the Advanced High Performance Bus (AHB) and the Advanced Peripheral Bus (APB) on the chip. Off the chip, they communicate with the external PHY through the MII and RMII interfaces to establish an Ethernet connection.

## 52.4 Functional Description

### 52.4.1 EMAC_CORE

The MAC supports two interfaces (see Section 52.4.4) towards the PHY chip. The PHY interface can be selected only once after the chip reset. The MAC core communicates with the application side (DMA side) using the MAC Transmit Interface (MTI), MAC Receive Interface (MRI), and the MAC Control Interface (MCI).

#### 52.4.1.1 Transmission

Transmission is initiated when the MTL application pushes in data with the SOF signal (start of frame) asserted. When the SOF signal is detected, the MAC accepts the data and begins transmitting to the RMII or MII. The time required to transmit the frame data to the RMII or MII after the application initiates transmission is variable, depending on delay factors like IFG delay, time to transmit preamble or SFD (Start Frame Delimiter), and any back-off delays for half-duplex mode. Until then, the MAC does not accept the data received from MTL by deasserting the ready signal.
```