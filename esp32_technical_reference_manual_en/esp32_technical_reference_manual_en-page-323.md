**Title:**
Chapter 19 UART Controller (UART)

**Header:**
Register 19.2. UART_INT_RAW_REG (0x4)

**Menu/Table:**
- A table showing the register bits from 31 to 0, with each bit labeled as follows:
  - UART_AT_CMD_CHAR_DET_INT_RAW
  - UART_AT_CMD_CHAR_DET_INT
  - UART_RS485_CLASH_INT_RAW
  - UART_RS485_FRM_ERR_INT_RAW
  - UART_RS485_PARITY_ERR_INT_RAW
  - UART_TX_DONE_INT_RAW
  - UART_TX_BRK_IDLE DONE_INT_RAW
  - UART_TX_BRK DONE_INT_RAW
  - UART_GLITCH_DET_INT_RAW
  - UART_SW_XOFF_INT_RAW
  - UART_SW_XON_INT_RAW
  - UART_RXFIFO_TOUT_INT_RAW
  - UART_BRK_DET_INT_RAW
  - UART_CTS_CHG_INT_RAW
  - UART_DSR_CHG_INT_RAW
  - UART_RXFIFO_OVF_INT_RAW
  - UART_FRM_ERR_INT_RAW

**Body Text:**
- Descriptions of each register bit:
  - **UART_AT_CMD_CHAR_DET_INT_RAW**: The raw interrupt status bit for the UART_AT_CMD_CHAR_DET_INT (RO)
  - **UART_AT_CMD_CHAR_DET_INT**: Interrupt.
  - **UART_RS485_CLASH_INT_RAW**: The raw interrupt status bit for the UART_RS485_CLASH_INT (RO)
  - **UART_RS485_FRM_ERR_INT_RAW**: The raw interrupt status bit for the UART_RS485_FRM_ERR_INT (RO)
  - **UART_RS485_PARITY_ERR_INT_RAW**: The raw interrupt status bit for the UART_RS485_PARITY_ERR_INT (RO)
  - **UART_TXDone_INT_RAW**: The raw interrupt status bit for the UART_TX_DONE_INT (RO)
  - **UART_TX_BRK_IDLE DONE_INT_RAW**: The raw interrupt status bit for the UART_TX_BRK_IDLE DONE_INT (RO)
  - **UART_TX_BRK DONE_INT_RAW**: The raw interrupt status bit for the UART_TX_BRK DONE_INT (RO)
  - **UART_GLITCH_DET_INT_RAW**: The raw interrupt status bit for the UART_GLITCH_DET_INT (RO)
  - **UART_SW_XOFF_INT_RAW**: The raw interrupt status bit for the UART_SW_XOFF_INT (RO)
  - **UART_SW_XON_INT_RAW**: The raw interrupt status bit for the UART_SW_XON_INT (RO)
  - **UART_RXFIFO_TOUT_INT_RAW**: The raw interrupt status bit for the UART_RXFIFO_TOUT_INT (RO)
  - **UART_BRK_DET_INT_RAW**: The raw interrupt status bit for the UART_BRK_DET_INT (RO)
  - **UART_CTS_CHG_INT_RAW**: The raw interrupt status bit for the UART_CTS_CHG_INT (RO)
  - **UART_DSR_CHG_INT_RAW**: The raw interrupt status bit for the UART_DSR_CHG_INT (RO)
  - **UART_RXFIFO_OVF_INT_RAW**: The raw interrupt status bit for the UART_RXFIFO_OVF_INT (RO)
  - **UART_FRM_ERR_INT_RAW**: The raw interrupt status bit for the UART_FRM_ERR_INT (RO)

**Footer:**
Continued on the next page...

**Company Information:**
Espressif Systems

**Document Version and Feedback Link:**
ESP32 TRM (Version 5.6)
Submit Documentation Feedback