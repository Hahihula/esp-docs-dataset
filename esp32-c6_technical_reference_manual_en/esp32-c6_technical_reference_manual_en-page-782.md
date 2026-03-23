

```markdown
|Bit Name                                 |Bits Description                                                                 |
|------------------------------------------|----------------------------------------------------------------------------------|
|31                                       |reserved                                                                          |
|20                                       |LP_UART_WAKEUP_INT_ENA                                                            |
|19                                       |LP_UART_AT_CMD_CHAR_DET_INT_ENA                                                   |
|(reserved)                              |(reserved)                                                                        |
|18                                       |LP_UART_TX_DONE_INT_ENA                                                           |
|17                                       |LP_UART_RX_TX_BRK_IDLE_DONE_INT_ENA                                               |
|16                                       |LP_UART_SW_XON_INT_ENA                                                            |
|15                                       |LP_UART_SW_XOFF_INT_ENA                                                           |
|14                                       |LP_UART_GLITCH_DET_INT_ENA                                                        |
|13                                       |LP_UART_TX_BRK_DONE_INT_ENA                                                       |
|12                                       |LP_UART_TX_BRK_IDLE_DONE_INT_ENA                                                  |
|11                                       |LP_UART_RXFIFO_OUT_INT_ENA                                                        |
|10                                       |LP_UART_DSR_CHG_INT_ENA                                                           |
|9                                        |LP_UART_CTS_CHG_INT_ENA                                                           |
|8                                        |LP_UART_FRM_ERR_INT_ENA                                                           |
|7                                        |LP_UART_PARITY_ERR_INT_ENA                                                        |
|6                                        |LP_UART_TXFIFO_EMPTY_INT_ENA                                                      |
|5                                        |LP_UART_RXFIFO_FULL_INT_ENA                                                       |
```

Register 27.42. LP_UART_INT_ENA_REG (0x000C)

LP_UART_RXFIFO_FULL_INT_ENA Write 1 to enable LP_UART_RXFIFO_FULL_INT. (R/W)
LP_UART_TXFIFO_EMPTY_INT_ENA Write 1 to enable LP_UART_TXFIFO_EMPTY_INT. (R/W)
LP_UART_PARITY_ERR_INT_ENA Write 1 to enable LP_UART_PARITY_ERR_INT. (R/W)
LP_UART_FRM_ERR_INT_ENA Write 1 to enable LP_UART_FRM_ERR_INT. (R/W)
LP_UART_RXFIFO_OVF_INT_ENA Write 1 to enable LP_UART_RXFIFO_OVF_INT. (R/W)
LP_UART_DSR_CHG_INT_ENA Write 1 to enable LP_UART_DSR_CHG_INT. (R/W)
LP_UART_CTS_CHG_INT_ENA Write 1 to enable LP_UART_CTS_CHG_INT. (R/W)
LP_UART_BRK_DET_INT_ENA Write 1 to enable LP_UART_BRK_DET_INT. (R/W)
LP_UART_RXFIFO_OUT_INT_ENA Write 1 to enable LP_UART_RXFIFO_OUT_INT. (R/W)
LP_UART_SW_XON_INT_ENA Write 1 to enable LP_UART_SW_XON_INT.(R/W)
LP_UART_SW_XOFF_INT_ENA Write 1 to enable LP_UART_SW_XOFF_INT. (R/W)
LP_UART_GLITCH_DET_INT_ENA Write 1 to enable LP_UART_GLITCH_DET_INT. (R/W)
LP_UART_TX_BRK_DONE_INT_ENA Write 1 to enable LP_UART_TX_BRK_DONE_INT. (R/W)
LP_UART_TX_BRK_IDLE_DONE_INT_ENA Write 1 to enable LP_UART_TX_BRK_IDLE_DONE_INT. (R/W)
LP_UART_TX_DONE_INT_ENA Write 1 to enable LP_UART_TX_DONE_INT. (R/W)
LP_UART_AT_CMD_CHAR_DET_INT_ENA Write 1 to enable LP_UART_AT_CMD_CHAR_DET_INT. (R/W)
LP_UART_WAKEUP_INT_ENA Write 1 to enable LP_UART_WAKEUP_INT. (R/W)

Espressif Systems
782
ESP32-C6 TRM (Version 1.1)
Submit Documentation Feedback