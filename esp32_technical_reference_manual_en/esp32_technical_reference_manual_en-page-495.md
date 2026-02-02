**Chapter Title:**
Chapter 24 Ethernet Media Access Controller (EMAC)

**Section Header:**
Register 24.7 DMA OPERATION_MODE_REG (0x018)

**Continuation Notice:**
Continued from the previous page...

**Field Descriptions and Values with Access Type Indicators in Parentheses:**  
- **RX_THRESH_CTRL**: These two bits control the threshold level of the MTL Receive FIFO. Transfer (request) to DMA starts when the frame size within the MTL Receive FIFO is larger than the threshold. 2'b00: 64; 2'b01: 32; 2'b10: 96; 2'b11: 128. (R/W)
- **OPT_SECOND_FRAME**: When this bit is set, it instructs the DMA to process the second frame of the Transmit data even before the status for the first frame is obtained. (R/W)
- **START_STOP_RX**: When this bit is set, the Receive process is placed in the Running state. The DMA attempts to acquire the descriptor from the Receive list and processes the incoming frames.When this bit is cleared, the Rx DMA operation is stopped after the transfer of the current frame. (R/W)

**Footer:**
Espressif Systems  
495 ESP32 TRM (Version 5.6)  

**Link Texts at Bottom:**  
Submit Documentation Feedback

**Navigation Link in Header:**
GoBack