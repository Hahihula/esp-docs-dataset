

```markdown
Register 32.53. LP_UART_SWFC_CONF1_REG (0x0040)

| Bit | Description                |
|-----|----------------------------|
| 15  | LP_UART_XOFF_THRESHOLD     |
| 11  | (reserved)                 |
| 8   | (reserved)                 |
| 7   | (reserved)                 |
| 3   | LP_UART_XON_THRESHOLD      |
| 2   | (reserved)                 |
| 0   | Reset                      |

LP_UART_XON_THRESHOLD Configures the threshold for data in RX FIFO to send XON characters in software flow control.
Measurement unit: byte. (R/W)

LP_UART_XOFF_THRESHOLD Configures the threshold for data in RX FIFO to send XOFF characters in software flow control.
Measurement unit: byte. (R/W)
```

```markdown
Register 32.54. LP_UART_TXBRK_CONF_SYNC_REG (0x0044)

| Bit | Description                |
|-----|----------------------------|
| 7   | (reserved)                 |
| 0   | LP_UART_TX_BRK_NUM         |

LP_UART_TX_BRK_NUM Configures the number of NULL characters to be sent after finishing data transmission.
Valid only when LP_UART_TXD_BRK is 1. (R/W)
```