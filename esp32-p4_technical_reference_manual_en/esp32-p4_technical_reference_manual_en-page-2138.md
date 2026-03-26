

```markdown
Register 42.9. UART_CONFO_SYNC_REG (0x0020)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | (reserved) | UART_XIFO_RST | UART_RXIFO_RST | UART_SW_M | RTS | UART_AUTOBAUD_EN | CLK_LEN | UART_ERR_WR_MASK | OVF | UART_RDX_DLY | INV | UART_IRDA_TX_EN | UART_LOOPBACK | UART_IRDA_RX_TX_INV | UART_RDX_DPLX | UART_STOP_BIT_NUM | UART_BIT_NUM | UART_PARITY_EN |
| Value | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 1 | 3 | 0 | 0 | Reset |

UART_PARITY Configures the parity check mode.
O: Even parity
1: Odd parity
(R/W)

UART_PARITY_EN Configures whether or not to enable UART parity check.
O: Disable
1: Enable
(R/W)

UART_BIT_NUM Configures the number of data bits.
O: 5 bits
1: 6 bits
2: 7 bits
3: 8 bits
(R/W)

UART_STOP_BIT_NUM Configures the number of stop bits.
O: Invalid. No effect
1: 1 bit
2: 1.5 bits
3: 2 bits
(R/W)

UART_TXD_BRK Configures whether or not to send NULL characters when finishing data transmission.
O: Not send
1: Send
(R/W)

UART_IRDA_DPLX Configures whether or not to enable IrDA loopback test.
O: Disable
1: Enable
(R/W)

UART_IRDA_TX_EN Configures whether or not to enable the IrDA transmitter.
O: Disable
1: Enable
(R/W)
```