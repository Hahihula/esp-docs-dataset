

```markdown
Register 42.14. UART_SLEEP_CONF2_REG (0x0038)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     |    |    |    | (reserved) | UART_WK_MODE_SEL | UART_WK_CHAR_MASK | UART_WK_CHAR_NUM | UART_RX_WAKE_UP_THRD | UART_ACTIVE_THRESHOLD |
| Value | 0x0 | 0x5 | 1 | 0xF0 |

UART_ACTIVE_THRESHOLD Configures the number of RXD edge changes to wake up the chip in wakeup mode 0. (R/W)

UART_RX_WAKE_UP_THRD Configures the number of received data bytes to wake up the chip in wakeup mode 1. (R/W)

UART_WK_CHAR_NUM Configures the number of wakeup characters. (R/W)

UART_WK_CHAR_MASK Configures whether or not to mask wakeup characters.
0: Not mask
1: Mask
(R/W)

UART_WK_MODE_SEL Configures which wakeup mode to select. See Section 42.4.8 Wakeup for the explanation of each mode.
0: Mode 0
1: Mode 1
2: Mode 2
3: Mode 3
(R/W)
```