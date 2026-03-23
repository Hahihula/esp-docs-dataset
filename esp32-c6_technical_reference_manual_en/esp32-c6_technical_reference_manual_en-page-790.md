

```markdown
Register 27.52. LP_UART_SWFC_CONF0_SYNC_REG (0x003C)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     |    |    |    |    | LP_UART_SEND_XOFF | LP_UART_FORCE_XON | LP_UART_SW_FLOW_CON_EN | LP_UART_XON_OFF_DEL | LP_UART_XON_OFF_SEND_STILL_SEND | LP_UART_XON_CHAR | (reserved) |
| Value | 0x13 |     |     |     |     |     |     |     |     |     |     |

LP_UART_XON_CHAR Configures the XON character for flow control. (R/W)
LP_UART_XOFF_CHAR Configures the XOFF character for flow control. (R/W)
LP_UART_XON_XOFF_STILL_SEND Configures whether the LP UART transmitter can send XON or XOFF characters when it is disabled.
  O: Cannot send
  1: Can send
  (R/W)

LP_UART_SW_FLOW_CON_LEN Configures whether or not to enable software flow control.
  O: Disable
  1: Enable
  (R/W)

LP_UART_XONOFF_DEL Configures whether or not to remove flow control characters from the received data.
  O: Not move
  1: Move
  (R/W)

LP_UART_FORCE_XON Configures whether the transmitter continues to sending data.
  O: Not send
  1: Send
  (R/W)

LP_UART_FORCE_XOFF Configures whether or not to stop the transmitter from sending data.
  O: Not stop
  1: Stop
  (R/W)

LP_UART_SEND_XON Configures whether or not to send XON characters.
  O: Not send
  1: Send
  (R/W/SS/SC)

LP_UART_SEND_XOFF Configures whether or not to send XOFF characters.
  O: Not send
  1: Send
  (R/W/SS/SC)
```