

```markdown
Chapter 29 I2C Controller (I2C) GoBack


Register 29.6. I2C_SCL_RSTART_SETUP_REG (0x0044)

| Bit | Description |
|-----|-------------|
| 31-8 | reserved |
| 7-0  | I2C_SCL_RSTART_SETUP_TIME |

I2C_SCL_RSTART_SETUP_TIME Configures the time between the positive edge of SCL and the negative edge of SDA for a RESTART condition.
Measurement unit: i2c_sclk
(R/W)


Register 29.7. I2C_SCL_STOP_HOLD_REG (0x0048)

| Bit | Description |
|-----|-------------|
| 31-8 | reserved |
| 7-0  | I2C_SCL_STOP_HOLD_TIME |

I2C_SCL_STOP_HOLD_TIME Configures the delay after the STOP condition.
Measurement unit: i2c_sclk
(R/W)


Register 29.8. I2C_SCL_STOP_SETUP_REG (0x004C)

| Bit | Description |
|-----|-------------|
| 31-8 | reserved |
| 7-0  | I2C_SCL_STOP_SETUP_TIME |

I2C_SCL_STOP_SETUP_TIME Configures the time between the rising edge of SCL and the rising edge of SDA.
Measurement unit: i2c_sclk
(R/W)
```