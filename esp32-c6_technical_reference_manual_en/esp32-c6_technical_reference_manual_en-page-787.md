

```markdown
Register 27.47. LP_UART_CONF1_REG (0x0024)

| Bit | Description                  |
|-----|------------------------------|
| 31  | (reserved)                   |
| 30  | LP_UART_CLK_EN               |
| 29  | LP_UART_SW_DTR               |
| 28  | LP_UART_DTR_INV              |
| 27  | LP_UART_RTS_INV              |
| 26  | LP_UART_DSR_INV              |
| 25  | LP_UART_CTS_INV              |
| 24  | LP_UART_TXFIFO_EMPTY_THRHD   |
| 23  | LP_UART_RXFIFO_FULL_THRHD    |
| 22  | (reserved)                   |
| 15  | Oxc                          |
| 14  | O                            |
| 13  | O                            |
| 12  | O                            |
| 11  | O                            |
| 10  | O                            |
| 9   | O                            |
| 8   | O                            |
| 7   | Oxc                          |
| 6   | O                            |
| 5   | O                            |
| 4   | O                            |
| 3   | O                            |
| 2   | O                            |
| 1   | O                            |
| 0   | Reset                        |

LP_UART_RXFIFO_FULL_THRHD Configures the threshold for RX FIFO being full.
Measurement unit: byte. (R/W)

LP_UART_TXFIFO_EMPTY_THRHD Configures the threshold for TX FIFO being empty.
Measurement unit: byte. (R/W)

LP_UART_CTS_INV Configures whether or not to invert the level of LP UART CTS signal.
0: Not invert
1: Invert
(R/W)

LP_UART_DSR_INV Configures whether or not to invert the level of LP UART DSR signal.
0: Not invert
1: Invert
(R/W)

LP_UART_RTS_INV Configures whether or not to invert the level of LP UART RTS signal.
0: Not invert
1: Invert
(R/W)

LP_UART_DTR_INV Configures whether or not to invert the level of LP UART DTR signal.
0: Not invert
1: Invert
(R/W)

LP_UART_SW_DTR Configures the DTR signal used in software flow control.
0: Data to be transmitted is not ready.
1: Data to be transmitted is ready.
(R/W)

LP_UART_CLK_EN Configures clock gating.
0: Support clock only when the application writes registers.
1: Always force the clock on for registers.
(R/W)
```