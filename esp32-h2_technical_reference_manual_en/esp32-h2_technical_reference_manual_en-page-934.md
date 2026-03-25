

```markdown
Register 31.16. I2S_LC_HUNG_CONF_REG (0x0060)

| Bit | Name                                 | Description                                                                 |
|-----|--------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                          |                                                                             |
| 12  | I2S_LC_FIFO_TIMEOUT_ENA            | Configures whether to enable FIFO timeout.                                  |
| 11  | I2S_LC_FIFO_TIMEOUT_SHIFT          | Configures the tick counter threshold.                                      |
| 10  | (reserved)                          |                                                                             |
| 8   | I2S_LC_FIFO_TIMEOUT                 | Configures FIFO timeout threshold.                                          |
| 7   | (reserved)                          |                                                                             |
| 6   | (reserved)                          |                                                                             |
| 5   | (reserved)                          |                                                                             |
| 4   | (reserved)                          |                                                                             |
| 3   | (reserved)                          |                                                                             |
| 2   | (reserved)                          |                                                                             |
| 1   | (reserved)                          |                                                                             |
| 0   | Reset                                | 0x10                                                                          |

I2S_LC_FIFO_TIMEOUT Configures FIFO timeout threshold. The FIFO hung counter is incremented by one each time I2S is in an error state and the tick counter reaches its threshold. I2S_TX_HUNG_INT or I2S_RX_HUNG_INT interrupt will be triggered when FIFO hung counter is equal to the FIFO timeout threshold. (R/W)

I2S_LC_FIFO_TIMEOUT_SHIFT Configures the tick counter threshold. The tick counter is incremented by one each time I2S is in an error state and it is on the rising edge in each system clock (APB). The tick counter is reset when counter value >= 88000/2^I2S_LC_FIFO_TIMEOUT_SHIFT. (R/W)

I2S_LC_FIFO_TIMEOUT_ENA Configures whether to enable FIFO timeout.
0: Disable
1: Enable
(R/W)
```

```markdown
Register 31.17. I2S_CONF_SIGLE_DATA_REG (0x0068)

| Bit | Name                  | Description                                                                 |
|-----|-----------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)            |                                                                             |
| 0   | I2S_SINGLE_DATA       | Configures constant channel data to be sent out. (R/W)                       |

I2S_SINGLE_DATA Configures constant channel data to be sent out. (R/W)
```