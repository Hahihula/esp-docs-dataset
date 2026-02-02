**Chapter Title:**
Chapter 25 Two-Wire Automotive Interface (TWAI)

**Register Information for TWAI_CMD_REG (0x0004):**

- **TWAI_TX_REQ**: Set the bit to 1 to allow the driving nodes start transmission. (WO)
- **TWAI_ABORT_TX**: Set the bit to 1 to cancel a pending transmission request. (WO)
- **TWAI_RELEASEBuf**: Set the bit to 1 to release the RX buffer. (WO)
- **TWAI_CLR_OVERRUN**: Set the bit to 1 to clear the data overrun status bit. (WO)
- **TWAI_SELF_RX_REQ**: Self reception request command. Set the bit to 1 to allow a message be transmitted and received simultaneously. (WO)

**Register Information for TWAI_STATUS_REG (0x0008):**

- **TWAI_RXBuf_ST**: The data in the RX buffer is not empty, with at least one received data packet.
- **TWAI_OVERRUN_ST**: The RX FIFO is full and data overrun has occurred. (RO)
- **TWAI_TXBuf_ST**: The TX buffer is empty, the CPU may write a message into it. (RO)
- **TWAI_TXComplete**: The TWAI controller has successfully received a packet from the bus.
- **TWAI_RX_ST**: The TWAI Controller is receiving a message from the bus.
- **TWAI_TX_ST**: The TWAI Controller transmitting to the bus
- **TWAI_ERR_ST**: At least one of the RX/TX error counter has reached or exceeded the value set in register TWAI_ERR_WARNING_LIMIT_REG. (RO)
- **TWAI_BUS_OFF_ST**: In bus-off status, the TWAI Controller is no longer involved in bus activities.

**Footer:**
Espressif Systems
Submit Documentation Feedback

**Page Number and Document Version Information:** 
558 ESP32 TRM (Version 5.6)