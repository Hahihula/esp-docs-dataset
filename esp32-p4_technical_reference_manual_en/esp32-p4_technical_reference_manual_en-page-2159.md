
```markdown
Register 42.43. LP_UART_INT_CLR_REG (0x0010)

| Bit | Field Name                             | Description                                                                 |
|-----|-----------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                             |                                                                             |
| 30  | LP_UART_WAKEUP_INT_CLR                 | Write 1 to clear LP_UART_WAKEUP_INT. (WT)                                  |
| 29  | LP_UART_AT_CMD_CHAR_DET_INT_CLR        | Write 1 to clear LP_UART_AT_CMD_CHAR_DET_INT. (WT)                         |
| 28  | (reserved)                             |                                                                             |
| 27  | LP_UART_TX_DONE_INT_CLR                | Write 1 to clear LP_UART_TX_DONE_INT. (WT)                                 |
| 26  | LP_UART_TX_BRK_IDLE_DONE_INT_CLR       | Write 1 to clear LP_UART_TX_BRK_IDLE_DONE_INT. (WT)                        |
| 25  | LP_UART_TX_BRK_DONE_INT_CLR            | Write 1 to clear LP_UART_TX_BRK_DONE_INT. (WT)                             |
| 24  | LP_UART_GLITCH_DET_INT_CLR             | Write 1 to clear LP_UART_GLITCH_DET_INT. (WT)                              |
| 23  | LP_UART_SW_XOFF_INT_CLR                | Write 1 to clear LP_UART_SW_XOFF_INT. (WT)                                 |
| 22  | LP_UART_SW_XON_INT_CLR                 | Write 1 to clear LP_UART_SW_XON_INT. (WT)                                  |
| 21  | LP_UART_RXFIFO_TOUT_INT_CLR            | Write 1 to clear LP_UART_RXFIFO_TOUT_INT. (WT)                             |
| 20  | LP_UART_BRK_DET_INT_CLR                | Write 1 to clear LP_UART_BRK_DET_INT. (WT)                                 |
| 19  | LP_UART_CTS_CHG_INT_CLR                | Write 1 to clear LP_UART_CTS_CHG_INT. (WT)                                 |
| 18  | LP_UART_DSR_CHG_INT_CLR                | Write 1 to clear LP_UART_DSR_CHG_INT. (WT)                                 |
| 17  | LP_UART_RXFIFO_OVF_INT_CLR             | Write 1 to clear LP_UART_RXFIFO_OVF_INT. (WT)                              |
| 16  | LP_UART_FRM_ERR_INT_CLR                | Write 1 to clear LP_UART_FRM_ERR_INT. (WT)                                 |
| 15  | LP_UART_PARITY_ERR_INT_CLR             | Write 1 to clear LP_UART_PARITY_ERR_INT. (WT)                              |
| 14  | LP_UART_TXFIFO_EMPTY_INT_CLR           | Write 1 to clear LP_UART_TXFIFO_EMPTY_INT. (WT)                           |
| 13  | LP_UART_RXFIFO_FULL_INT_CLR            | Write 1 to clear LP_UART_RXFIFO_FULL_INT. (WT)                             |
```