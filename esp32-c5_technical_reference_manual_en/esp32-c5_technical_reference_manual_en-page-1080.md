

```markdown
Register 32.51. LP_UART_SLEEP_CONF2_REG (0x0038)

| Bit | 31 | 28 | 27 | 26 | 25 | 21 | 20 | 18 | 17 | 13 | 12 | 10 | 9 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|---|---|
|     |    | (reserved) | LP_UART_WK_MODE_SEL | LP_UART_WK_CHAR_MASK | LP_UART_WK_CHAR_NUM | LP_UART_RX_WAKE_UP_THRD | (reserved) | LP_UART_ACTIVE_THRESHOLD |
| Value | 0 | 0 | 0 | 0x0 | 0x5 | 1 | 0 | 0 | 0 | 0x10 |

LP_UART_ACTIVE_THRESHOLD Configures the number of RXD edge changes to wake up the chip in wakeup mode 0. (R/W)

LP_UART_RX_WAKE_UP_THRD Configures the number of received data bytes to wake up the chip in wakeup mode 1. (R/W)

LP_UART_WK_CHAR_NUM Configures the number of wakeup characters. (R/W)

LP_UART_WK_CHAR_MASK Configures whether or not to mask wakeup characters.
0: Not mask
1: Mask
(R/W)

LP_UART_WK_MODE_SEL Configures which wakeup mode to select.
0: Mode 0
1: Mode 1
2: Mode 2
3: Mode 3
(R/W)
```