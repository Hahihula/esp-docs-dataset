

```markdown
Chapter 52 Ethernet Media Access Controller (EMAC)
GoBack

After the EOF (end of frame) is transmitted to the MAC, the MAC completes normal transmission and then gives the Transmit Status to the MTL. If a normal collision (in half-duplex mode) occurs during transmission, the MAC core makes valid the Transmit Status to the MTL. It will then accept and drop all further data until the next SOF is received. The MTL block should retransmit the same frame from SOF on observing a retry request (in the Status) from the MAC.

The MAC issues an underflow status if the MTL is not able to provide the data continuously during the transmission. During the normal transmission of a frame from the MTL, if the MAC receives an SOF without getting an EOF for the previous frame, then the SOF is ignored and the new frame is considered as a continuation of the previous frame.

Transmit Flow Control

In full-duplex mode, when the Transmit Flow Control Enable bit (TFCE) is set to 1, the MAC generates pause frames and transmits them as necessary, with the calculated CRC appended.

Pause frame generation can be initiated in two ways. When the application sets the Flow Control Busy bit (FCBBA) to 1, or when the RX FIFO is full, a pause frame is transmitted.

*   If the application has requested flow control by setting the FCBBA bit to 1, the MAC will generate and transmit a single pause frame. The value of the pause time in the generated frame is the pause time value programmed in the PAUSE_TIME field. If the application wants to extend or end the pause prior to the time specified in the previously transmitted pause frame, it must request another pause frame transmission after programming the pause time field PAUSE_TIME with an appropriate value.
*   If the application has requested flow control when the RX FIFO is full, the MAC will generate and transmit a pause frame. The value of the pause time in the generated frame is the pause time value programmed in the PAUSE_TIME field. If the RX FIFO remains full at a configurable number of slot times (PLT) before the pause time runs out, a second pause frame will be transmitted. The process will be repeated as long as the RX FIFO remains full. If the FIFO is no longer full prior to the sampling time, the MAC will send a pause frame with zero pause time to indicate to the remote end that the RX buffer is ready to receive new data frames.

Retransmission During Collision

In half-duplex mode, a collision may occur on the MAC line interface when frames are transmitted to the MAC. The MAC may indicate a retry attempt by giving the status even before the EOF is transferred. Then the MAC will enable the retransmission by popping out the frame again from the FIFO. After more than 96 bytes are popped towards the MAC core, the FIFO controller frees the space in the FIFO, and makes it available to the DMA to push in more data. This means that the retransmission is not possible after this threshold is crossed or when the MAC core indicates a late-collision event.

The MAC transmitter may abort the transmission of a frame because of collision, TX FIFO underflow, loss of carrier, jabber timeout, no carrier, excessive deferral, or late collision. When frame transmission is aborted because of collision, the MAC requests retransmission of the frame.

Transmit Status Word

At the end of the Ethernet frame transfer, the MAC outputs the transmit status to the application. The detailed description of the Transmit Status is the same as for TDESO.
```