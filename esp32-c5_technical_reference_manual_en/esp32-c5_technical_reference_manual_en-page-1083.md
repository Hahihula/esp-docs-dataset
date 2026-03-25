

```markdown
Register 32.55. LP_UART_IDLE_CONF_SYNC_REG (0x0048)

| Bit Range | Description                                                                 |
|-----------|-----------------------------------------------------------------------------|
| 31        | (reserved)                                                                  |
| 20-19     | LP_UART_TX_IDLE_NUM                                                         |
| 10-9      | LP_UART_RX_IDLE_THRHD                                                       |
| 0         | Reset                                                                       |

LP_UART_RX_IDLE_THRHD Configures the threshold to generate a frame end signal when the receiver takes more time to receive one data byte data.
Measurement unit: bit time (the time to transmit 1 bit). (R/W)

LP_UART_TX_IDLE_NUM Configures the interval between two data transfers.
Measurement unit: bit time (the time to transmit 1 bit). (R/W)

Register 32.56. LP_UART_DELAY_CONF_SYNC_REG (0x004C)

| Bit Range | Description                                                                 |
|-----------|-----------------------------------------------------------------------------|
| 31        | (reserved)                                                                  |
| 3         | LP_UART_DL1_EN                                                              |
| 2         | LP_UART_DLO_EN                                                               |
| 1-0       | Reset                                                                       |

LP_UART_DLO_EN Configures whether to add a turnaround delay of 1 bit before the start bit.
0: Not add
1: Add
(R/W)

LP_UART_DL1_EN Configures whether to add a turnaround delay of 1 bit after the stop bit.
0: Not add
1: Add
(R/W)
```