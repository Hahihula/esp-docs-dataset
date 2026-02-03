**Title:**
Chapter 26 UART Controller (UART)

**Subtitle:**
Register 26.3. UART_INT_RAW_REG (0x0004)

**Body Text with Descriptions of Interrupts and Registers:**

Continued from the previous page...

- **UART_TX_BRK_DONE_INT_RAW**: This interrupt raw bit turns to high level when the transmitter completes sending NULL characters, after all data in TX FIFO are sent. (R/WTC/SS)
  
- **UART_TX_BRK_IDLEDone_INT_RAW**: This interrupt raw bit turns to high level when the transmitter has kept the shortest duration after sending the last data. (R/WTC/SS)

- **UART_TX_DONE_INT_RAW**: This interrupt raw bit turns to high level when the transmitter has sent out all data in FIFO. (R/WTC/SS)
  
- **UART_RS485_PARITY_ERROR_INT_RAW**: This interrupt raw bit turns to high level when the receiver detects a parity error from the echo of the transmitter in RS485 mode. (R/WTC/SS)

- **UART_RS485_FRM_ERR_INT_RAW**: This interrupt raw bit turns to high level when the receiver detects a data frame error from the echo of the transmitter in RS485 mode. (R/WTC/SS)
  
- **UART_RS485_CLASH_INT_RAW**: This interrupt raw bit turns to high level when a collision is detected between the transmitter and the receiver in RS485 mode. (R/WTC/SS)

- **UART_AT_CMD_CHAR_DET_INT_RAW**: This interrupt raw bit turns to high level when the receiver detects the configured UART_AT_CMD_CHA. (R/WTC/SS)
  
- **UART_WAKEUP_INT_RAW**: This interrupt raw bit turns to high level when the input RXD edge changes more times than what (UART_ACTIVE_THRESHOLD + 3) specifies in Light-sleep mode. (R/WTC/SS)

**Footer:**
Espressif Systems
949 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback