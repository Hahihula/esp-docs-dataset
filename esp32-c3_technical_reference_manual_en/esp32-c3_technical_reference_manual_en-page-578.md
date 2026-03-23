
```markdown
Register 26.6. UART_INT_CLR_REG (0x0010)

| Bit | Field Name                             | Description                                                                 |
|-----|-----------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                             |                                                                             |
| 30  | UART_WAKEUP_INT_CLR                    | Set this bit to clear the UART_THE_RXFIFO_FULL_INT interrupt. (WT)           |
| 29  | UART_AT_CMD_CHAR_INT_CLR               | Set this bit to clear the UART_TXFIFO_EMPTY_INT interrupt. (WT)              |
| 28  | UART_RS485_CLASH_INT_CLR               | Set this bit to clear the UART_PARITY_ERR_INT interrupt. (WT)                |
| 27  | UART_RS485_FRM_ERR_INT_CLR             | Set this bit to clear the UART_FRM_ERR_INT interrupt. (WT)                   |
| 26  | UART_TX_PARTY_DONE_INT_CLR             | Set this bit to clear the UART_RXFIFO_OVF_INT interrupt. (WT)                |
| 25  | UART_TX_BRK_IDLE_DONE_INT_CLR          | Set this bit to clear the UART_DSR_CHG_INT interrupt. (WT)                   |
| 24  | UART_SW_XON_INT_CLR                    | Set this bit to clear the UART_CTS_CHG_INT interrupt. (WT)                   |
| 23  | UART_BRK_DET_INT_CLR                   | Set this bit to clear the UART_BRK_DET_INT interrupt. (WT)                   |
| 22  | UART_RXFIFO_TOUT_INT_CLR               | Set this bit to clear the UART_RXFIFO_TOUT_INT interrupt. (WT)               |
| 21  | UART_SW_XOFF_INT_CLR                   | Set this bit to clear the UART_SW_XON_INT interrupt. (WT)                    |
| 20  | UART_GLITCH_DET_INT_CLR                | Set this bit to clear the UART_SW_XOFF_INT interrupt. (WT)                   |
| 19  | UART_TX_BRK_DONE_INT_CLR               | Set this bit to clear the UART_GLITCH_DET_INT interrupt. (WT)                |
| 18  | UART_TX_BRK_IDLE_DONE_INT_CLR          | Set this bit to clear the UART_TX_BRK_DONE_INT interrupt. (WT)               |
| 17  | UART_TX_DONE_INT_CLR                   | Set this bit to clear the UART_TX_BRK_IDLE_DONE_INT interrupt. (WT)          |
| 16  | UART_RS485_PARITY_ERR_INT_CLR          | Set this bit to clear the UART_TX_DONE_INT interrupt. (WT)                    |
```