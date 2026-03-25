

```markdown
Register 30.4. I2C_SCL_HIGH_PERIOD_REG (0x0038)

| Bit | Description                |
|-----|----------------------------|
| 15-9| I2C_SCL_WAIT_HIGH_PERIOD   |
| 8-0 | I2C_SCL_HIGH_PERIOD        |

I2C_SCL_HIGH_PERIOD Configures for how long SCL remains high in Master mode.
Measurement unit: I2C_SCLK
(R/W)

I2C_SCL_WAIT_HIGH_PERIOD Configures the SCL FSM's waiting period for SCL high level in Master mode.
Measurement unit: I2C_SCLK
(R/W)


Register 30.5. I2C_SCL_START_HOLD_REG (0x0040)

| Bit | Description                     |
|-----|---------------------------------|
| 8-0 | I2C_SCL_START_HOLD_TIME         |

I2C_SCL_START_HOLD_TIME Configures the time between the falling edge of SDA and the falling edge of SCL for a START condition.
Measurement unit: I2C_SCLK
(R/W)
```