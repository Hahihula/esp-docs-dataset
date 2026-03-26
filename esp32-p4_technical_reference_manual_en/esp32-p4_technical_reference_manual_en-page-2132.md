

```markdown
Register 42.3. UART_INT_RAW_REG (0x0004)

| Bit | Field Name                                 | Description                                                                 |
|-----|---------------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                                 |                                                                             |
| 30  | UART_WAKE_UP_INT_RAW                       | The raw interrupt status of UART_WAKE_UP_INT.                               |
| 29  | UART_AT_CMD_CHAR_INT_RAW                   | The raw interrupt status of UART_AT_CMD_CHAR_INT.                           |
| 28  | UART_CLASH_INT_RAW                         | The raw interrupt status of UART_CLASH_INT.                                 |
| 27  | UART_RS485_ERR_INT_RAW                     | The raw interrupt status of UART_RS485_ERR_INT.                             |
| 26  | UART_RS485_PARITY_ERR_INT_RAW              | The raw interrupt status of UART_RS485_PARITY_ERR_INT.                      |
| 25  | UART_TX_BRK_DONE_INT_RAW                   | The raw interrupt status of UART_TX_BRK_DONE_INT.                           |
| 24  | UART_SW_XOFF_INT_RAW                       | The raw interrupt status of UART_SW_XOFF_INT.                               |
| 23  | UART_GLITCH_DET_INT_RAW                    | The raw interrupt status of UART_GLITCH_DET_INT.                            |
| 22  | UART_TX_BRK_IDLE_DONE_INT_RAW              | The raw interrupt status of UART_TX_BRK_IDLE_DONE_INT.                      |
| 21  | UART_TX_DONE_INT_RAW                       | The raw interrupt status of UART_TX_DONE_INT.                               |
| 20  | UART_RS485_PARITY_ERR_INT_RAW              | The raw interrupt status of UART_RS485_PARITY_ERR_INT.                      |
| 19  | UART_RS485_FRM_ERR_INT_RAW                 | The raw interrupt status of UART_RS485_FRM_ERR_INT.                         |
| 18  | UART_TX_TOUT_INT_RAW                       | The raw interrupt status of UART_TX_TOUT_INT.                               |
| 17  | UART_BRK_DET_INT_RAW                       | The raw interrupt status of UART_BRK_DET_INT.                               |
| 16  | UART_CTS_CHG_INT_RAW                       | The raw interrupt status of UART_CTS_CHG_INT.                               |
| 15  | UART_DSR_CHG_INT_RAW                       | The raw interrupt status of UART_DSR_CHG_INT.                               |
| 14  | UART_RXFIFO_OVF_INT_RAW                    | The raw interrupt status of UART_RXFIFO_OVF_INT.                            |
| 13  | UART_FRM_ERR_INT_RAW                       | The raw interrupt status of UART_FRM_ERR_INT.                               |
| 12  | UART_PARITY_ERR_INT_RAW                    | The raw interrupt status of UART_PARITY_ERR_INT.                            |
| 11  | UART_TXEmpty_INT_RAW                       | The raw interrupt status of UART_TXEmpty_INT.                               |
| 10  | UART_RXFIFO_FULL_INT_RAW                   | The raw interrupt status of UART_RXFIFO_FULL_INT.                           |
```