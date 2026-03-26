

```markdown
Register 42.57. LP_UART_STATUS_REG (0x001C)

| 31 | 30 | 29 | 28 | 24 | 23 | 19 | 18 | 16 | 15 | 14 | 13 | 12 | 8 | 7 | 3 | 2 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
| 1   | 1  | 1  | 0  | 0  | 0  | 0  | 0  | 0  | 1  | 1  | 0  | 0  | 0  | 0  | 0  | 0  | 0 |

LP_UART_RXFIFO_CNT Represents the number of valid data bytes in RX FIFO. (RO)

LP_UART_DSRN Represents the level of the internal LP UART DSR signal. (RO)

LP_UART_CTSN Represents the level of the internal LP UART CTS signal. (RO)

LP_UART_RXD Represents the level of the internal LP UART RXD signal. (RO)

LP_UART_TXFIFO_CNT Represents the number of valid data bytes in RX FIFO. (RO)

LP_UART_DTRN Represents the level of the internal LP UART DTR signal. (RO)

LP_UART_RTSN Represents the level of the internal LP UART RTS signal. (RO)

LP_UART_TXD Represents the level of the internal LP UART TXD signal. (RO)
```

```markdown
Register 42.58. LP_UART_MEM_TX_STATUS_REG (0x0068)

| 31 | 17 | 16 | 12 | 11 | 8 | 7 | 3 | 2 | 0 |
|----|----|----|----|----|----|----|----|----|----|
|    |    |    |    |    |    | Ox0| Ox0|    |    |

LP_UART_TX_SRAM_WADDR Represents the offset address to write TX FIFO. (RO)

LP_UART_TX_SRAM_RADDR Represents the offset address to read TX FIFO. (RO)
```