
```markdown
Register 42.41. LP_UART_INT_ST_REG (0x0008)

| Bit | Field Name                             | Description                                                                 |
|-----|-----------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                             |                                                                             |
| 30  | LP_UART_WAKEUP_INT_ST                  | The masked interrupt status of LP_UART_WAKEUP_INT. (RO)                      |
| 29  | LP_UART_AT_CMD_CHAR_DET_INT_ST         | The masked interrupt status of LP_UART_AT_CMD_CHAR_DET_INT. (RO)             |
| 28  | (reserved)                             |                                                                             |
| 27  | LP_UART_TX_DONE_INT_ST                 | The masked interrupt status of LP_UART_TX_DONE_INT. (RO)                     |
| 26  | LP_UART_TX_BRK_DONE_INT_ST             | The masked interrupt status of LP_UART_TX_BRK_DONE_INT. (RO)                 |
| 25  | LP_UART_TX_SW_XON_INT_ST               | The masked interrupt status of LP_UART_TX_SW_XON_INT. (RO)                   |
| 24  | LP_UART_TX_SW_OFF_INT_ST               | The masked interrupt status of LP_UART_TX_SW_OFF_INT. (RO)                   |
| 23  | LP_UART_GLITCH_DET_INT_ST              | The masked interrupt status of LP_UART_GLITCH_DET_INT. (RO)                  |
| 22  | LP_UART_BRK_DET_INT_ST                 | The masked interrupt status of LP_UART_BRK_DET_INT. (RO)                     |
| 21  | LP_UART_CTS_CHG_INT_ST                 | The masked interrupt status of LP_UART_CTS_CHG_INT. (RO)                     |
| 20  | LP_UART_DSR_CHG_INT_ST                 | The masked interrupt status of LP_UART_DSR_CHG_INT. (RO)                     |
| 19  | LP_UART_RXFIFO_OVF_INT_ST              | The masked interrupt status of LP_UART_RXFIFO_OVF_INT. (RO)                  |
| 18  | LP_UART_FRM_ERR_INT_ST                 | The masked interrupt status of LP_UART_FRM_ERR_INT. (RO)                     |
| 17  | LP_UART_PARITY_ERR_INT_ST              | The masked interrupt status of LP_UART_PARITY_ERR_INT. (RO)                  |
| 16  | LP_UART_TXFIFO_EMPTY_INT_ST            | The masked interrupt status of LP_UART_TXFIFO_EMPTY_INT. (RO)                |
| 15  | LP_UART_RXFIFO_FULL_INT_ST             | The masked interrupt status of LP_UART_RXFIFO_FULL_INT. (RO)                 |
```