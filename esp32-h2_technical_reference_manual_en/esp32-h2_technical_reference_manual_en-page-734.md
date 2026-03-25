

```markdown
Register 28.15. UART_SWFC_CONFO_SYNC_REG (0x003C)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 23  | UART_SEND_XOFF                                                              |
| 22  | UART_FORCE_XON                                                              |
| 21  | UART_SEND_XON                                                              |
| 20  | UART_FORCE_XOFF                                                             |
| 19  | UART_SEND_XOFF                                                              |
| 18  | UART_XONOFF_DEL                                                             |
| 17  | UART_XONOFF_DEL_EN                                                          |
| 16  | UART_SW_FLOW_CON_EN                                                         |
| 15  | UART_XONOFF_DEL_EN                                                          |
| 8   | UART_XOFF_CHAR                                                              |
| 7   | UART_XON_CHAR                                                               |
| 0   | Reset                                                                      |

UART_XON_CHAR Configures the XON character for flow control. (R/W)

UART_XOFF_CHAR Configures the XOFE character for flow control. (R/W)

UART_XON_XOFF_STILL_SEND Configures whether the UART transmitter can send XON or XOFF characters when it is disabled.
  - 0: Cannot send
  - 1: Can send
(R/W)

UART_SW_FLOW_CON_EN Configures whether or not to enable software flow control.
  - 0: Disable
  - 1: Enable
(R/W)

UART_XONOFF_DEL Configures whether or not to remove flow control characters from the received data.
  - 0: Not remove
  - 1: Remove
(R/W)

UART_FORCE_XON Configures whether the transmitter continues to sending data.
  - 0: Not send
  - 1: Send
(R/W)

UART_FORCE_XOFF Configures whether or not to stop the transmitter from sending data.
  - 0: Not stop
  - 1: Stop
(R/W)

UART_SEND_XON Configures whether or not to send XON characters.
  - 0: Not send
  - 1: Send
(R/W/SS/SC)

UART_SEND_XOFF Configures whether or not to send XOFE characters.
  - 0: Not send
  - 1: Send
(R/W/SS/SC)
```