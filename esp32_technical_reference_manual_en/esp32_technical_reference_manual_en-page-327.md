**Title:**
Chapter 19 UART Controller (UART)

**Header:**
Register 19.4. UART_INT_ENA_REG (0xC)

**Menu/Navigation Link:**
GoBack

**Table Description and Values:**
- The table lists various interrupt enable bits for the UART controller, each associated with a specific function.
  
| Bit Number | Function |
|------------|----------|
| 31         | Reserved |
| ...        | ...      |

**Interrupt Enable Bits Descriptions (Selected):**

- **UART_AT_CMD_CHAR_DET_INTENA**: The interrupt enable bit for the UART_AT_CMD_CHAR_DET_INT interrupt. (R/W)
  
- **UART_RS485_CLASH_INT_ENA**: The interrupt enable bit for the UART_RS485_CLASH_INT interrupt.
  - (R/W)

- **UART_RS485_FRM_ERR_INTENA**: The interrupt enable bit for the UART_RS485_FRM_ERR_INT interrupt. (R/W)
  
- **UART_RS485_PARITY_ERR_INTENA**: The interrupt enable bit for the UART_RS485_PARITY_ERR_INT interrupt.
  - (R/W)

- **UART_TX_DONE_INT_ENA**: The interrupt enable bit for the UART_TXDone_INT interrupt.
  - (R/W)
  
- **UART_TX_BRK_IDLE_DONE_INTENA**: The interrupt enable bit for the UART_TXBRK_IDLE_DONE_INT interrupt. (R/W)
  
- **UART_TX_BRK_DONE_INTENA**: The interrupt enable bit for the UART_TXBRK_DONE_INT interrupt.

- **UART_GLITCH_DET_INTENA**: The interrupt enable bit for the UART_GLITCH_DET_INT interrupt.
  - (R/W)

- **UART_SW_XOFF_INTENA**: The interrupt enable bit for the UART_SW_XOFF_INT interrupt. (R/W)
  
- **UART_SW_XON_INTENA**: The interrupt enable bit for the UART_SW_XON_INT interrupt.

- **UART_RXFIFO_TOUT_INTENA**: The interrupt enable bit for the UART_RXFIFO_TOUT_INT interrupt.
  - (R/W)

- **UART_BRK_DET_INTENA**: The interrupt enable bit for the UART_BRK_DET_INT interrupt. (R/W)
  
- **UART_CTS_CHG_INTENA**: The interrupt enable bit for the UARTCTS_CHG_INT interrupt.

- **UART_DSR_CHG_INTENA**: The interrupt enable bit for the UART_DSR_CHG_INT interrupt.
  - (R/W)

- **UART_RXFIFO_OVF_INTENA**: The interrupt enable bit for the UART_RXFIFO_OVF_INT interrupt. (R/W)
  
- **UART_FRM_ERR_INTENA**: The interrupt enable bit for the UART_FRM_ERR_INT interrupt.

- **UART_PARITY_ERR_INTENA**: The interrupt enable bit for the UART_PARITY_ERR_INT interrupt.
  - (R/W)

**Footer:**
Continued on the next page...
327
ESP32 TRM (Version 5.6)
Submit Documentation Feedback