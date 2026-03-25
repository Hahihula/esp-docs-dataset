

```markdown
Register 34.43. LP_I2C_SCL_STOP_SETUP_REG (0x004C)

LP_I2C_SCL_STOP_SETUP_TIME Configures the time between the rising edge of SCL and the rising edge of SDA.
Measurement unit: I2C_SCLK clock cycles
(R/W)
```

```markdown
Register 34.44. LP_I2C_SCL_ST_TIME_OUT_REG (0x0078)

LP_I2C_SCL_ST_TO_I2C Configures the threshold value of SCL_FSM state unchanged period. It should be no more than 23.
Measurement unit: I2C_SCLK clock cycles
(R/W)
```

```markdown
Register 34.45. LP_I2C_SCL_MAIN_ST_TIME_OUT_REG (0x007C)

LP_I2C_SCL_MAIN_ST_TO_I2C Configures the threshold value of SCL_MAIN_FSM state unchanged period. It should be no more than 23.
Measurement unit: I2C_SCLK clock cycles
(R/W)
```