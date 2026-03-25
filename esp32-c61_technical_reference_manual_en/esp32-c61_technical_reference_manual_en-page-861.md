

```markdown
Register 25.9. UART_CONFO_SYNC_REG (0x0020)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | (reserved) | UART_RXIFO_RST | UART_RXTXIFO_RST | UART_SW_M | RTS | UART_AUTOBAUD_EN | CLK_LEN | UART_ERR_WR_MASK | INV | UART_RXD_DAT_OVF | UART_RXD_INV | UART_TXD_DPLX | UART_LOOPBACK | UART_IRDA_TX_EN | UART_IRDA_RX_TX_INV | UART_RXTX_INVL | UART_IRDA_TX_DPLX | UART_STOP_BIT_NUM | UART_BIT_NUM | UART_PARITY_EN |
|     |            |              |               |        |      |                 |         |                  |       |             |           |                |              |                   |                     |                      |                    |               |          |            | Reset |

UART_PARITY Configures the parity check mode.
0: Even parity
1: Odd parity
(R/W)

UART_PARITY_EN Configures whether or not to enable UART parity check.
0: Disable
1: Enable
(R/W)

UART_BIT_NUM Configures the number of data bits.
0: 5 bits
1: 6 bits
2: 7 bits
3: 8 bits
(R/W)

UART_STOP_BIT_NUM Configures the number of stop bits.
0: Invalid. No effect
1: 1 bit
2: 1.5 bits
3: 2 bits
(R/W)

UART_TXD_BRK Configures whether or not to send NULL characters when finishing data transmission.
0: Not send
1: Send
(R/W)

UART_IRDA_DPLX Configures whether or not to enable IrDA loopback test.
0: Disable
1: Enable
(R/W)

UART_IRDA_TX_EN Configures whether or not to enable the IrDA transmitter.
0: Disable
1: Enable
(R/W)
```
Continued on the next page...
```