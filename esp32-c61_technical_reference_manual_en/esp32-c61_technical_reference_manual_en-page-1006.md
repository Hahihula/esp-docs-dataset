

```markdown
Register 27.15. I2C_FILTER_CFG_REG (0x0050)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 30  | (reserved)                                                                  |
| 29  | (reserved)                                                                  |
| 28  | (reserved)                                                                  |
| 27  | (reserved)                                                                  |
| 26  | (reserved)                                                                  |
| 25  | (reserved)                                                                  |
| 24  | (reserved)                                                                  |
| 23  | (reserved)                                                                  |
| 22  | (reserved)                                                                  |
| 21  | (reserved)                                                                  |
| 20  | (reserved)                                                                  |
| 19  | (reserved)                                                                  |
| 18  | (reserved)                                                                  |
| 17  | I2C_SCL_FILTER_THRES                                                       |
| 16  | I2C_SDA_FILTER_THRES                                                       |
| 15  | I2C_SCL_FILTER_EN                                                          |
| 14  | I2C_SDA_FILTER_EN                                                          |
| 13  | (reserved)                                                                  |
| 12  | (reserved)                                                                  |
| 11  | (reserved)                                                                  |
| 10  | (reserved)                                                                  |
| 9   | (reserved)                                                                  |
| 8   | (reserved)                                                                  |
| 7   | (reserved)                                                                  |
| 6   | (reserved)                                                                  |
| 5   | (reserved)                                                                  |
| 4   | (reserved)                                                                  |
| 3   | (reserved)                                                                  |
| 2   | (reserved)                                                                  |
| 1   | (reserved)                                                                  |
| 0   | Reset                                                                      |

I2C_SCL_FILTER_THRES Configures the threshold pulse width to be filtered on SCL. When a pulse on the SCL input has smaller width than this register value, the I2C controller will ignore that pulse. Measurement unit: I2C_SCLK clock cycles (R/W)

I2C_SDA_FILTER_THRES Configures the threshold pulse width to be filtered on SDA. When a pulse on the SDA input has smaller width than this register value, the I2C controller will ignore that pulse. Measurement unit: I2C_SCLK clock cycles (R/W)

I2C_SCL_FILTER_EN Configures to enable the filter function for SCL.
O: No effect
1: Enable
(R/W)

I2C_SDA_FILTER_EN Configures to enable the filter function for SDA.
O: No effect
1: Enable
(R/W)
```