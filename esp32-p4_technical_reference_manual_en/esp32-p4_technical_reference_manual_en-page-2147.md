

```markdown
Register 42.20. UART_CLK_CONF_REG (0x0088)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 |
|-----|----|----|----|----|----|----|----|----|----|
|     |    | UART_RX_SCLK_EN | UART_TX_SCLK_EN | UART_RX_RST_CORE | UART_TX_RST_CORE | (reserved) | (reserved) | Reset |

UART_TX_SCLK_EN Configures whether or not to enable UART TX clock.
O: Disable
1: Enable
(R/W)

UART_RX_SCLK_EN Configures whether or not to enable UART RX clock.
O: Disable
1: Enable
(R/W)

UART_TX_RST_CORE Write 1 and then write 0 to reset UART TX. (R/W)

UART_RX_RST_CORE Write 1 and then write 0 to reset UART RX. (R/W)


Register 42.21. UART_STATUS_REG (0x001C)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | UART_TXD | UART_RTSN | UART_DTRN | (reserved) | UART_RXFIFO_CNT | UART_RXD | UART_CTSN | UART_RXD | UART_DSRN | UART_RTD | UART_DTRN | UART_TXD | Reset |

UART_RXFIFO_CNT Represents the number of valid data bytes in RX FIFO. (RO)

UART_DSRN Represents the level of the internal UART DSR signal. (RO)

UART_CTSN Represents the level of the internal UART CTS signal. (RO)

UART_RXD Represents the level of the internal UART RXD signal. (RO)

UART_TXFIFO_CNT Represents the number of valid data bytes in RX FIFO. (RO)

UART_DTRN Represents the level of the internal UART DTR signal. (RO)

UART_RTSN Represents the level of the internal UART RTS signal. (RO)

UART_TXD Represents the level of the internal UART TXD signal. (RO)
```