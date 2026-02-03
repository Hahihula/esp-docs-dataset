**Chapter Title:**
Chapter 31 Two-wire Automotive Interface (TWAI®)

**Back Link:**
GoBack

**Register Information:**
- **Register Name:** TWAI_INT_RAW_REG (0x000C)
- **Address Bits:** [Diagram showing address bits from 31 to 0]

**Field Descriptions and Functions in the Register:**

- **TWAI_RX_INT_ST**: Receive interrupt. If this bit is set to 1, it indicates there are messages to be handled in the RX FIFO.
- **TWAI_TX_INT_ST**: Transmit interrupt. If this bit is set to 1, it indicates the message transmission is finished and a new transmission can start.
- **TWAI_ERR_WARN_INT_ST**: Error warning interrupt. This field will indicate an error status signal or bus-off state change in TWAI Status register (e.g., switched from 0 to 1).
- **TWAI_OVERRUN_INT_ST**: Data overrun interrupt. If this bit is set to 1, it indicates a data overrun.
- **TWAI_ERR_PASSIVE_INT_ST**: Error passive interrupt. This field will indicate the error status change in TWAI Controller between active and passive states due to changes of error counters (e.g., switched from an active state).
- **TWAI_ARB_LOST_INT_ST**: Arbitration lost interrupt. If this bit is set to 1, it indicates that arbitration has been lost.
- **TWAI_BUS_ERR_INT_ST**: Error interrupt. This field will indicate a bus error detected on the TWAI bus (e.g., switched from an idle state).
- **TWAI_BUS_STATE_INT_ST**: Bus state interrupt. If this bit is set to 1, it indicates that there has been some change in status of TWAI controller.

**Footer:**
Espressif Systems
Page Number: 1225
Document Title: ESP32-S3 TRM (Version 1.7)
Link Texts:
- Submit Documentation Feedback