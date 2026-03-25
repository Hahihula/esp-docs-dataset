
```markdown
Register 28.3. UART_INT_RAW_REG (0x0004)

| Bit | Field Name                             | Description                                                                 |
|-----|-----------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                             |                                                                             |
| 30  | UART_WAKE_UP_INT_RAW_DET_INT_RAW       | The raw interrupt status of UART_WAKE_UP_INT_RAW.                           |
| 29  | UART_AT_CMD_CLASH_INT_RAW              | The raw interrupt status of UART_AT_CMD_CLASH_INT_RAW.                      |
| 28  | UART_RS485_ERR_INT_RAW                 | The raw interrupt status of UART_RS485_ERR_INT_RAW.                         |
| 27  | UART_RS485_PARITY_ERR_INT_RAW          | The raw interrupt status of UART_RS485_PARITY_ERR_INT_RAW.                  |
| 26  | UART_TX_BRK_DONE_INT_RAW               | The raw interrupt status of UART_TX_BRK_DONE_INT_RAW.                       |
| 25  | UART_TX_IDLE_DONE_INT_RAW              | The raw interrupt status of UART_TX_IDLE_DONE_INT_RAW.                      |
| 24  | UART_SW_XON_INT_RAW                    | The raw interrupt status of UART_SW_XON_INT_RAW.                            |
| 23  | UART_SW_OFF_INT_RAW                    | The raw interrupt status of UART_SW_OFF_INT_RAW.                            |
| 22  | UART_GLITCH_DET_INT_RAW                | The raw interrupt status of UART_GLITCH_DET_INT_RAW.                        |
| 21  | UART_TX_BRK_DONE_INT_RAW               | The raw interrupt status of UART_TX_BRK_DONE_INT_RAW.                       |
| 20  | UART_TX_BRK_IDLE_DONE_INT_RAW          | The raw interrupt status of UART_TX_BRK_IDLE_DONE_INT_RAW.                  |
| 19  | UART_TX_DONE_INT_RAW                   | The raw interrupt status of UART_TX_DONE_INT_RAW.                           |
| 18  | UART_RS485_PARITY_ERR_INT_RAW          | The raw interrupt status of UART_RS485_PARITY_ERR_INT_RAW.                  |
| 17  | UART_RS485_FRM_ERR_INT_RAW             | The raw interrupt status of UART_RS485_FRM_ERR_INT_RAW.                     |
| 16  | UART_TX_TOUT_INT_RAW                   | The raw interrupt status of UART_TX_TOUT_INT_RAW.                           |
| 15  | UART_RXFIFO_OVF_INT_RAW                | The raw interrupt status of UART_RXFIFO_OVF_INT_RAW.                        |
| 14  | UART_DSR_CHG_INT_RAW                   | The raw interrupt status of UART_DSR_CHG_INT_RAW.                           |
| 13  | UART_CTS_CHG_INT_RAW                   | The raw interrupt status of UART_CTS_CHG_INT_RAW.                           |
| 12  | UART_BRK_DET_INT_RAW                   | The raw interrupt status of UART_BRK_DET_INT_RAW.                           |
| 11  | UART_RXFIFO_TOUT_INT_RAW               | The raw interrupt status of UART_RXFIFO_TOUT_INT_RAW.                       |
| 10  | UART_SW_XON_INT_RAW                    | The raw interrupt status of UART_SW_XON_INT_RAW.                            |
| 9   | UART_SW_OFF_INT_RAW                    | The raw interrupt status of UART_SW_OFF_INT_RAW.                            |
| 8   | UART_GLITCH_DET_INT_RAW                | The raw interrupt status of UART_GLITCH_DET_INT_RAW.                        |
| 7   | UART_TX_BRK_DONE_INT_RAW               | The raw interrupt status of UART_TX_BRK_DONE_INT_RAW.                       |
| 6   | UART_TX_BRK_IDLE_DONE_INT_RAW          | The raw interrupt status of UART_TX_BRK_IDLE_DONE_INT_RAW.                  |
| 5   | UART_TX_DONE_INT_RAW                   | The raw interrupt status of UART_TX_DONE_INT_RAW.                           |
| 4   | UART_RS485_PARITY_ERR_INT_RAW          | The raw interrupt status of UART_RS485_PARITY_ERR_INT_RAW.                  |
| 3   | UART_RS485_FRM_ERR_INT_RAW             | The raw interrupt status of UART_RS485_FRM_ERR_INT_RAW.                     |
| 2   | UART_TX_TOUT_INT_RAW                   | The raw interrupt status of UART_TX_TOUT_INT_RAW.                           |
| 1   | UART_RXFIFO_OVF_INT_RAW                | The raw interrupt status of UART_RXFIFO_OVF_INT_RAW.                        |
| 0   | UART_DSR_CHG_INT_RAW                   | The raw interrupt status of UART_DSR_CHG_INT_RAW.                           |

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
UART_SW_OFF_INT_RAW The raw interrupt status of UART_SW_OFF_INT. (R/WTC/SS)
UART_GLITCH_DET_INT_RAW The raw interrupt status of UART_GLITCH_DET_INT. (R/WTC/SS)
UART_TX_BRK_DONE_INT_RAW The raw interrupt status of UART_TX_BRK_DONE_INT. (R/WTC/SS)

UART_TX_BRK_IDLE_DONE_INT_RAW The raw interrupt status of UART_TX_BRK_IDLE_DONE_INT. (R/WTC/SS)
UART_TX_DONE_INT_RAW The raw interrupt status of UART_TX_DONE_INT. (R/WTC/SS)
UART_RS485_PARITY_ERR_INT_RAW The raw interrupt status of UART_RS485_PARITY_ERR_INT. (R/WTC/SS)
UART_RS485_FRM_ERR_INT_RAW The raw interrupt status of UART_RS485_FRM_ERR_INT. (R/WTC/SS)

Continued on the next page...
```