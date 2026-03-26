

```markdown
Register 44.15. I2C_FILTER_CFG_REG (0x0050)
```

| Bit | Description |
|-----|-------------|
| 31-10 | reserved |
| 9   | I2C_SDA_FILTER_EN |
| 8   | I2C_SCL_FILTER_EN |
| 7   | I2C_SDA_FILTER_THRES |
| 6   | I2C_SCL_FILTER_THRES |
| 5   | Reset |

I2C_SCL_FILTER_THRES Configures the threshold pulse width to be filtered on SCL. When a pulse on the SCL input has smaller width than this register value, the I2C controller will ignore that pulse. Measurement unit: I2C_SCLK clock cycles (R/W)

I2C_SDA_FILTER_THRES Configures the threshold pulse width to be filtered on SDA. When a pulse on the SDA input has smaller width than this register value, the I2C controller will ignore that pulse. Measurement unit: I2C_SCLK clock cycles (R/W)

I2C_SCL_FILTER_EN Configures to enable the filter function for SCL.
0: No effect
1: Enable
(R/W)

I2C_SDA_FILTER_EN Configures to enable the filter function for SDA.
0: No effect
1: Enable
(R/W)
```