Title: Chapter 19 UART Controller (UART)

Subtitle: Register 19.5. UART_INT_CLR_REG (0x10)

Menu/Navigation Link:
- GoBack

Table Description and Content:

| Bit Number | Name                          |
|------------|-------------------------------|
| 31         | UART_AT_CMD_CHAR_DET_INL_CLR  |
| 20 - 18    | UART_RS485_CLASH_INT_INL_CLR |
| 19 - 17    | UART_RS485_FRM_ERR_INL_CLR   |
| 16 - 15    | UART_RS485_PARITY_ERR_INL_CLR|
| 14         | UART_TX_BRK_DET_INL_CLR      |
| 13         | UART_TX_OVR_DET_INL_CLR      |
| 12         | UART_RXFIFO_DET_INL_CLR      |
| 11 - 9     | UART_TX_FIF0_DET_INL_CLR     |
| 8          | UART_RXFIFO_OVF_DET_INL_CLR  |
| 7          | UART_TXOVERT_DET_INL_CLR     |
| 6          | UART_RXFIFO_ERR_DET_INL_CLR  |
| 5 - 4      | UART_TX_FIFO_DET_INL_CLR      |
| 3          | UART_TXOVERR_DET_INL_CLR      |
| 2          | UART_RXFIFO_OVF_DET_INL_CLR  |
| 1          | UART_RXFIFO_ERR_DET_INL_CLR  |
| 0          | UART_RXFIFO_DET_INL_CLR       |

Text Content:

- **UART_AT_CMD_CHAR_DET_INL_CLR**: Set this bit to clear the UART_AT_CMD_CHAR_DET_INT interrupt. (WO)
  
- **UART_RS485_CLASH_INT_INL_CLR**: Set this bit to clear the UART_RS485_CLASH_INT interrupt. (WO)

- **UART_RS485_FRM_ERR_INL_CLR**: Set this bit to clear the UART_RS485_FRM_ERR_INT interrupt. (WO)

- **UART_RS485_PARITY_ERR_INL_CLR**: Set this bit to clear the UART_RS485_PARITY_ERR_INT interrupt. (WO)

- **UART_TX DONE INT CLR**: Set this bit to clear the UART_TX_DONE_INT interrupt. (WO)

- **UART_TX BRK IDLE DONE INT_CLR**: Set this bit to clear the UART_TX_BRK_IDLEDone_INT interrupt. (WO)

- **UART_TX BRK DONE INT_CLR**: Set this bit to clear the UART_TX_BRK_DONE_INT interrupt. (WO)

- **UART_GLITCH_DET_INL_CLR**: Set this bit to clear the UART_GLITCH_DET_INT interrupt. (WO)

- **UART_SW_XOFF_INT_CLR**: Set this bit to clear the UART_SW_XOFF_INT interrupt. (WO)

- **UART_SW_XON_INT_CLR**: Set this bit to clear the UART_SW_XON_INT interrupt. (WO)

- **UART_RXFIFO_TOUT_INT_CLR**: Set this bit to clear the UART_RXFIFO_TOUT_INT interrupt. This bit can be set only when both rxfifo_cnt and rx_mem_cnt are 0. (WO)

- **UART_BRK_DET_INL_CLR**: Set this bit to clear the UART_BRK_DET_INT interrupt. (WO)

- **UART_CTS_CHG_INT_CLR**: Set this bit to clear the UARTCTS_CHG_INT interrupt. (WO)

- **UART_DSR_CHG_INT_CLR**: Set this bit to clear the UART_DSR_CHG_INT interrupt. (WO)

- **UART_RXFIFO_OVF_INL_CLR**: Set this bit to clear the UART_RXFIFO_OVF_INT interrupt. (WO)

- **UART_FRM_ERR_INL_CLR**: Set this bit to clear the UART_FRM_ERR_INT interrupt. (WO)

- **UART_PARITY_ERR_INL_CLR**: Set this bit to clear the UART_PARITY_ERR_INT interrupt. (WO)

- **UART_TXFIFO_EMPTY_INL_CLR**: Set this bit to clear the UART_TXFIFO_EMPTY_INT interrupt. (WO)

- **UART_RXFIFO_FULL_INL_CLR**: Set this bit to clear the UART_RXFIFO_FULL_INT interrupt. This bit can be set only when data in Rx_FIFO is less than UART_RXFIFO_FULLTHRHD. (WO)

Footer:
- Espresso Systems
- Page number: 329
- Document version and submission information link text "Submit Documentation Feedback" with ESP32 TRM (Version 5.6)