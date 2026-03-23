

```markdown
Register 26.3. UART_INT_RAW_REG (0x0004)

| Bit | Field Name                     | Description                                                                                                                                                                                                 |
|-----|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 31  |                                 | (reserved)                                                                                                                                                                                                |
| 30  | UART_WAKE_UP_INT_RAW            | This interrupt raw bit turns to high level when the receiver receives more data than what UART_RXFIFO_FULL_THRDH specifies. (R/WTC/SS)                                                                         |
| 29  | UART_AT_CMD_CHAR_DET_INT_RAW    | This interrupt raw bit turns to high level when the amount of data in TX FIFO is less than what UART_TXFIFO_EMPTY_THRDH specifies. (R/WTC/SS)                                                                     |
| 28  | UART_RS485_CLASH_INT_RAW        | This interrupt raw bit turns to high level when the receiver detects a parity error in the data. (R/WTC/SS)                                                                                                      |
| 27  | UART_RS485_FRM_ERR_INT_RAW      | This interrupt raw bit turns to high level when the receiver receives more data than the capacity of RX FIFO. (R/WTC/SS)                                                                                        |
| 26  | UART_TX_DONE_INT_RAW            | This interrupt raw bit turns to high level when the receiver detects a data frame error. (R/WTC/SS)                                                                                                             |
| 25  | UART_DSR_CHG_INT_RAW            | This interrupt raw bit turns to high level when the receiver receives more data than what UART_RXFIFO_FULL_THRDH specifies. (R/WTC/SS)                                                                         |
| 24  | UART_GITX_DET_INT_RAW           | This interrupt raw bit turns to high level when the receiver detects an edge change of DSRn signal. (R/WTC/SS)                                                                                                    |
| 23  | UART_SW_XON_INT_RAW             | This interrupt raw bit turns to high level when the receiver receives an XON character and UART_SW_FLOW_CON_EN is set to 1. (R/WTC/SS)                                                                          |
| 22  | UART_SW_XOFF_INT_RAW            | This interrupt raw bit turns to high level when the receiver receives an XOFF character and UART_SW_FLOW_CON_EN is set to 1. (R/WTC/SS)                                                                         |
| 21  | UART_GLITCH_DET_INT_RAW         | This interrupt raw bit turns to high level when the receiver detects a glitch in the middle of a start bit. (R/WTC/SS)                                                                                          |

UART_RXFIFO_FULL_INT_RAW
This interrupt raw bit turns to high level when the receiver receives more data than what UART_RXFIFO_FULL_THRDH specifies. (R/WTC/SS)

UART_TXFIFO_EMPTY_INT_RAW
This interrupt raw bit turns to high level when the amount of data in TX FIFO is less than what UART_TXFIFO_EMPTY_THRDH specifies. (R/WTC/SS)

UART_PARITY_ERR_INT_RAW
This interrupt raw bit turns to high level when the receiver detects a parity error in the data. (R/WTC/SS)

UART_FRM_ERR_INT_RAW
This interrupt raw bit turns to high level when the receiver detects a data frame error. (R/WTC/SS)

UART_RXFIFO_OVF_INT_RAW
This interrupt raw bit turns to high level when the receiver receives more data than the capacity of RX FIFO. (R/WTC/SS)

UART_DSR_CHG_INT_RAW
This interrupt raw bit turns to high level when the receiver detects the edge change of DSRn signal. (R/WTC/SS)

UART_CTS_CHG_INT_RAW
This interrupt raw bit turns to high level when the receiver detects the edge change of CTSn signal. (R/WTC/SS)

UART_BRK_DET_INT_RAW
This interrupt raw bit turns to high level when the receiver detects a 0 after the stop bit. (R/WTC/SS)

UART_RXFIFO_TOUT_INT_RAW
This interrupt raw bit turns to high level when the receiver takes more time than UART_RX_TOUT_THRDH to receive a byte. (R/WTC/SS)

UART_SW_XON_INT_RAW
This interrupt raw bit turns to high level when the receiver receives an XON character and UART_SW_FLOW_CON_EN is set to 1. (R/WTC/SS)

UART_SW_XOFF_INT_RAW
This interrupt raw bit turns to high level when the receiver receives an XOFF character and UART_SW_FLOW_CON_EN is set to 1. (R/WTC/SS)

UART_GLITCH_DET_INT_RAW
This interrupt raw bit turns to high level when the receiver detects a glitch in the middle of a start bit. (R/WTC/SS)
```