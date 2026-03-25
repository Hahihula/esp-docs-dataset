

```markdown
Register 34.49. LP_I2C_FILTER_CFG_REG (0x0050)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 10  | LP_I2C_SDA_FILTER_EN                                                       |
| 9   | LP_I2C_SCL_FILTER_EN                                                       |
| 7   | LP_I2C_SDA_FILTER_THRES                                                   |
| 4   | LP_I2C_SCL_FILTER_THRES                                                   |
| 3   | (reserved)                                                                 |
| 0   | Reset                                                                      |

LP_I2C_SCL_FILTER_THRES Configures the threshold pulse width to be filtered on SCL. When a pulse on the SCL input has smaller width than this value, the I2C controller will ignore that pulse.
Measurement unit: I2C_SCLK clock cycles
(R/W)

LP_I2C_SDA_FILTER_THRES Configures the threshold pulse width to be filtered on SDA. When a pulse on the SDA input has smaller width than this value, the I2C controller will ignore that pulse.
Measurement unit: I2C_SCLK clock cycles
(R/W)

LP_I2C_SCL_FILTER_EN Configures to enable the filter function for SCL.
0: No effect
1: Enable
(R/W)

LP_I2C_SDA_FILTER_EN Configures to enable the filter function for SDA.
0: No effect
1: Enable
(R/W)
```