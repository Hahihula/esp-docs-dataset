

```markdown
Register 32.42. LP_UART_INT_ENA_REG (0x000C)

| Bit | Field Name                                 | Description                                                                 |
|-----|---------------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                                 |                                                                             |
| 30  | LP_UART_WAKEUP_INT_ENA                     | Write 1 to enable LP_UART_WAKEUP_INT. (R/W)                                 |
| 29  | LP_UART_AT_CMD_CHAR_DET_INT_ENA            | Write 1 to enable LP_UART_AT_CMD_CHAR_DET_INT. (R/W)                        |
| 28  | (reserved)                                 |                                                                             |
| 27  | LP_UART_TX_DONE_INT_ENA                    | Write 1 to enable LP_UART_TX_DONE_INT. (R/W)                                |
| 26  | LP_UART_TX_BRK_IDLE_DONE_INT_ENA           | Write 1 to enable LP_UART_TX_BRK_IDLE_DONE_INT. (R/W)                      |
| 25  | LP_UART_TX_BRK_DONE_INT_ENA                | Write 1 to enable LP_UART_TX_BRK_DONE_INT. (R/W)                           |
| 24  | LP_UART_SW_XON_INT_ENA                     | Write 1 to enable LP_UART_SW_XON_INT.(R/W)                                  |
| 23  | LP_UART_SW_XOFF_INT_ENA                    | Write 1 to enable LP_UART_SW_XOFF_INT. (R/W)                                |
| 22  | LP_UART_GLITCH_DET_INT_ENA                 | Write 1 to enable LP_UART_GLITCH_DET_INT. (R/W)                             |
| 21  | LP_UART_RXFIFO_TOUT_INT_ENA                | Write 1 to enable LP_UART_RXFIFO_TOUT_INT. (R/W)                           |
| 20  | LP_UART_BRK_DET_INT_ENA                    | Write 1 to enable LP_UART_BRK_DET_INT. (R/W)                                |
| 19  | LP_UART_CTS_CHG_INT_ENA                    | Write 1 to enable LP_UART_CTS_CHG_INT. (R/W)                                |
| 18  | LP_UART_DSR_CHG_INT_ENA                    | Write 1 to enable LP_UART_DSR_CHG_INT. (R/W)                                |
| 17  | LP_UART_RXFIFO_OVF_INT_ENA                 | Write 1 to enable LP_UART_RXFIFO_OVF_INT. (R/W)                            |
| 16  | LP_UART_FRM_ERR_INT_ENA                    | Write 1 to enable LP_UART_FRM_ERR_INT. (R/W)                                |
| 15  | LP_UART_PARITY_ERR_INT_ENA                 | Write 1 to enable LP_UART_PARITY_ERR_INT. (R/W)                            |
| 14  | LP_UART_TXFIFO_EMPTY_INT_ENA               | Write 1 to enable LP_UART_TXFIFO_EMPTY_INT. (R/W)                          |
| 13  | LP_UART_RXFIFO_FULL_INT_ENA                | Write 1 to enable LP_UART_RXFIFO_FULL_INT. (R/W)                           |
| 12  | LP_UART_TX_DONE_INT_ENA                    | Write 1 to enable LP_UART_TX_DONE_INT. (R/W)                                |
| 11  | LP_UART_TX_BRK_IDLE_DONE_INT_ENA           | Write 1 to enable LP_UART_TX_BRK_IDLE_DONE_INT. (R/W)                      |
| 10  | LP_UART_TX_BRK_DONE_INT_ENA                | Write 1 to enable LP_UART_TX_BRK_DONE_INT. (R/W)                           |
| 9   | LP_UART_SW_XON_INT_ENA                     | Write 1 to enable LP_UART_SW_XON_INT.(R/W)                                  |
| 8   | LP_UART_SW_XOFF_INT_ENA                    | Write 1 to enable LP_UART_SW_XOFF_INT. (R/W)                                |
| 7   | LP_UART_GLITCH_DET_INT_ENA                 | Write 1 to enable LP_UART_GLITCH_DET_INT. (R/W)                             |
| 6   | LP_UART_RXFIFO_TOUT_INT_ENA                | Write 1 to enable LP_UART_RXFIFO_TOUT_INT. (R/W)                           |
| 5   | LP_UART_BRK_DET_INT_ENA                    | Write 1 to enable LP_UART_BRK_DET_INT. (R/W)                                |
| 4   | LP_UART_CTS_CHG_INT_ENA                    | Write 1 to enable LP_UART_CTS_CHG_INT. (R/W)                                |
| 3   | LP_UART_DSR_CHG_INT_ENA                    | Write 1 to enable LP_UART_DSR_CHG_INT. (R/W)                                |
| 2   | LP_UART_RXFIFO_OVF_INT_ENA                 | Write 1 to enable LP_UART_RXFIFO_OVF_INT. (R/W)                            |
| 1   | LP_UART_FRM_ERR_INT_ENA                    | Write 1 to enable LP_UART_FRM_ERR_INT. (R/W)                                |
| 0   | LP_UART_PARITY_ERR_INT_ENA                 | Write 1 to enable LP_UART_PARITY_ERR_INT. (R/W)                            |

LP_UART_WAKEUP_INT_ENA Write 1 to enable LP_UART_WAKEUP_INT. (R/W)
LP_UART_AT_CMD_CHAR_DET_INT_ENA Write 1 to enable LP_UART_AT_CMD_CHAR_DET_INT. (R/W)
LP_UART_TX_DONE_INT_ENA Write 1 to enable LP_UART_TX_DONE_INT. (R/W)
LP_UART_TX_BRK_IDLE_DONE_INT_ENA Write 1 to enable LP_UART_TX_BRK_IDLE_DONE_INT. (R/W)
LP_UART_TX_BRK_DONE_INT_ENA Write 1 to enable LP_UART_TX_BRK_DONE_INT. (R/W)
LP_UART_SW_XON_INT_ENA Write 1 to enable LP_UART_SW_XON_INT.(R/W)
LP_UART_SW_XOFF_INT_ENA Write 1 to enable LP_UART_SW_XOFF_INT. (R/W)
LP_UART_GLITCH_DET_INT_ENA Write 1 to enable LP_UART_GLITCH_DET_INT. (R/W)
LP_UART_RXFIFO_TOUT_INT_ENA Write 1 to enable LP_UART_RXFIFO_TOUT_INT. (R/W)
LP_UART_BRK_DET_INT_ENA Write 1 to enable LP_UART_BRK_DET_INT. (R/W)
LP_UART_CTS_CHG_INT_ENA Write 1 to enable LP_UART_CTS_CHG_INT. (R/W)
LP_UART_DSR_CHG_INT_ENA Write 1 to enable LP_UART_DSR_CHG_INT. (R/W)
LP_UART_RXFIFO_OVF_INT_ENA Write 1 to enable LP_UART_RXFIFO_OVF_INT. (R/W)
LP_UART_FRM_ERR_INT_ENA Write 1 to enable LP_UART_FRM_ERR_INT. (R/W)
LP_UART_PARITY_ERR_INT_ENA Write 1 to enable LP_UART_PARITY_ERR_INT. (R/W)
LP_UART_TXFIFO_EMPTY_INT_ENA Write 1 to enable LP_UART_TXFIFO_EMPTY_INT. (R/W)
LP_UART_RXFIFO_FULL_INT_ENA Write 1 to enable LP_UART_RXFIFO_FULL_INT. (R/W)

LP_UART_WAKEUP_INT_ENA Write 1 to enable LP_UART_WAKEUP_INT. (R/W)
```