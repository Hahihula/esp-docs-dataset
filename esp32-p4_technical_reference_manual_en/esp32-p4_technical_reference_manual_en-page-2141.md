

```markdown
Register 42.10. UART_CONF1_REG (0x0024)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     |    |    |    |    |    |    |    |    |    | UART_CLK_EN | UART_SW_DTR | UART_DTR_INV | UART_RTS_INV | UART_DSR_INV | UART_CTS_INV | UART_TXFIFO_EMPTY_THRD | UART_RXFIFO_FULL_THRD | (reserved) |
| Value | 0x60 |    |    |    |    |    |    |    |    |            |             |              |               |                |                 |                  |                   |           |

UART_RXFIFO_FULL_THRD Configures the threshold for RX FIFO being full.
Measurement unit: byte. (R/W)

UART_TXFIFO_EMPTY_THRD Configures the threshold for TX FIFO being empty.
Measurement unit: byte. (R/W)

UART_CTS_INV Configures whether or not to invert the level of UART CTS signal.
0: Not invert
1: Invert
(R/W)

UART_DSR_INV Configures whether or not to invert the level of UART DSR signal.
0: Not invert
1: Invert
(R/W)

UART_RTS_INV Configures whether or not to invert the level of UART RTS signal.
0: Not invert
1: Invert
(R/W)

UART_DTR_INV Configures whether or not to invert the level of UART DTR signal.
0: Not invert
1: Invert
(R/W)

UART_SW_DTR Configures the DTR signal used in software flow control.
0: Data to be transmitted is not ready.
1: Data to be transmitted is ready.
(R/W)

UART_CLK_EN Configures clock gating.
0: Support clock only when the application writes registers.
1: Always force the clock on for registers.
(R/W)
```