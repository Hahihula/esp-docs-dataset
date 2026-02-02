**Chapter Title:**
Chapter 24 Ethernet Media Access Controller (EMAC)

**Body Text:**

multicast address of the control frame (0x180 C200 0001). If a match is detected (i.e. the destination address of the received frame matches the destination address of the reserved control frame), the MAC will determine whether to transmit the received control frame to the application, according to the PCF (Pass Control Frames) bit in the Frame Register.

The MAC will also decode the type, the opcode, and the pause timer field of the Receive Control Frame. If the value of the status byte counter is 64 bits and there are no CRC errors, the MAC transmitter will halt the transmission of any data frame. The duration of the pause is the decoded pause time value multiplied by the interval (which is 64 bytes for both 10 Mbit/s and 100 Mb/s modes). At the same time, if another pause frame of zero pause time is detected, the MAC will reset the pause time to manage the new pause request.

If the type field (0x8808), the opcode (0x00001), and the byte length (64 bytes) of the received control frame are not 0x8808, 0x00001, and 64 bytes, respectively, or if there is a CRC error, the MAC will not generate a pause.

If a pause frame has a multicast destination address, the MAC filters the frame, according to the address matching.

For pause frames with a unicast destination address, the MAC checks whether the DA matches the content of the EMACADDRO Register, and whether the Unicast Pause Frame Detect (UPFD) bit in the Flow Control Register is set to 1. The Pass Control Frames (PCF) bits in the Frame Filter Register [7:6] control the filtering of frames and addresses.

**Subsection Title:**
24.2.2.4 Reception of Multiple Frames

Since the status is available immediately after the data is received. Frames can be stored there, as long as the FIFO is not full.

**Subsection Title:**
24.2.2.5 Error Handling

If the Rx FIFO is full before receiving the EOF data from the MAC, an overflow will be generated and the entire frame will be discarded. In fact, status bit RDESO[1] will indicate that this frame is partial due to an overflow, and that it should be discarded.

If the function that corresponds to the Flush Transmit FIFO (FTF) bit and the Forward Undersized Good Frames (FUGF) bit in the Operation Mode Register is enabled, the Rx FIFO can filter error frames and runt frames. If the receive FIFO is configured to operate in store-and-forward mode, all error frames will be filtered and discarded.

In passthrough mode, if a frame’s status and length are available when reading a SOF from the Rx FIFO, the entire error frame can be discarded. DMA can clear the error frame being read from the FIFO by enabling the Receive Frame Clear bit. The data transmission to the application (DMA) will then stop, and the remaining frames will be read internally and discarded. If FIFO is available, the transmission of the next frame will be initiated.

**Subsection Title:**
24.2.2.6 Receive Status Word

After receiving the Ethernet frames, the MAC outputs the receive status to the application. The detailed description of the receive status is the same as that which is configured by bit [31:0] in RDESO.

**Footer Information:**

Espressif Systems
466 ESP32 TRM (Version 5.6)
Submit Documentation Feedback