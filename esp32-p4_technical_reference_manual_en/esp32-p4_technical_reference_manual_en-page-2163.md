

```markdown
Register 42.47. LP_UART_CONF1_REG (0x0024)

| Bit | Field Name                     | Description                                                                 |
|-----|--------------------------------|-----------------------------------------------------------------------------|
| 31  |                                | (reserved)                                                                  |
| 30  |                                | (reserved)                                                                  |
| 29  | LP_UART_CLK_EN                 | Configures clock gating.                                                   |
|     | 0: Support clock only when the application writes registers.<br>1: Always force the clock on for registers. (R/W) |
| 28  | LP_UART_SW_DTR                 | Configures the DTR signal used in software flow control.<br>0: Data to be transmitted is not ready.<br>1: Data to be transmitted is ready. (R/W) |
| 27  | LP_UART_DTR_INV                | Configures whether or not to invert the level of LP UART DTR signal.<br>0: Not invert<br>1: Invert (R/W) |
| 26  | LP_UART_RTS_INV                | Configures whether or not to invert the level of LP UART RTS signal.<br>0: Not invert<br>1: Invert (R/W) |
| 25  | LP_UART_DSR_INV                | Configures whether or not to invert the level of LP UART DSR signal.<br>0: Not invert<br>1: Invert (R/W) |
| 24  | LP_UART_CTS_INV                | Configures whether or not to invert the level of LP UART CTS signal.<br>0: Not invert<br>1: Invert (R/W) |
| 23  | LP_UART_TXFIFO_EMPTY_THRHDD    | Configures the threshold for TX FIFO being empty.<br>Measurement unit: byte. (R/W) |
| 22  | LP_UART_RXFIFO_FULL_THRHDD     | Configures the threshold for RX FIFO being full.<br>Measurement unit: byte. (R/W) |
| 21  |                                | (reserved)                                                                  |
| 20  |                                | (reserved)                                                                  |
| 19  |                                | (reserved)                                                                  |
| 18  |                                | (reserved)                                                                  |
| 17  |                                | (reserved)                                                                  |
| 16  |                                | (reserved)                                                                  |
| 15  | LP_UART_CTS_INV                | Configures whether or not to invert the level of LP UART CTS signal.<br>0: Not invert<br>1: Invert (R/W) |
| 14  | LP_UART_RTS_INV                | Configures whether or not to invert the level of LP UART RTS signal.<br>0: Not invert<br>1: Invert (R/W) |
| 13  | LP_UART_DSR_INV                | Configures whether or not to invert the level of LP UART DSR signal.<br>0: Not invert<br>1: Invert (R/W) |
| 12  | LP_UART_CTS_INV                | Configures whether or not to invert the level of LP UART CTS signal.<br>0: Not invert<br>1: Invert (R/W) |
| 11  |                                | (reserved)                                                                  |
| 10  |                                | (reserved)                                                                  |
| 9   |                                | (reserved)                                                                  |
| 8   |                                | (reserved)                                                                  |
| 7   |                                | (reserved)                                                                  |
| 6   |                                | (reserved)                                                                  |
| 5   |                                | (reserved)                                                                  |
| 4   |                                | (reserved)                                                                  |
| 3   |                                | (reserved)                                                                  |
| 2   |                                | (reserved)                                                                  |
| 1   |                                | (reserved)                                                                  |
| 0   | Reset                          |                                                                             |

LP_UART_RXFIFO_FULL_THRHDD Configures the threshold for RX FIFO being full.<br>Measurement unit: byte. (R/W)

LP_UART_TXFIFO_EMPTY_THRHDD Configures the threshold for TX FIFO being empty.<br>Measurement unit: byte. (R/W)

LP_UART_CTS_INV Configures whether or not to invert the level of LP UART CTS signal.<br>0: Not invert<br>1: Invert (R/W)

LP_UART_DSR_INV Configures whether or not to invert the level of LP UART DSR signal.<br>0: Not invert<br>1: Invert (R/W)

LP_UART_RTS_INV Configures whether or not to invert the level of LP UART RTS signal.<br>0: Not invert<br>1: Invert (R/W)

LP_UART_DTR_INV Configures whether or not to invert the level of LP UART DTR signal.<br>0: Not invert<br>1: Invert (R/W)

LP_UART_SW_DTR Configures the DTR signal used in software flow control.<br>0: Data to be transmitted is not ready.<br>1: Data to be transmitted is ready. (R/W)

LP_UART_CLK_EN Configures clock gating.<br>0: Support clock only when the application writes registers.<br>1: Always force the clock on for registers. (R/W)
```