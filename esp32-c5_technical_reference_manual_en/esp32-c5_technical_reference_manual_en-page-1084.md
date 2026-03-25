

```markdown
Register 32.57. LP_UART_CLK_CONF_REG (0x0088)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 |
|-----|----|----|----|----|----|----|----|----|----|
|     |    |    |    | (reserved) | LP_UART_RX_RST_CORE | LP_UART_TX_RST_CORE | LP_UART_RX_SCLK_EN | LP_UART_TX_SCLK_EN | (reserved) |
| Value | 0 | 0 | 0 | 0 | 0 | 1 | 1 | 0 | Reset |

LP_UART_TX_SCLK_EN Configures whether or not to enable LP UART TX clock.
O: Disable
1: Enable
(R/W)

LP_UART_RX_SCLK_EN Configures whether or not to enable LP UART RX clock.
O: Disable
1: Enable
(R/W)

LP_UART_TX_RST_CORE Write 1 and then write 0 to reset LP UART TX. (R/W)

LP_UART_RX_RST_CORE Write 1 and then write 0 to reset LP UART RX. (R/W)


Register 32.58. LP_UART_STATUS_REG (0x001C)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | LP_UART_TXD | LP_UART_RXD | (reserved) | LP_UART_RTSN | LP_UART_DTRN | LP_UART_RXFIFO_CNT | LP_UART_TXFIFO_CNT | LP_UART_RXFIFO_CNT | LP_UART_DSRN | LP_UART_CTSN | LP_UART_RXD | LP_UART_TXD | LP_UART_RXFIFO_CNT | (reserved) | LP_UART_RxD | LP_UART_CTSN | LP_UART_DTRN | LP_UART_RXD | LP_UART_TXD | LP_UART_RXFIFO_CNT | LP_UART_TXFIFO_CNT | LP_UART_RXFIFO_CNT | LP_UART_DSRN | LP_UART_CTSN | LP_UART_RXD | LP_UART_TXD | (reserved) | LP_UART_RXFIFO_CNT | LP_UART_TXFIFO_CNT | LP_UART_RXFIFO_CNT | Reset |

LP_UART_RXFIFO_CNT Represents the number of valid data bytes in RX FIFO. (RO)

LP_UART_DSRN Represents the level of the internal LP UART DSR signal. (RO)

LP_UART_CTSN Represents the level of the internal LP UART CTS signal. (RO)

LP_UART_RXD Represents the level of the internal LP UART RXD signal. (RO)

LP_UART_TXFIFO_CNT Represents the number of valid data bytes in RX FIFO. (RO)

LP_UART_DTRN Represents the level of the internal LP UART DTR signal. (RO)

LP_UART_RTSN Represents the level of the internal LP UART RTS signal. (RO)

LP_UART_TXD Represents the level of the internal LP UART TXD signal. (RO)
```