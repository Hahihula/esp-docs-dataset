

```markdown
Register 27.8. I2C_SCL_STOP_SETUP_REG (0x004C)

| Bit 31 | Bits 9:8 | Bit 7-0       |
|--------|----------|---------------|
|   0    |     Reset|               |

I2C_SCL_STOP_SETUP_TIME Configures the time between the rising edge of SCL and the rising edge of SDA.
Measurement unit: I2C_SCLK clock cycles
(R/W)

Register 27.9. I2C_SCL_ST_TIME_OUT_REG (0x0078)

| Bit 31 | Bits 5:4 | Bit 3-0 |
|--------|----------|---------|
|   0    |     Reset| 0x10    |

I2C_SCL_ST_TO_I2C Configures the threshold value of SCL_FSM state unchanged period. It should be no more than 23, more than 1.
Maximum Clock Cycle Threshold = 2^I2C_SCL_ST_TO_I2C+1 - 1
Measurement unit: I2C_SCLK clock cycles
(R/W)
```