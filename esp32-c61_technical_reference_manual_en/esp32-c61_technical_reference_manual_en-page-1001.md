

```markdown
Register 2710. I2C_SCL_MAIN_ST_TIME_OUT_REG (0x007C)

I2C_SCL_MAIN_ST_TO_I2C Configures the threshold value of SCL_MAIN_FSM state unchanged period. It should be no more than 23. The actual period is 2^(I2C_SCL_MAIN_ST_TO_I2C+1)-1.
Measurement unit: I2C_SCLK clock cycles
(R/W)
```