

```markdown
Register 34.8. I2C_SCL_STOP_SETUP_REG (0x004C)

| 31 | 9 | 8 | ... | 0 |
|-----|----|----|-----|---|
| 0   |    |    |     | Reset |

I2C_SCL_STOP_SETUP_TIME Configures the time between the rising edge of SCL and the rising edge of SDA.
Measurement unit: I2C_SCLK clock cycles
(R/W)

Register 34.9. I2C_SCL_ST_TIME_OUT_REG (0x0078)

| 31 | ... | 5 | 4 | 0 |
|-----|------|----|---|---|
| 0   |      |    | Ox10 | Reset |

I2C_SCL_ST_TO_I2C Configures the threshold value of SCL_FSM state unchanged period. It should be no more than 23, more than 1.
Maximum Clock Cycle Threshold = 2^I2C_SCL_ST_TO_I2C + 1 - 1
Measurement unit: I2C_SCLK clock cycles
(R/W)
```