
```markdown
Register 27.4. UART_INT_ST_REG (0x0008)

| Bit | Field Name                             | Description                                                                 |
|-----|-----------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                             |                                                                             |
| 30  | UART_WAKEUP_INT_ST                     | The masked interrupt status of UART_WAKEUP_INT. (RO)                         |
| 29  | UART_AT_CMD_CHAR_DET_INT_ST            | The masked interrupt status of UART_AT_CMD_CHAR_DET_INT. (RO)                |
| 28  | UART_RS485_CLASH_INT_ST                | The masked interrupt status of UART_RS485_CLASH_INT. (RO)                    |
| 27  | UART_RS485_FRM_ERR_INT_ST              | The masked interrupt status of UART_RS485_FRM_ERR_INT. (RO)                  |
| 26  | UART_RS485_PARITY_ERR_INT_ST           | The masked interrupt status of UART_RS485_PARITY_ERR_INT. (RO)               |
| 25  | UART_TX_DONE_INT_ST                    | The masked interrupt status of UART_TX_DONE_INT. (RO)                        |
| 24  | UART_TX_BRK_IDLE_DONE_INT_ST           | The masked interrupt status of UART_TX_BRK_IDLE_DONE_INT. (RO)               |
| 23  | UART_SW_XON_INT_ST                     | The masked interrupt status of UART_SW_XON_INT. (RO)                         |
| 22  | UART_SW_XOFF_INT_ST                    | The masked interrupt status of UART_SW_XOFF_INT. (RO)                        |
| 21  | UART_GLITCH_DET_INT_ST                 | The masked interrupt status of UART_GLITCH_DET_INT. (RO)                     |
| 20  | UART_TXFIFO_TOUT_INT_ST                | The masked interrupt status of UART_RXFIFO_TOUT_INT. (RO)                     |
| 19  | UART_BRK_DET_INT_ST                    | The masked interrupt status of UART_BRK_DET_INT. (RO)                        |
| 18  | UART_CTS_CHG_INT_ST                    | The masked interrupt status of UART_CTS_CHG_INT. (RO)                        |
| 17  | UART_DSR_CHG_INT_ST                    | The masked interrupt status of UART_DSR_CHG_INT. (RO)                        |
| 16  | UART_RXFIFO_OVF_INT_ST                 | The masked interrupt status of UART_RXFIFO_OVF_INT. (RO)                     |
| 15  | UART_FRM_ERR_INT_ST                    | The masked interrupt status of UART_FRM_ERR_INT. (RO)                        |
| 14  | UART_PARITY_ERR_INT_ST                 | The masked interrupt status of UART_PARITY_ERR_INT. (RO)                     |
| 13  | UART_TXFIFO_EMPTY_INT_ST               | The masked interrupt status of UART_TXFIFO_EMPTY_INT. (RO)                   |
| 12  | UART_RXFIFO_FULL_INT_ST                | The masked interrupt status of UART_RXFIFO_FULL_INT. (RO)                     |
| 11  | UART_TX_BRK_DONE_INT_ST                | The masked interrupt status of UART_TX_TX_BRK_DONE_INT. (RO)                 |
| 10  | UART_GLITCH_SW_OFF_INT_ST              | The masked interrupt status of UART_GLITCH_SW_OFF_INT. (RO)                  |
| 9   | UART_TX_BRK_DET_INT_ST                 | The masked interrupt status of UART_TX_BRK_DET_INT. (RO)                     |
| 8   | UART_RXFIFO_OVF_DET_INT_ST             | The masked interrupt status of UART_RXFIFO_OVF_DET_INT. (RO)                 |
| 7   | UART_RXFIFO_EMPTY_DET_INT_ST           | The masked interrupt status of UART_RXFIFO_EMPTY_DET_INT. (RO)               |
| 6   | UART_TXFIFO_FULL_DET_INT_ST            | The masked interrupt status of UART_TXFIFO_FULL_DET_INT. (RO)                |
| 5   | UART_DTR_CHG_INT_ST                    | The masked interrupt status of UART_DTR_CHG_INT. (RO)                        |
| 4   | UART_RTS_CHG_INT_ST                    | The masked interrupt status of UART_RTS_CHG_INT. (RO)                        |
| 3   | UART_CTS_DET_INT_ST                    | The masked interrupt status of UART_CTS_DET_INT. (RO)                        |
| 2   | UART_DSR_DET_INT_ST                    | The masked interrupt status of UART_DSR_DET_INT. (RO)                        |
| 1   | UART_RXFIFO_OVF_DET_INT_ST             | The masked interrupt status of UART_RXFIFO_OVF_DET_INT. (RO)                 |
| 0   | Reset                                  |                                                                             |
```