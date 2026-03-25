
```markdown
Register 28.6. UART_INT_CLR_REG (0x0010)

| Bit | Field Name                     | Description                                                                 |
|-----|---------------------------------|-----------------------------------------------------------------------------|
| 31  | reserved                       |                                                                             |
| 30  | UART_WAKEUP_INT_CLR            | Write 1 to clear UART_WAKEUP_INT. (WT)                                     |
| 29  | UART_AT_CMD_CHAR_DET_INT_CLR   | Write 1 to clear UART_AT_CMD_CHAR_DET_INT. (WT)                            |
| 28  | UART_RS485_CLASH_INT_CLR       | Write 1 to clear UART_RS485_CLASH_INT. (WT)                                |
| 27  | UART_RS485_FRM_ERR_INT_CLR     | Write 1 to clear UART_RS485_FRM_ERR_INT. (WT)                              |
| 26  | UART_RS485_PARITY_ERR_INT_CLR  | Write 1 to clear UART_RS485_PARITY_ERR_INT. (WT)                           |
| 25  | UART_TX_DONE_INT_CLR           | Write 1 to clear UART_TX_DONE_INT. (WT)                                    |
| 24  | UART_TX_BRK_IDLE_DONE_INT_CLR  | Write 1 to clear UART_TX_BRK_IDLE_DONE_INT. (WT)                           |
| 23  | UART_TX_BRK_DONE_INT_CLR       | Write 1 to clear UART_TX_BRK_DONE_INT. (WT)                                |
| 22  | UART_SW_XOFF_INT_CLR           | Write 1 to clear UART_SW_XOFF_INT. (WT)                                    |
| 21  | UART_SW_XON_INT_CLR            | Write 1 to clear UART_SW_XON_INT. (WT)                                     |
| 20  | UART_RXFIFO_TOUT_INT_CLR       | Write 1 to clear UART_RXFIFO_TOUT_INT. (WT)                                |
| 19  | UART_BRK_DET_INT_CLR           | Write 1 to clear UART_BRK_DET_INT. (WT)                                    |
| 18  | UART_CTS_CHG_INT_CLR           | Write 1 to clear UART_CTS_CHG_INT. (WT)                                    |
| 17  | UART_DSR_CHG_INT_CLR           | Write 1 to clear UART_DSR_CHG_INT. (WT)                                    |
| 16  | UART_RXFIFO_OVF_INT_CLR        | Write 1 to clear UART_RXFIFO_OVF_INT. (WT)                                 |
| 15  | UART_FRM_ERR_INT_CLR           | Write 1 to clear UART_FRM_ERR_INT. (WT)                                    |
| 14  | UART_PARITY_ERR_INT_CLR        | Write 1 to clear UART_PARITY_ERR_INT. (WT)                                 |
| 13  | UART_TXFIFO_EMPTY_INT_CLR      | Write 1 to clear UART_TXFIFO_EMPTY_INT. (WT)                               |
| 12  | UART_RXFIFO_FULL_INT_CLR       | Write 1 to clear UART_RXFIFO_FULL_INT. (WT)                                |

```