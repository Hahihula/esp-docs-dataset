

```markdown
## Register 42.16. UART_SWFC_CONF1_REG (0x0040)

| Bit Range | Field Name             | Description                                                                 |
|-----------|------------------------|-----------------------------------------------------------------------------|
| 31-8      | reserved               |                                                                             |
| 7-0       | UART_XON_THRESHOLD     | Configures the threshold for data in RX FIFO to send XON characters in software flow control. Measurement unit: byte. (R/W) |
|           |                        |                                                                             |
| 7-0       | UART_XOFF_THRESHOLD    | Configures the threshold for data in RX FIFO to send XOFF characters in software flow control. Measurement unit: byte. (R/W) |

## Register 42.17. UART_TXBRK_CONF_SYNC_REG (0x0044)

| Bit Range | Field Name             | Description                                                                 |
|-----------|------------------------|-----------------------------------------------------------------------------|
| 31-8      | reserved               |                                                                             |
| 7-0       | UART_TX_BRK_NUM        | Configures the number of NULL characters to be sent after finishing data transmission. Valid only when UART_TXD_BRK is 1. (R/W) |

## Register 42.18. UART_IDLE_CONF_SYNC_REG (0x0048)

| Bit Range | Field Name             | Description                                                                 |
|-----------|------------------------|-----------------------------------------------------------------------------|
| 31-20     | reserved               |                                                                             |
| 19-10     | UART_RX_IDLE_THRDH     | Configures the threshold to generate a frame end signal when the receiver takes more time to receive one data byte data. Measurement unit: bit time (the time to transmit 1 bit). (R/W) |
| 9-0       | UART_TX_IDLE_NUM       | Configures the interval between two data transfers. Measurement unit: bit time (the time to transmit 1 bit). (R/W) |
```