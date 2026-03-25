

```markdown
Register 34.47. LP_I2C_TO_REG (0x000C)

LP_I2C_TIME_OUT_VALUE Configures the timeout threshold period for SCL sticking at high or low level. The actual period is 2^(LP_I2C_TIME_OUT_VALUE+1)-1.
Measurement unit: I2C_SCLK clock cycles.
(R/W)

LP_I2C_TIME_OUT_EN Configures to enable time out control.

0: No effect
1: Enable
(R/W)
```