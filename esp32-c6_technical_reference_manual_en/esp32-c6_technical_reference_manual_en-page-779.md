
```markdown
Register 27.40. LP_UART_INT_RAW_REG (0x0004)

| Bit | Field Name                                 | Description                                                                 |
|-----|---------------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                                 |                                                                             |
| 30  | LP_UART_WAKEUP_INT_RAW                     | The raw interrupt status of LP_UART_WAKEUP_INT.                            |
| 29  | LP_UART_AT_CMD_CHAR_DET_INT_RAW            | The raw interrupt status of LP_UART_AT_CMD_CHAR_DET_INT.                   |
| 28  | (reserved)                                 |                                                                             |
| 27  | LP_UART_TX_DONE_INT_RAW                    | The raw interrupt status of LP_UART_TX_DONE_INT.                           |
| 26  | LP_UART_BRK_DONE_INT_RAW                   | The raw interrupt status of LP_UART_BRK_DONE_INT.                          |
| 25  | LP_UART_SW_XON_INT_RAW                     | The raw interrupt status of LP_UART_SW_XON_INT.                            |
| 24  | LP_UART_TX_SW_OFF_INT_RAW                  | The raw interrupt status of LP_UART_TX_SW_OFF_INT.                         |
| 23  | LP_UART_GLIITCH_DET_INT_RAW                | The raw interrupt status of LP_UART_GLITCH_DET_INT.                        |
| 22  | LP_UART_TX_BRK_DONE_INT_RAW                | The raw interrupt status of LP_UART_TX_BRK_DONE_INT.                       |
| 21  | LP_UART_TX_BRK_IDLE_DONE_INT_RAW           | The raw interrupt status of LP_UART_TX_BRK_IDLE_DONE_INT.                  |
| 20  | LP_UART_RXFIFO_FULL_INT_RAW                | The raw interrupt status of LP_UART_RXFIFO_FULL_INT. (R/WTC/SS)             |
| 19  | LP_UART_TXFIFO_EMPTY_INT_RAW               | The raw interrupt status of LP_UART_TXFIFO_EMPTY_INT. (R/WTC/SS)            |
| 18  | LP_UART_PARITY_ERR_INT_RAW                 | The raw interrupt status of LP_UART_PARITY_ERR_INT. (R/WTC/SS)              |
| 17  | LP_UART_FRM_ERR_INT_RAW                    | The raw interrupt status of LP_UART_FRM_ERR_INT. (R/WTC/SS)                 |
| 16  | LP_UART_RXFIFO_OVF_INT_RAW                 | The raw interrupt status of LP_UART_RXFIFO_OVF_INT. (R/WTC/SS)              |
| 15  | LP_UART_DSR_CHG_INT_RAW                    | The raw interrupt status of LP_UART_DSR_CHG_INT. (R/WTC/SS)                 |
| 14  | LP_UART_CTS_CHG_INT_RAW                    | The raw interrupt status of LP_UART_CTS_CHG_INT. (R/WTC/SS)                 |
| 13  | LP_UART_BRK_DET_INT_RAW                    | The raw interrupt status of LP_UART_BRK_DET_INT. (R/WTC/SS)                 |
| 12  | LP_UART_RXFIFO_TOUT_INT_RAW                | The raw interrupt status of LP_UART_RXFIFO_TOUT_INT. (R/WTC/SS)             |
| 11  | LP_UART_SW_XON_INT_RAW                     | The raw interrupt status of LP_UART_SW_XON_INT. (R/WTC/SS)                  |
| 10  | LP_UART_SW_XOFF_INT_RAW                    | The raw interrupt status of LP_UART_SW_XOFF_INT. (R/WTC/SS)                 |
| 9   | LP_UART_GLITCH_DET_INT_RAW                 | The raw interrupt status of LP_UART_GLITCH_DET_INT. (R/WTC/SS)              |
| 8   | LP_UART_TX_BRK_DONE_INT_RAW                | The raw interrupt status of LP_UART_TX_BRK_DONE_INT. (R/WTC/SS)             |
| 7   | LP_UART_TX_BRK_IDLE_DONE_INT_RAW           | The raw interrupt status of LP_UART_TX_BRK_IDLE_DONE_INT. (R/WTC/SS)        |
| 6-0 | Reset                                      | All bits reset to 0                                                         |

Continued on the next page...
```