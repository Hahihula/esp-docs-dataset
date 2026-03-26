

```markdown
Register 42.52. LP_UART_SWFC_CONF0_SYNC_REG (0x003C)

| Bit | Name                                 | Description                                                                 |
|-----|--------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                          |                                                                             |
| 23  | LP_UART_SEND_XOFF                   | Configures the XON character for flow control. (R/W)                        |
| 22  | LP_UART_FORCE_XON                   | Configures whether the transmitter continues to sending data.                |
| 21  | LP_UART_SEND_XOFF                   | Configures whether or not to send XOFF characters.                           |
| 20  | LP_UART_FORCE_XOFF                  | Configures whether or not to stop the transmitter from sending data.         |
| 19  | LP_UART_SEND_XON                    | Configures whether or not to send XON characters.                            |
| 18  | LP_UART_XONOFF_DEL                  | Configures whether or not to remove flow control characters from received data.|
| 17  | LP_UART_SW_FLOW_CON_EN              | Configures whether or not to enable software flow control.                   |
| 16  | LP_UART_XON_OFF_CHAR                | Configures the XOFF character for flow control. (R/W)                        |
| 15  | LP_UART_XON_CHAR                    | Configures the XON character for flow control. (R/W)                         |
| 8   | LP_UART_XON_OFF_STILL_SEND          | Configures whether the LP UART transmitter can send XON or XOFF characters when it is disabled. |
| 7   | LP_UART_XON_OFF_CHAR                | Configures the XOFF character for flow control. (R/W)                        |
| 6   | LP_UART_XON_CHAR                    | Configures the XON character for flow control. (R/W)                         |

LP_UART_XON_CHAR    Configures the XON character for flow control. (R/W)
LP_UART_XOFF_CHAR    Configures the XOFF character for flow control. (R/W)
LP_UART_XON_OFF_STILL_SEND  Configures whether the LP UART transmitter can send XON or XOFF characters when it is disabled.
0: Cannot send
1: Can send
(R/W)

LP_UART_SW_FLOW_CON_EN  Configures whether or not to enable software flow control.
0: Disable
1: Enable
(R/W)

LP_UART_XONOFF_DEL    Configures whether or not to remove flow control characters from the received data.
0: Not move
1: Move
(R/W)

LP_UART_FORCE_XON    Configures whether the transmitter continues to sending data.
0: Not send
1: Send
(R/W)

LP_UART_FORCE_XOFF   Configures whether or not to stop the transmitter from sending data.
0: Not stop
1: Stop
(R/W)

LP_UART_SEND_XON     Configures whether or not to send XON characters.
0: Not send
1: Send
(R/W/SS/SC)

LP_UART_SEND_XOFF    Configures whether or not to send XOFF characters.
0: Not send
1: Send
(R/W/SS/SC)
```