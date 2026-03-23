

```markdown
Register 27.39. LP_UART_TOUT_CONF_SYNC_REG (0x0064)
```

| 31 | 12 | 11 | 2 | 1 | 0 |
|----:|----:|----:|---:|---:|---:|
|    |     |     |   |   |   |
| 0x0a | Reset |

LP_UART_RX_TOUT_EN Configures whether or not to enable LP UART receiver's timeout function.
- 0: Disable
- 1: Enable
(R/W)

LP_UART_RX_TOUT_FLOW_DIS Configures whether or not to stop the idle status counter when hardware flow control is enabled.
- 0: Invalid. No effect
- 1: Stop
(R/W)

LP_UART_RX_TOUT_THRD Configures the amount of time that the bus can remain idle before timeout.
Measurement unit: bit time (the time to transmit 1 bit). (R/W)
```