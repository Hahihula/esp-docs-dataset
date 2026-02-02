**Title:**
Chapter 22 I2S Controller (I2S)

**Subtitle:**
Register 22.35. I2S_STATE_REG (0x00bc)

**Binary Diagram Description:**
- The diagram shows a binary register with bits labeled as follows:
  - `I2S_RX_FIFO_RESET_BACK`
    - Bit positions are shown from left to right.
    - Values in the bit positions range between '0' and '1'.
  - `I2S_TX_FIFO_RESET_BACK`
    - Similar structure, values ranging between '0' and '1'.

**Text Descriptions:**

- **I2S_RX_FIFO_RESET_BACK**
  This bit is used to confirm if the Rx FIFO reset is done. 
  - Value of "1": Reset is not ready.
  - Value of "0": Reset is ready.

- **I2S_TX_FIFO_RESET_BACK**
  This bit is used to confirm if the Tx FIFO reset is done.
  - Value of "1": Reset is not ready.
  - Value of "0": Reset is ready (RO).

- **I2S_TX_IDLE**
  The status bit of the transmitter. 
  - Value of "1": The transmitter is idle; 
  - Value of "0": The transmitter is busy.

**Footer:**
Espressif Systems
449 ESP32 TRM (Version 5.6)
Submit Documentation Feedback