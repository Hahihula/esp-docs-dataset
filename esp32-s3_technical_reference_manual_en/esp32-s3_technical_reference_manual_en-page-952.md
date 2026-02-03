**Title:**
Chapter 26 UART Controller (UART)

**Subtitle:**
Register 26.5. UART_INT_ENA_REG (0x00C0)

**Diagram Description:**
The diagram shows a bit map of the register with labels for each bit position, indicating different interrupt enable bits related to UART functions.

**Bit Labels and Descriptions:**

- **UART_WAKE_UP_INTENA:** This is an enable bit.
- **UART_RXFIFO_FULL_INTENA:** This is the enable bit for UART_RXFIFO_FULL_INT. (R/W)
- **UART_TXFIFO_EMPTY_INTENA:** This is the enable bit for UART_TXFIFO_EMPTY_INT. (R/W)
- **UART_PARITY_ERR_INTENA:** This is the enable bit for UART_PARITY_ERR_INT. (R/W)
- **UART_FRM_ERR_INTENA:** This is the enable bit for UART_FRM_ERR_INT. (R/W)
- **UART_RXFIFO_OVF_INTENA:** This is the enable bit for UART_RXFIFO_OVF_INT. (R/W)
- **UART_DSR_CHG_INTENA:** This is the enable bit for UART_DSR_CHG_INT. (R/W)
- **UART_CTS_CHG_INTENA:** This is the enable bit for UARTCTS_CHG_INT. (R/W)
- **UART_BRK_DET_INTENA:** This is the enable bit for UARTBRK_DET_INT. (R/W)
- **UART_RXFIFO_TOUT_INTENA:** This is the enable bit for UART_RXFIFO_TOUT_INT. (R/W)
- **UART_SW_XON_INTENA:** This is the enable bit for UART_SW_XON_INT. (R/W)
- **UART_SW_XOFF_INTENA:** This is the enable bit for UART_SW_XOFF_INT. (R/W)
- **UART_GLITCH_DET_INTENA:** This is the enable bit for UARTGLITCH_DET_INT. (R/W)
- **UART_TX_BRK_DONE_INTENA:** This is the enable bit for UART_TXBRK_DONE_INT. (R/W)
- **UART_TX_BRK_IDLEDone_INTENA:** This is the enable bit for UART_TX_BRK_IDLEDONE_INT. (R/W)
- **UART_TX_DONE_INTENA:** This is the enable bit for UART_TX_DONE_INT. (R/W)

**Footer:**
Continued on the next page...

**Page Information:**
Espressif Systems
952 ESP32-S3 TRM (Version 1.7)