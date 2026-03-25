

```markdown
Register 32.15. UART_SWFC_CONFO_SYNC_REG (0x003C)

| Bit | Field Name                  | Description                                                                 |
|-----|-----------------------------|-----------------------------------------------------------------------------|
| 31  |                             | (reserved)                                                                  |
| 23  | UART_SEND_XOFF              | Configures whether or not to send XOFF characters.                           |
| 22  | UART_FORCE_XOFF             | Configures whether or not to stop the transmitter from sending data.         |
| 21  | UART_FORCE_XON              | Configures whether the transmitter continues to sending data.                |
| 20  | UART_SEND_XON               | Configures whether or not to send XON characters.                            |
| 19  |                             |                                                                             |
| 18  | UART_XOFF_CHAR              | Configures the XOFF character for flow control. (R/W)                        |
| 17  | UART_XON_CHAR               | Configures the XON character for flow control. (R/W)                         |
| 16  | UART_XONOFF_DEL             | Configures whether or not to remove flow control characters from received data.|
| 15  | UART_SW_FLOW_CON_EN         | Configures whether or not to enable software flow control.                   |
| 14  |                             |                                                                             |
| 13  | UART_SEND_XONOFF            | Configures whether the transmitter can send XON or XOFE characters when disabled.|
| 12  |                             |                                                                             |
| 11  |                             | Ox13                                                                         |
| 10  |                             | Ox11                                                                         |
| 9   |                             | Reset                                                                        |
| 8   |                             |                                                                             |

UART_XON_CHAR Configures the XON character for flow control. (R/W)

UART_XOFF_CHAR Configures the XOFE character for flow control. (R/W)

UART_XON_XOFF_STILL_SEND Configures whether the UART transmitter can send XON or XOFE characters when it is disabled.
O: Cannot send
1: Can send
(R/W)

UART_SW_FLOW_CON_EN Configures whether or not to enable software flow control.
O: Disable
1: Enable
(R/W)

UART_XONOFF_DEL Configures whether or not to remove flow control characters from the received data.
O: Not move
1: Move
(R/W)

UART_FORCE_XON Configures whether the transmitter continues to sending data.
O: Not send
1: Send
(R/W)

UART_FORCE_XOFF Configures whether or not to stop the transmitter from sending data.
O: Not stop
1: Stop
(R/W)

UART_SEND_XON Configures whether or not to send XON characters.
O: Not send
1: Send
(R/W/SS/SC)

UART_SEND_XOFF Configures whether or not to send XOFE characters.
O: Not send
1: Send
(R/W/SS/SC)
```