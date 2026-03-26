

```markdown
Register 42.55. LP_UART_IDLE_CONF_SYNC_REG (0x0048)

| Bit | Description |
|-----|-------------|
| 31-20 | (reserved) |
| 19   | LP_UART_TX_IDLE_NUM |
| 10   | LP_UART_RX_IDLE_THRHD |
| 9    | Reset |

LP_UART_RX_IDLE_THRHD Configures the threshold to generate a frame end signal when the receiver takes more time to receive one data byte data.
Measurement unit: bit time (the time to transmit 1 bit). (R/W)

LP_UART_TX_IDLE_NUM Configures the interval between two data transfers.
Measurement unit: bit time (the time to transmit 1 bit). (R/W)

Register 42.56. LP_UART_CLK_CONF_REG (0x0088)

| Bit | Description |
|-----|-------------|
| 31-27 | (reserved) |
| 26   | LP_UART_TX_RST_CORE |
| 25   | LP_UART_RX_RST_CORE |
| 24   | LP_UART_TX_SCLK_EN |
| 23   | LP_UART_RX_SCLK_EN |
| 22-0 | (reserved) |

LP_UART_TX_SCLK_EN Configures whether or not to enable LP UART TX clock.
0: Disable
1: Enable
(R/W)

LP_UART_RX_SCLK_EN Configures whether or not to enable LP UART RX clock.
0: Disable
1: Enable
(R/W)

LP_UART_TX_RST_CORE Write 1 and then write 0 to reset LP UART TX. (R/W)

LP_UART_RX_RST_CORE Write 1 and then write 0 to reset LP UART RX. (R/W)
```