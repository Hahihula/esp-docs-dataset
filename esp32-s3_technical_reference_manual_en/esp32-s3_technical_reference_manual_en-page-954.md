**Title:**
Chapter 26 UART Controller (UART)

**Menu/Navigation Link:**
GoBack

**Register Information:**
- Register Name: UART_INT_CLR_REG (0x0010)
- Bit Description Table:
  - Bits are labeled from 31 to 0.
  - Each bit has a corresponding function related to UART interrupts.

**Bit Descriptions with Comments:**

- **UART_RXFIFO_FULL_INT_CLR**
  - Set this bit to clear the UART_THE_RXFIFO_FULL_INT interrupt. (WT)

- **UART_TXFIFO_EMPTY_INT_CLR**
  - Set this bit to clear the UART_TXFIFO_EMPTY_INT interrupt. (WT)

- **UART_PARITY_ERR_INT_CLR**
  - Set this bit to clear the UART_PARITY_ERR_INT interrupt. (WT)

- **UART_FRM_ERR_INT_CLR**
  - Set this bit to clear the UART_FRM_ERR_INT interrupt. (WT)

- **UART_RXFIFO_OVF_INT_CLR**
  - Set this bit to clear the UART_UART_RXFIFO_OVF_INT interrupt. (WT)

- **UART_DSR_CHG_INT_CLR**
  - Set this bit to clear the UART_DSR_CHG_INT interrupt. (WT)

- **UART_CTS_CHG_INT_CLR**
  - Set this bit to clear the UART_CTS_CHG_INT interrupt. (WT)

- **UART_BRK_DET_INT_CLR**
  - Set this bit to clear the UART_BRK_DET_INT interrupt. (WT)

- **UART_RXFIFO_TOUT_INT_CLR**
  - Set this bit to clear the UART_RXFIFO_TOUT_INT interrupt. (WT)

- **UART_SW_XON_INT_CLR**
  - Set this bit to clear the UART_SW_XON_INT interrupt. (WT)

- **UART_SW_XOFF_INT_CLR**
  - Set this bit to clear the UART_SW_XOFF_INT interrupt. (WT)

- **UART_GLITCH_DET_INT_CLR**
  - Set this bit to clear the UART_GLITCH_DET_INT interrupt. (WT)

- **UART_TX_BRK_DONE_INT_CLR**
  - Set this bit to clear the UART_TX_BRK_DONE_INT interrupt. (WT)

- **UART_TX_BRK_IDLE_DONE_INT_CLR**
  - Set this bit to clear the UART_TX_BRK_IDLE DONE INT interrupt. (WT)

- **UART_TXDone_INT_CLR**
  - Set this bit to clear the UART_TX_DONE_INT interrupt. (WT)

- **UART_RS485_PARITY_ERR_INT_CLR**
  - Set this bit to clear the UART_RS485_PARITY_ERR_INT interrupt. (WT)

**Footer:**
Continued on the next page...

**Document Information:**
Espressif Systems
954 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback