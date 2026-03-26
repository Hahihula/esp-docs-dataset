

```markdown
Register 44.47. LP_I2C_TO_REG (0x000C)
```

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 6   | LP_I2C_TIME_OUT_EN                                                         |
| 5   | LP_I2C_TIME_OUT_VALUE                                                      |
| 4   | Reset                                                                      |

LP_I2C_TIME_OUT_VALUE Configures the timeout threshold period for SCL sticking at high or low level. The actual period is `2^(reg_time_out_value +1) -1`. Measurement unit: i2c_sclk. (R/W)

LP_I2C_TIME_OUT_EN Configures to enable time out control.
0: No effect
1: Enable
(R/W)
```