

```markdown
Register 29.49. LP_I2C_FILTER_CFG_REG (0x0050)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 10  | LP_I2C_SDA_FILTER_EN                                                       |
| 9   | LP_I2C_SCL_FILTER_THRES                                                   |
| 8   | LP_I2C_SDA_FILTER_EN                                                       |
| 7   | LP_I2C_SCL_FILTER_THRES                                                   |
| 6-4 | (reserved)                                                                  |
| 3   | LP_I2C_SCL_FILTER_THRES                                                   |
| 2   | LP_I2C_SDA_FILTER_THRES                                                   |
| 1   | Reset                                                                      |

LP_I2C_SCL_FILTER_THRES Configures the threshold pulse width to be filtered on SCL. When a pulse on the SCL input has smaller width than this value, the I2C controller will ignore that pulse.
Measurement unit: i2c_sclk
(R/W)

LP_I2C_SDA_FILTER_THRES Configures the threshold pulse width to be filtered on SDA. When a pulse on the SDA input has smaller width than this value, the I2C controller will ignore that pulse.
Measurement unit: i2c_sclk
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

```markdown
Register 29.50. LP_I2C_SCL_SP_CONF_REG (0x0080)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 30-24| (reserved)                                                                  |
| 7   | LP_I2C_SCL_RST_SLV_NUM                                                      |
| 6   | LP_I2C_SCL_RST_SLV_EN                                                      |
| 5   | LP_I2C_SCL_RST_SLV_EN                                                      |
| 4   | LP_I2C_SCL_RST_SLV_EN                                                      |
| 3-0 | (reserved)                                                                  |

LP_I2C_SCL_RST_SLV_EN Configures to send out SCL pulses when I2C master is IDLE. The number of pulses equals to LP_I2C_SCL_RST_SLV_NUM[4:0]. (R/W/SC)

LP_I2C_SCL_RST_SLV_NUM Configure the pulses of SCL generated in I2C master mode.
Valid when LP_I2C_SCL_RST_SLV_EN is 1.
Measurement unit: i2c_sclk
(R/W)
```