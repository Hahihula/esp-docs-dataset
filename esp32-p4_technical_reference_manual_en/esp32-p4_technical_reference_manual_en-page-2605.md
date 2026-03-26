

```markdown
Chapter 52 Ethernet Media Access Controller (EMAC)

If a match is detected (i.e., the destination address of the received frame matches the destination address of the reserved control frame), the MAC decides whether to transmit the received control frame to the application, according to the PCF field.

The MAC also decodes the type, the opcode, and the pause timer field of the receiving control Frame. If the byte count of the status indicates 64 bytes, and if there is no CRC error, the MAC transmitter will pause the transmission of any data frame for the duration of the decoded pause time value multiplied by the slot time (64 byte times for 10/100 Mbit/s mode). Meanwhile, if another pause frame is detected with a zero pause time, the MAC will reset the pause time and give another pause request.

If the received control frame matches neither the type field (0x8808), the opcode (0x00001), nor the byte length (64 bytes), or if there is a CRC error, the MAC will not generate a pause.

In the case of a pause frame with a multicast destination address, the MAC filters the frame according to the address match.

For a pause frame with a unicast destination address, the filtering depends on whether the DA matched the contents of the MAC Address Register 0 and the UPFD (detecting a pause frame even with a unicast destination address) is set. The PCF register controls the filtering for control frames in addition to the address filter.

Receive Operation Multiframe Handling

Since the status is available immediately following the data, the MAC is capable of storing any number of frames into the FIFO, as long as it is not full.

Error Handling

If the RX FIFO is full before it receives the EOF data from the MAC, an overflow will be declared and the whole frame will be dropped. The status bit RDESO[11] will reflect the fact that this frame is a partial frame due to overflow. The RX FIFO can perform the filtering of error frames and runt frames, if this function is enabled via FLUSH_TX_FIFO and FWD_UNDER_GF.

In cut-through mode, if a frame's status and length are available when reading an SOF from the RX FIFO, the whole error frame can be dropped. The DMA can flush the error frame being read from the FIFO by clearing FWD_ERR_FRAME to 0. The DMA then stops transferring data to the application, internally reads out the rest of the frame, and drops it. The MTL will then start the transfer of the next frame, if it is available. If FIFO is available, the transmission of the next frame will be initiated.

Receive Status Word

At the end of the Ethernet frame transfer, the MAC outputs the receive status to the application via EMAC_DMA. The detailed description of the receive status is the same for bit[31:0] in RDESO.

52.4.2 EMAC_MTL (MAC Transaction Layer)

The MAC Transaction Layer provides FIFO memory to buffer and regulate the frames between the application system memory and the MAC. It also enables the data to be transmitted between the application clock domain and the MAC clock domains. The MTL layer has two data paths, namely the Transmit path and the Receive path. The data path for both directions is 32-bit wide and operates with a simple FIFO protocol.
```