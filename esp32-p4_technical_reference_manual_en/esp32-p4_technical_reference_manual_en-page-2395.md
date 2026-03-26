

```markdown
Register 44.5. I2C_SCL_START_HOLD_REG (0x0040)

| Bit 31 | Bit 9 | Bit 8 | Bit 0 |
|--------|-------|-------|-------|
| (reserved) |       | Reset |       |

I2C_SCL_START_HOLD_TIME Configures the time between the falling edge of SDA and the falling edge of SCL for a START condition.
Measurement unit: I2C_SCLK clock cycles
(R/W)

Register 44.6. I2C_SCL_RSTART_SETUP_REG (0x0044)

| Bit 31 | Bit 9 | Bit 8 | Bit 0 |
|--------|-------|-------|-------|
| (reserved) |       | Reset |       |

I2C_SCL_RSTART_SETUP_TIME Configures the time between the positive edge of SCL and the negative edge of SDA for a RESTART condition.
Measurement unit: I2C_SCLK clock cycles
(R/W)

Register 44.7. I2C_SCL_STOP_HOLD_REG (0x0048)

| Bit 31 | Bit 9 | Bit 8 | Bit 0 |
|--------|-------|-------|-------|
| (reserved) |       | Reset |       |

I2C_SCL_STOP_HOLD_TIME Configures the delay after the STOP condition.
Measurement unit: I2C_SCLK clock cycles
(R/W)
```