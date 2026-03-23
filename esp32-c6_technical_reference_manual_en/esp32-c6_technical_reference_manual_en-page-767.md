

```markdown
Register 2714. UART_SLEEP_CONF2_REG (0x0038)

| 31 | 28 | 27 | 26 | 25         | 21 | 20 | 18 | 17             | 10 | 9          | 0               |
|----|----|----|----|-------------|----|----|----|----------------|----|------------|-----------------|
|    |    |    |    | UART_WK_MODE_SEL | UART_WK_CHAR_MASK | UART_WK_CHAR_NUM | UART_RX_WAKE_UP_THRD | Reset |

UART_ACTIVE_THRESHOLD Configures the number of RXD edge changes to wake up the chip in wakeup mode 0. (R/W)

UART_RX_WAKE_UP_THRD Configures the number of received data bytes to wake up the chip in wakeup mode 1. (R/W)

UART_WK_CHAR_NUM Configures the number of wakeup characters. (R/W)

UART_WK_CHAR_MASK Configures whether or not to mask wakeup characters.
0: Not mask
1: Mask
(R/W)

UART_WK_MODE_SEL Configures which wakeup mode to select.
0: Mode 0
1: Mode 1
2: Mode 2
3: Mode 3
(R/W)
```