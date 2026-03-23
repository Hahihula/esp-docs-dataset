
```markdown
Register 26.18. UART_CLK_CONF_REG (0x0078)

| 31 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 12 | 11 | 6 | 5 | 0 |
|-----|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|---:|---:|---:|
|     | UART_RX_SCLK_EN | UART_TX_SCLK_EN | UART_RST_CORE | UART_SCLK_SEL | UART_SCLK_DIV_A | UART_SCLK_DIV_NUM | (reserved) | UART_SCLK_DIV_B | 0x1 | 0x0 |    |    | Reset |

UART_SCLK_DIV_B The denominator of the frequency divisor. (R/W)
UART_SCLK_DIV_A The numerator of the frequency divisor. (R/W)
UART_SCLK_DIV_NUM The integral part of the frequency divisor. (R/W)
UART_SCLK_SEL Selects UART clock source. 1: APB_CLK; 2: RC_FAST_CLK; 3: XTAL_CLK. (R/W)
UART_SCLK_EN Set this bit to enable UART TX/RX clock. (R/W)
UART_RST_CORE Write 1 and then write 0 to this bit, to reset UART TX/RX. (R/W)
UART_TX_SCLK_EN Set this bit to enable UART TX clock. (R/W)
UART_RX_SCLK_EN Set this bit to enable UART RX clock. (R/W)

Register 26.19. UART_STATUS_REG (0x001C)

| 31 | 30 | 29 | 28 | 26 | 25 | 16 | 15 | 14 | 13 | 12 | 10 | 9 | 0 |
|-----|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|---:|---:|
|     | UART_TXD | UART_RXD | UART_RTSN | UART_DTRN | (reserved) | UART_TXFIFO_CNT | UART_RXFIFO_CNT | UART_CTSN | UART_DSRN | UART_RTD | UART_RXD | UART_TXD | Reset |

UART_RXFIFO_CNT Stores the number of valid data bytes in RX FIFO. (RO)
UART_DSRN This bit represents the level of the internal UART DSR signal. (RO)
UART_CTSN This bit represents the level of the internal UART CTS signal. (RO)
UART_RXD This bit represents the level of the internal UART RXD signal. (RO)
UART_TXFIFO_CNT Stores the number of data bytes in TX FIFO. (RO)
UART_DTRN This bit represents the level of the internal UART DTR signal. (RO)
UART_RTSN This bit represents the level of the internal UART RTS signal. (RO)
UART_TXD This bit represents the level of the internal UART TXD signal. (RO)
```