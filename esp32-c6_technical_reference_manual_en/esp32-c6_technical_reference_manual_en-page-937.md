

```markdown
Register 29.15. I2C_FILTER_CFG_REG (0x0050)
```

| Bit | Description                |
|-----|----------------------------|
| 31  | (reserved)                 |
| 30  | O                          |
| 29  | O                          |
| ... | ...                        |
| 8   | I2C_SDA_FILTER_EN          |
| 7   | I2C_SCL_FILTER_EN          |
| 6   | I2C_SDA_FILTER_THRES       |
| 5   | I2C_SCL_FILTER_THRES       |
| 4   | O                          |
| 3   | O                          |
| 2   | O                          |
| 1   | Reset                      |
| 0   | O                          |

I2C_SCL_FILTER_THRES Configures the threshold pulse width to be filtered on SCL. When a pulse on the SCL input has smaller width than this register value, the I2C controller will ignore that pulse. Measurement unit: i2c_sclk (R/W)

I2C_SDA_FILTER_THRES Configures the threshold pulse width to be filtered on SDA. When a pulse on the SDA input has smaller width than this register value, the I2C controller will ignore that pulse. Measurement unit: i2c_sclk (R/W)

I2C_SCL_FILTER_EN Configures to enable the filter function for SCL.
O: No effect
1: Enable
(R/W)

I2C_SDA_FILTER_EN Configures to enable the filter function for SDA.
O: No effect
1: Enable
(R/W)
```