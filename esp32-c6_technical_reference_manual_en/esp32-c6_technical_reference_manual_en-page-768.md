

```markdown
Register 27.15. UART_SWFC_CONFO_SYNC_REG (0x003C)
```

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     |    |    |    | UART_SEND_XOFF | UART_SEND_XON | UART_FORCE_XON | UART_FORCE_XOFF | UART_SW_FLOW_CON_EN | UART_XONOFF_DEL | UART_XONOFF_CHAR | UART_XON_CHAR | Reset |
| Value | 0x13 | 0x11 |    |                |              |               |                 |                   |                  |                 |             |

UART_XON_CHAR Configures the XON character for flow control. (R/W)

UART_XOFF_CHAR Configures the XOOF character for flow control. (R/W)

UART_XON_XOFF_STILL_SEND Configures whether the UART transmitter can send XON or XOFF characters when it is disabled.
- 0: Cannot send
- 1: Can send
(R/W)

UART_SW_FLOW_CON_EN Configures whether or not to enable software flow control.
- 0: Disable
- 1: Enable
(R/W)

UART_XONOFF_DEL Configures whether or not to remove flow control characters from the received data.
- 0: Not move
- 1: Move
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

UART_SEND_XOFF Configures whether or not to send XOOF characters.
- 0: Not send
- 1: Send
(R/W/SS/SC)
```