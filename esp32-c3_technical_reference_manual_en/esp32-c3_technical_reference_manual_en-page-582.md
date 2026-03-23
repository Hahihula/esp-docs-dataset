

```markdown
Register 26.11. UART_FLOW_CONF_REG (0x0034)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 30  | UART_SW_FLOW_CON_EN Set this bit to enable software flow control. When UART receives flow control characters XON or XOFF, which can be configured by UART_XON_CHAR or UART_XOFF_CHAR respectively, UART_SW_XON_INT or UART_SW_XOFF_INT interrupts can be triggered if enabled. (R/W) |
| 29  | UART_XONOFF_DEL Set this bit to remove flow control characters from the received data. (R/W) |
| 28  | UART_FORCE_XON Set this bit to force the transmitter to send data. (R/W)     |
| 27  | UART_FORCE_XOFF Set this bit to stop the transmitter from sending data. (R/W)|
| 26  | UART_SEND_XON Set this bit to send an XON character. This bit is cleared by hardware automatically. (R/W/SS/SC) |
| 25  | UART_SEND_XOFF Set this bit to send an XOFF character. This bit is cleared by hardware automatically. (R/W/SS/SC) |

Register 26.12. UART_SLEEP_CONF_REG (0x0038)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 30  | UART_ACTIVE_THRESHOLD UART is activated from Light-sleep mode when the input RXD edge changes more times than the value of this field plus 3. (R/W) |
```