**Chapter Title:**
Chapter 27 SD/MMC Host Controller (SDHOST)

**Register Information:**
- **Register Name:** STATUS_REG (0x0048)
- **Field Descriptions and Values in Binary Format**

| Bit | Description |
|-----|-------------|
| 31, 30, 29 | FIFO_COUNT - FIFO count, number of filled locations in FIFO. (RO) |
| ... | ... |

**Fields:**
- **FIFO_COUNT:** FIFO count, number of filled locations in FIFO.
- **RESPONSE_INDEX:** Index of previous response, including any auto-stop sent by core. (RO)
- **DATA_STATE_MC BUSY:** Data transmit or receive state-machine is busy. (RO)
- **DATA BUSY:** Inverted version of raw selected card_data[0]. (RO)

**Data State 3:**
- **DATA_3_STATUS:** Raw selected card_data[3], checks whether card is present.
  - O: card not present
  - 1: card present

**Command FSM States:**
- **COMMAND FSM STATES:** Command FSM states. (RO)
  - Idle, Send init sequence, Send cmd start bit, Send cmd tx bit,
    - Continue with various command and receive steps up to Wait, cmd-to-response turnaround.

**Status Fields:**
- **FIFO_FULL:** FIFO is full status.
- **FIFO_EMPTY:** FIFO is empty status.
- **FIFO_TX WATERMARK:** FIFO reached Transmit watermark level, not qualified with data transfer. (RO)
- **FIFO_RX WATERMARK:** FIFO reached Receive watermarked level, not qualified with data transfer.

**Footer:**
Espressif Systems
621 ESP32 TRM (Version 5.6)

**Navigation Links:**
GoBack

**Action Link:**
Submit Documentation Feedback