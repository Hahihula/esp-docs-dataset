

```markdown
Register 26.5. UART_INT_ENA_REG (0x000C)

| Bit | Name                                 | Description                                                                 |
|-----|---------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                           |                                                                             |
| 30  | UART_WAKEUP_INT_ENA                  | This is the enable bit for UART_WAKEUP_INT. (R/W)                            |
| 29  | UART_AT_CMD_CHAR_DET_INT_ENA         | This is the enable bit for UART_AT_CMD_CHAR_DET_INT. (R/W)                   |
| 28  | UART_RS485_CLASH_INT_ENA             | This is the enable bit for UART_RS485_CLASH_INT. (R/W)                       |
| 27  | UART_ERR_INT_ENA                     | This is the enable bit for UART_ERR_INT. (R/W)                               |
| 26  | UART_TX_DONE_INT_ENA                 | This is the enable bit for UART_TX_DONE_INT. (R/W)                           |
| 25  | UART_RX_DONE_INT_ENA                 | This is the enable bit for UART_RX_DONE_INT. (R/W)                           |
| 24  | UART_BRK_DET_INT_ENA                 | This is the enable bit for UART_BRK_DET_INT. (R/W)                           |
| 23  | UART_SW_XON_INT_ENA                  | This is the enable bit for UART_SW_XON_INT. (R/W)                            |
| 22  | UART_SW_XOFF_INT_ENA                 | This is the enable bit for UART_SW_XOFF_INT. (R/W)                           |
| 21  | UART_GLITCH_DET_INT_ENA              | This is the enable bit for UART_GLITCH_DET_INT. (R/W)                        |
| 20  | UART_TX_BRK_DONE_INT_ENA             | This is the enable bit for UART_TX_BRK_DONE_INT. (R/W)                       |
| 19  | UART_TX_BRK_IDLE_DONE_INT_ENA        | This is the enable bit for UART_TX_BRK_IDLE_DONE_INT. (R/W)                  |
| 18  | UART_RXFIFO_FULL_INT_ENA             | This is the enable bit for UART_RXFIFO_FULL_INT. (R/W)                       |
| 17  | UART_TXFIFO_EMPTY_INT_ENA            | This is the enable bit for UART_TXFIFO_EMPTY_INT. (R/W)                      |
| 16  | UART_PARITY_ERR_INT_ENA              | This is the enable bit for UART_PARITY_ERR_INT. (R/W)                        |
| 15  | UART_FRM_ERR_INT_ENA                 | This is the enable bit for UART_FRM_ERR_INT. (R/W)                           |
| 14  | UART_RXFIFO_OVF_INT_ENA              | This is the enable bit for UART_RXFIFO_OVF_INT. (R/W)                        |
| 13  | UART_DSR_CHG_INT_ENA                 | This is the enable bit for UART_DSR_CHG_INT. (R/W)                           |
| 12  | UART_CTS_CHG_INT_ENA                 | This is the enable bit for UART_CTS_CHG_INT. (R/W)                           |
| 11  | UART_BRK_DET_INT_ENA                 | This is the enable bit for UART_BRK_DET_INT. (R/W)                           |
| 10  | UART_RXFIFO_TOUT_INT_ENA             | This is the enable bit for UART_RXFIFO_TOUT_INT. (R/W)                       |
| 9   | UART_SW_XON_INT_ENA                  | This is the enable bit for UART_SW_XON_INT. (R/W)                            |
| 8   | UART_SW_XOFF_INT_ENA                 | This is the enable bit for UART_SW_XOFF_INT. (R/W)                           |
| 7   | UART_GLITCH_DET_INT_ENA              | This is the enable bit for UART_GLITCH_DET_INT. (R/W)                        |
| 6   | UART_TX_BRK_DONE_INT_ENA             | This is the enable bit for UART_TX_BRK_DONE_INT. (R/W)                       |
| 5   | UART_TX_BRK_IDLE_DONE_INT_ENA        | This is the enable bit for UART_TX_BRK_IDLE_DONE_INT. (R/W)                  |
| 4   | UART_RXFIFO_FULL_INT_ENA             | This is the enable bit for UART_RXFIFO_FULL_INT. (R/W)                       |
| 3   | UART_TXFIFO_EMPTY_INT_ENA            | This is the enable bit for UART_TXFIFO_EMPTY_INT. (R/W)                      |
| 2   | UART_PARITY_ERR_INT_ENA              | This is the enable bit for UART_PARITY_ERR_INT. (R/W)                        |
| 1   | UART_FRM_ERR_INT_ENA                 | This is the enable bit for UART_FRM_ERR_INT. (R/W)                           |
| 0   | Reset                                 |                                                                             |

UART_RXFIFO_FULL_INT_ENA    This is the enable bit for UART_RXFIFO_FULL_INT. (R/W)
UART_TXFIFO_EMPTY_INT_ENA   This is the enable bit for UART_TXFIFO_EMPTY_INT. (R/W)
UART_PARITY_ERR_INT_ENA     This is the enable bit for UART_PARITY_ERR_INT. (R/W)
UART_FRM_ERR_INT_ENA        This is the enable bit for UART_FRM_ERR_INT. (R/W)
UART_RXFIFO_OVF_INT_ENA     This is the enable bit for UART_RXFIFO_OVF_INT. (R/W)
UART_DSR_CHG_INT_ENA        This is the enable bit for UART_DSR_CHG_INT. (R/W)
UART_CTS_CHG_INT_ENA        This is the enable bit for UART_CTS_CHG_INT. (R/W)
UART_BRK_DET_INT_ENA        This is the enable bit for UART_BRK_DET_INT. (R/W)
UART_RXFIFO_TOUT_INT_ENA    This is the enable bit for UART_RXFIFO_TOUT_INT. (R/W)
UART_SW_XON_INT_ENA         This is the enable bit for UART_SW_XON_INT. (R/W)
UART_SW_XOFF_INT_ENA        This is the enable bit for UART_SW_XOFF_INT. (R/W)
UART_GLITCH_DET_INT_ENA     This is the enable bit for UART_GLITCH_DET_INT. (R/W)
UART_TX_BRK_DONE_INT_ENA    This is the enable bit for UART_TX_BRK_DONE_INT. (R/W)
UART_TX_BRK_IDLE_DONE_INT_ENA This is the enable bit for UART_TX_BRK_IDLE_DONE_INT. (R/W)

Continued on the next page...
```