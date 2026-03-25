

```markdown
Register 30.15. I2C_FILTER_CFG_REG (0x0050)
```

| Bit | Description                     |
|-----|---------------------------------|
| 31  | reserved                        |
| 30  | I2C_SCL_FILTER_THRES            |
| 29  | I2C_SDA_FILTER_THRES            |
| 28  | I2C_SCL_FILTER_EN               |
| 27  | I2C_SDA_FILTER_EN               |
| 26  | Reset                           |

I2C_SCL_FILTER_THRES Configures the threshold pulse width to be filtered on SCL. When a pulse on the SCL input has smaller width than this register value, the I2C controller will ignore that pulse. Measurement unit: I2C_SCLK (R/W)

I2C_SDA_FILTER_THRES Configures the threshold pulse width to be filtered on SDA. When a pulse on the SDA input has smaller width than this register value, the I2C controller will ignore that pulse. Measurement unit: I2C_SCLK (R/W)

I2C_SCL_FILTER_EN Configures whether to enable the filter function for SCL.
- 0: No effect
- 1: Enable
(R/W)

I2C_SDA_FILTER_EN Configures whether to enable the filter function for SDA.
- 0: No effect
- 1: Enable
(R/W)
```