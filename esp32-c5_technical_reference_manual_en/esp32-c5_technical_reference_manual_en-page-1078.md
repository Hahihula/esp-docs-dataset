

```markdown
Register 32.47. LP_UART_CONF1_REG (0x0024)

| Bit | Field Name                     | Description                                                                 |
|-----|---------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                     |                                                                             |
| 30  | LP_UART_CLK_EN                 | Configures clock gating.<br>0: Support clock only when the application writes registers.<br>1: Always force the clock on for registers. (R/W) |
| 29  | LP_UART_SW_DTR                 | Configures the DTR signal used in software flow control.<br>0: Data to be transmitted is not ready.<br>1: Data to be transmitted is ready. (R/W) |
| 28  | LP_UART_DTR_INV                | Configures whether or not to invert the level of LP UART DTR signal.<br>0: Not invert<br>1: Invert (R/W) |
| 27  | LP_UART_RTS_INV                | Configures whether or not to invert the level of LP UART RTS signal.<br>0: Not invert<br>1: Invert (R/W) |
| 26  | LP_UART_DSR_INV                | Configures whether or not to invert the level of LP UART DSR signal.<br>0: Not invert<br>1: Invert (R/W) |
| 25  | LP_UART_CTS_INV                | Configures whether or not to invert the level of LP UART CTS signal.<br>0: Not invert<br>1: Invert (R/W) |
| 24  | LP_UART_TXFIFO_EMPTY_THRHDD    | Configures the threshold for TX FIFO being empty.<br>Measurement unit: byte. (R/W) |
| 23  | LP_UART_RXFIFO_FULL_THRHDD     | Configures the threshold for RX FIFO being full.<br>Measurement unit: byte. (R/W) |

LP_UART_RXFIFO_FULL_THRHDD   Configures the threshold for RX FIFO being full.
Measurement unit: byte. (R/W)

LP_UART_TXFIFO_EMPTY_THRHDD   Configures the threshold for TX FIFO being empty.
Measurement unit: byte. (R/W)

LP_UART_CTS_INV              Configures whether or not to invert the level of LP UART CTS signal.
0: Not invert
1: Invert
(R/W)

LP_UART_DSR_INV              Configures whether or not to invert the level of LP UART DSR signal.
0: Not invert
1: Invert
(R/W)

LP_UART_RTS_INV              Configures whether or not to invert the level of LP UART RTS signal.
0: Not invert
1: Invert
(R/W)

LP_UART_DTR_INV              Configures whether or not to invert the level of LP UART DTR signal.
0: Not invert
1: Invert
(R/W)

LP_UART_SW_DTR               Configures the DTR signal used in software flow control.
0: Data to be transmitted is not ready.
1: Data to be transmitted is ready.
(R/W)

LP_UART_CLK_EN               Configures clock gating.
0: Support clock only when the application writes registers.
1: Always force the clock on for registers.
(R/W)
```