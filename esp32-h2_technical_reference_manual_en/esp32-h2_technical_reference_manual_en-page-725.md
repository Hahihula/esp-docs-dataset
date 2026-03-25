
```markdown
Register 28.5. UART_INT_ENA_REG (0x000C)

| Bit | Name                                 | Description                                                                 |
|-----|---------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                           |                                                                             |
| 30  | UART_WAKEUP_INT_ENA                  | Write 1 to enable UART_WAKEUP_INT. (R/W)                                   |
| 29  | UART_RS485_CLASH_INT_ENA             | Write 1 to enable UART_RS485_CLASH_INT. (R/W)                               |
| 28  | UART_RS485_FRM_ERR_INT_ENA           | Write 1 to enable UART_RS485_FRM_ERR_INT. (R/W)                             |
| 27  | UART_RS485_PARITY_ERR_INT_ENA        | Write 1 to enable UART_RS485_PARITY_ERR_INT. (R/W)                         |
| 26  | UART_TX_DONE_INT_ENA                 | Write 1 to enable UART_TX_DONE_INT. (R/W)                                   |
| 25  | UART_TX_BRK_IDLE_DONE_INT_ENA        | Write 1 to enable UART_TX_BRK_IDLE_DONE_INT. (R/W)                         |
| 24  | UART_TX_BRK_DONE_INT_ENA             | Write 1 to enable UART_TX_BRK_DONE_INT. (R/W)                               |
| 23  | UART_GLITCH_DET_INT_ENA              | Write 1 to enable UART_GLITCH_DET_INT. (R/W)                                |
| 22  | UART_SW_XOFF_INT_ENA                 | Write 1 to enable UART_SW_XOFF_INT. (R/W)                                   |
| 21  | UART_SW_XON_INT_ENA                  | Write 1 to enable UART_SW_XON_INT. (R/W)                                    |
| 20  | UART_RXFIFO_TOUT_INT_ENA             | Write 1 to enable UART_RXFIFO_TOUT_INT. (R/W)                               |
| 19  | UART_BRK_DET_INT_ENA                 | Write 1 to enable UART_BRK_DET_INT. (R/W)                                   |
| 18  | UART_CTS_CHG_INT_ENA                 | Write 1 to enable UART_CTS_CHG_INT. (R/W)                                   |
| 17  | UART_DSR_CHG_INT_ENA                 | Write 1 to enable UART_DSR_CHG_INT. (R/W)                                   |
| 16  | UART_RXFIFO_OVF_INT_ENA              | Write 1 to enable UART_RXFIFO_OVF_INT. (R/W)                                |
| 15  | UART_FRM_ERR_INT_ENA                 | Write 1 to enable UART_FRM_ERR_INT. (R/W)                                   |
| 14  | UART_PARITY_ERR_INT_ENA              | Write 1 to enable UART_PARITY_ERR_INT. (R/W)                               |
| 13  | UART_TXFIFO_EMPTY_INT_ENA            | Write 1 to enable UART_TXFIFO_EMPTY_INT. (R/W)                             |
| 12  | UART_RXFIFO_FULL_INT_ENA             | Write 1 to enable UART_RXFIFO_FULL_INT. (R/W)                               |

```