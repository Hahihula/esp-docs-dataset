**Chapter Title:**
Chapter 24 Ethernet Media Access Controller (EMAC)

**Section Heading and Subsection with Content:**

### 24.2.1.1 Transmit Flow Control

In full-duplex mode, when the Transmit Flow Control Enable bit (TFE bit in the Flow Control Register) is set to 1, the MAC will generate and send a pause frame as needed. The pause frame is added and transmitted together with the calculated CRC. The generation of pause frames can be initiated in two ways.

When the application sets the Flow Control Busy bit (FCB bit in the Flow Control Register) to 1, or when the Rx FIFO is full, a pause frame is transmitted.
- If an application has requested flow control by setting the FCB bit in the Flow Control Register to 1, the MAC will generate and send a single pause frame. The pause time value programmed in the Flow Control Register. To extend or end the pause time before the time specified in the previously transmitted pause frame, the application program must configure the pause time value in the Flow Control Register to the appropriate value and then request another pause frame transmission.
- If the application has requested flow control when the Rx FIFO is full, the MAC will generate and transmit a pause frame. The value of the pause time of the generated frame is the pause time value programmed in the Flow Control Register. If the Rx FIFO remains full during the configurable interval, which is determined by the Pause Low Threshold bit (PLT) in the Flow Control Register before the pause time expires, a second pause frame will be transmitted. As long as the Rx FIFO remains full, the process repeats itself. If the FIFO no longer fills up to sample times, the MAC will send a pause frame with zero pause time, indicating that remote end is ready for new data frame.

### 24.2.1.2 Retransmission During a Collision

In half-duplex mode, a collision may occur on the MAC line interface when frames are transmitted to the MAC. The MAC may even give a status to indicate a retry before the end of the frame is received. If more than 96 bytes are transmitted to the MAC core, the FIFO controller frees space in the FIFO, allowing DMA to push data into FIFO. This means that data cannot be retransmitted after threshold exceeded or when MAC core indicates late collision has occurred.

The MAC transmitter may abort transmission of a frame because of collision, Tx FIFO underflow, loss carrier, jabber timeout, no carrier, excessive deferral and late collision. When frame transmission is aborted due to collision, the MAC requests retransmission of the frame.
- The MAC strips Preamble before processing SFD.

### 24.2.2 Receive Operation

A receive operation initiated when MAC detects an RMII or MII. The MAC strips preamble from SFD and checks header fields for filtering FCS (Frame Check Sequence).