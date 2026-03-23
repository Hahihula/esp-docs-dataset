

```markdown
Register 27.46. LP_UART_CONFO_SYNC_REG (0x0020)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | (reserved) | LP_UART_TXIFO_RST | LP_UART_RXIFO_RST | LP_UART_SW_RST | LP_UART_MEM_CLK_EN | LP_UART_ERR_WR_MASK | LP_UART_DIS_RX_DFT_OVF | LP_UART_RXD_INV | LP_UART_TX_LOOPBK | LP_UART_TxD_BRK | LP_UART_STOP_BIT_NUM | LP_UART_BIT_NUM | LP_UART_PARITY_EN | LP_UART_PARITY | Reset |
|     | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 1 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 |

LP_UART_PARITY Configures the parity check mode.
- O: Even parity
- 1: Odd parity (R/W)

LP_UART_PARITY_EN Configures whether or not to enable LP UART parity check.
- O: Disable
- 1: Enable (R/W)

LP_UART_BIT_NUM Configures the number of data bits.
- O: 5 bits
- 1: 6 bits
- 2: 7 bits
- 3: 8 bits (R/W)

LP_UART_STOP_BIT_NUM Configures the number of stop bits.
- O: Invalid. No effect
- 1: 1 bit
- 2: 1.5 bits
- 3: 2 bits (R/W)

LP_UART_TXD_BRK Configures whether or not to send NULL characters when finishing data transmission.
- O: Not send
- 1: Send (R/W)

LP_UART_LOOPBACK Configures whether or not to enable LP UART loopback test.
- O: Disable
- 1: Enable (R/W)

Continued on the next page...
```