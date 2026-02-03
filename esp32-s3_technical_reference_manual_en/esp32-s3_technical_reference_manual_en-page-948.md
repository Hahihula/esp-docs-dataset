**Title:**
Chapter 26 UART Controller (UART)

**Header:**
Register 26.3. UART_INT_RAW_REG (0x0004)

**Body Text with Descriptions of Interrupts and Their Functions:**

- **UART_RXFIFO_FULL_INT_RAW**: This interrupt raw bit turns to high level when the receiver receives more data than what UART_RXFIFO_FULL_THRHD specifies.
  - (R/WTC/SS)
  
- **UART_TXFIFO_EMPTY_INT_RAW**: This interrupt raw bit turns to high level when the amount of data in TX FIFO is less than what UART_TXFIFO_EMPTY_THRHD specifies.
  - (R/WTC/SS)

- **UART_PARITY_ERR_INT_RAW**: This interrupt raw bit turns to high level when the receiver detects a parity error in the data.
  - (R/WTC/SS)
  
- **UART_FRM_ERR_INT_RAW**: This interrupt raw bit turns to high level when the receiver detects a data frame error.
  - (R/WTC/SS)

- **UART_RXFIFO_OVF_INT_RAW**: This interrupt raw bit turns to high level when the receiver receives more data than the capacity of RX FIFO.
  - (R/WTC/SS)
  
- **UART_DSR_CHG_INT_RAW**: This interrupt raw bit turns to high level when the receiver detects the edge change of DSRn signal.
  - (R/WTC/SS)

- **UART_CTS_CHG_INT_RAW**: This interrupt raw bit turns to high level when the receiver detects the edge change of CTSn signal.
  - (R/WTC/SS)
  
- **UART_BRK_DET_INT_RAW**: This interrupt raw bit turns to high level when the receiver detects a 0 after the stop bit.
  - (R/WTC/SS)

- **UART_RXFIFO_TOUT_INT_RAW**: This interrupt raw bit turns to high level when the receiver takes more time than UART_RX_TOThRD to receive a byte.
  - (R/WTC/SS)
  
- **UART_SW_XON_INT_RAW**: This interrupt raw bit turns to high level when the receiver receives an XON character and UART_SW_FLOW_CON_EN is set to 1.
  - (R/WTC/SS)

- **UART_SW_XOFF_INT_RAW**: This interrupt raw bit turns to high level when the receiver receives an XOFF character and UART_SW_FLOW_CON_EN is set to 1.
  - (R/WTC/SS)
  
- **UART_GLITCH_DET_INT_RAW**: This interrupt raw bit turns to high level when the receiver detects a glitch in the middle of a start bit.
  - (R/WTC/SS)

**Footer:**
Continued on the next page...

**Page Information:**
Espressif Systems
948 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback