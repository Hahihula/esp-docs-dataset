

```markdown
Register 32.3. UART_INT_RAW_REG (0x0004)

| Bit | Field Name                                 | Description                                                                 |
|-----|---------------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                                 |                                                                             |
| 30  | UART_WAKE_UP_INT_RAW                       | The raw interrupt status of UART_WAKE_UP_INT.                               |
| 29  | UART_AT_CMD_CHAR_INT_RAW                   | The raw interrupt status of UART_AT_CMD_CHAR_INT.                           |
| 28  | UART_CLASH_INT_RAW                         | The raw interrupt status of UART_CLASH_INT.                                 |
| 27  | UART_RS485_ERR_INT_RAW                     | The raw interrupt status of UART_RS485_ERR_INT.                             |
| 26  | UART_RS485_PARITY_ERR_INT_RAW              | The raw interrupt status of UART_RS485_PARITY_ERR_INT.                      |
| 25  | UART_TX_DONE_INT_RAW                       | The raw interrupt status of UART_TX_DONE_INT.                               |
| 24  | UART_BRK_IDLE_DONE_INT_RAW                 | The raw interrupt status of UART_BRK_IDLE_DONE_INT.                         |
| 23  | UART_SW_XOFF_INT_RAW                       | The raw interrupt status of UART_SW_XOFF_INT.                               |
| 22  | UART_TX_BRK_DET_INT_RAW                    | The raw interrupt status of UART_TX_BRK_DET_INT.                            |
| 21  | UART_CTS_CHG_INT_RAW                       | The raw interrupt status of UART_CTS_CHG_INT.                               |
| 20  | UART_DSR_CHG_INT_RAW                       | The raw interrupt status of UART_DSR_CHG_INT.                               |
| 19  | UART_RXFIFO_OVF_INT_RAW                    | The raw interrupt status of UART_RXFIFO_OVF_INT.                            |
| 18  | UART_FRM_ERR_INT_RAW                       | The raw interrupt status of UART_FRM_ERR_INT.                               |
| 17  | UART_PARITY_ERR_INT_RAW                    | The raw interrupt status of UART_PARITY_ERR_INT.                            |
| 16  | UART_RXFIFO_EMPTY_INT_RAW                  | The raw interrupt status of UART_RXFIFO_EMPTY_INT.                          |
| 15  | UART_TXFIFO_FULL_INT_RAW                   | The raw interrupt status of UART_TXFIFO_FULL_INT.                           |
| 14  | UART_SW_XON_INT_RAW                        | The raw interrupt status of UART_SW_XON_INT.                                |
| 13  | UART_GLITCH_DET_INT_RAW                    | The raw interrupt status of UART_GLITCH_DET_INT.                            |
| 12  | UART_TX_DONE_INT_RAW                       | The raw interrupt status of UART_TX_DONE_INT.                               |
| 11  | UART_TX_BRK_DONE_INT_RAW                   | The raw interrupt status of UART_TX_BRK_DONE_INT.                           |
| 10  | UART_RXFIFO_TOUT_INT_RAW                   | The raw interrupt status of UART_RXFIFO_TOUT_INT.                           |
| 9   | UART_BRK_DET_INT_RAW                       | The raw interrupt status of UART_BRK_DET_INT.                               |
| 8   | UART_CTS_CHG_INT_RAW                       | The raw interrupt status of UART_CTS_CHG_INT.                               |
| 7   | UART_DSR_CHG_INT_RAW                       | The raw interrupt status of UART_DSR_CHG_INT.                               |
| 6   | UART_RXFIFO_OVF_INT_RAW                    | The raw interrupt status of UART_RXFIFO_OVF_INT.                            |
| 5   | UART_FRM_ERR_INT_RAW                       | The raw interrupt status of UART_FRM_ERR_INT.                               |
| 4   | UART_PARITY_ERR_INT_RAW                    | The raw interrupt status of UART_PARITY_ERR_INT.                            |
| 3   | UART_RXFIFO_EMPTY_INT_RAW                  | The raw interrupt status of UART_RXFIFO_EMPTY_INT.                          |
| 2   | UART_TXFIFO_FULL_INT_RAW                   | The raw interrupt status of UART_TXFIFO_FULL_INT.                           |
| 1   | UART_SW_XOFF_INT_RAW                       | The raw interrupt status of UART_SW_XOFF_INT.                               |
| 0   | UART_SW_XON_INT_RAW                        | The raw interrupt status of UART_SW_XON_INT.                                |

UART_RXFIFO_FULL_INT_RAW The raw interrupt status of UART_RXFIFO_FULL_INT. (R/WTC/SS)
UART_TXFIFO_EMPTY_INT_RAW The raw interrupt status of UART_TXFIFO_EMPTY_INT. (R/WTC/SS)

UART_PARITY_ERR_INT_RAW The raw interrupt status of UART_PARITY_ERR_INT. (R/WTC/SS)
UART_FRM_ERR_INT_RAW The raw interrupt status of UART_FRM_ERR_INT. (R/WTC/SS)
UART_RXFIFO_OVF_INT_RAW The raw interrupt status of UART_RXFIFO_OVF_INT. (R/WTC/SS)
UART_DSR_CHG_INT_RAW The raw interrupt status of UART_DSR_CHG_INT. (R/WTC/SS)
UART_CTS_CHG_INT_RAW The raw interrupt status of UART_CTS_CHG_INT. (R/WTC/SS)
UART_BRK_DET_INT_RAW The raw interrupt status of UART_BRK_DET_INT. (R/WTC/SS)
UART_RXFIFO_TOUT_INT_RAW The raw interrupt status of UART_RXFIFO_TOUT_INT. (R/WTC/SS)
UART_SW_XON_INT_RAW The raw interrupt status of UART_SW_XON_INT. (R/WTC/SS)
UART_SW_XOFF_INT_RAW UART_SW_XOFF_INT. (R/WTC/SS)
UART_GLITCH_DET_INT_RAW The raw interrupt status of UART_GLITCH_DET_INT. (R/WTC/SS)
UART_TX_BRK_DONE_INT_RAW The raw interrupt status of UART_TX_BRK_DONE_INT. (R/WTC/SS)

UART_TX_BRK_IDLE_DONE_INT_RAW The raw interrupt status of UART_TX_BRK_IDLE_DONE_INT. (R/WTC/SS)
UART_TX_DONE_INT_RAW The raw interrupt status of UART_TX_DONE_INT. (R/WTC/SS)
UART_RS485_PARITY_ERR_INT_RAW The raw interrupt status of UART_RS485_PARITY_ERR_INT. (R/WTC/SS)
UART_RS485_FRM_ERR_INT_RAW The raw interrupt status of UART_RS485_FRM_ERR_INT. (R/WTC/SS)

Continued on the next page...
```