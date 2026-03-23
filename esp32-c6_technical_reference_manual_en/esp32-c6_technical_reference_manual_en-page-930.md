

```markdown
Chapter 29 I2C Controller (I2C)
GoBack

Register 29.4. I2C_SCL_HIGH_PERIOD_REG (0x0038)

[Diagram: Register bit field layout]
31                                 16     15                         9      8                          0
+--------------------------------------------------------------------------------------------------+
| 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | Reset |
+--------------------------------------------------------------------------------------------------+

I2C_SCL_HIGH_PERIOD Configures for how long SCL remains high in master mode.
Measurement unit: i2c_sclk
(R/W)

I2C_SCL_WAIT_HIGH_PERIOD Configures the SCL FSM's waiting period for SCL high level in master mode.
Measurement unit: i2c_sclk
(R/W)

Register 29.5. I2C_SCL_START_HOLD_REG (0x0040)

[Diagram: Register bit field layout]
31                                 8      0
+---------------------------------------------+
| 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | Reset |
+---------------------------------------------+

I2C_SCL_START_HOLD_TIME Configures the time between the falling edge of SDA and the falling edge of SCL for a START condition.
Measurement unit: i2c_sclk
(R/W)
```