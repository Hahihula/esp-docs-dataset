**Chapter Title:**
Chapter 31 Two-wire Automotive Interface (TWAI®)

**Section Header:**
Register 31.19. TWAI_CMD_REG (0x0004)

**Body Text with Table:**

- **TWAI_TX_REQ**: Set the bit to 1 to drive nodes to start transmission. (WO)
- **TWAI_ABORT_TX**: Set the bit to 1 to cancel a pending transmission request. (WO)
- **TWAI_RELEASEBuf**: Set the bit to 1 to release the RX buffer. (WO)
- **TWAI_CLR_OVERRUN**: Set the bit to 1 to clear the data overrun status bit. (WO)
- **TWAI_SELF_RX_REQ**: Self reception request command. Set the bit to 1 to allow a message be transmitted and received simultaneously. (WO)

**Section Header:**
Register 31.20. TWAI_STATUS_REG (0x0008)

**Body Text with Table:**

- **TWAI_RXBuf_ST**: The data in the RX buffer is not empty, with at least one received data packet.
- **TWAI_OVERRUN_ST**: The RX FIFO is full and data overrun has occurred. (RO)
- **TWAI_TXBuf_ST**: The TX buffer is empty, the CPU may write a message into it. (RO)
- **TWAI_TXComplete**: The TWAI controller has successfully received a packet from the bus.
- **TWAI_RX_ST**: The TWAI Controller is receiving a message from the bus.
- **TWAI_TX_ST**: The TWAI Controller is transmitting a message to the bus.

**Body Text with Table:**

- **TWAI_ERR_ST**: At least one of the RX/TX error counter has reached or exceeded the value set in register TWAI_ERR_WARNING_LIMIT_REG. (RO)
- **TWAI_BUS_OFF_ST**: In bus-off status, the TWAI Controller is no longer involved in bus activities.
- **TWAI_Miss_ST**: This bit reflects whether the data packet in the RX FIFO is complete: 1: The current packet is missing; 0: The current packet is complete.

**Footer Information:**
Espressif Systems
Submit Documentation Feedback

**Document Version and Page Number:**
ESP32-S3 TRM (Version 1.7)
Page number not visible in the image provided