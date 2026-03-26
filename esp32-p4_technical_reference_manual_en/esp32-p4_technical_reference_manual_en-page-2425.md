

```markdown
## Register 44.49. LP_I2C_FILTER_CFG_REG (0x0050)

| Bit | Description |
|-----|-------------|
| 31  | (reserved) |
| 10  | LP_I2C_SDA_FILTER_EN |
| 9   | LP_I2C_SCL_FILTER_THRES |
| 8   | LP_I2C_SDA_FILTER_THRES |
| 7   | LP_I2C_SCL_FILTER_THRES |
| 6   | (reserved) |
| 5   | (reserved) |
| 4   | (reserved) |
| 3   | (reserved) |
| 2   | (reserved) |
| 1   | (reserved) |
| 0   | Reset |

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
## Register 44.50. LP_I2C_SCL_SP_CONF_REG (0x0080)

| Bit | Description |
|-----|-------------|
| 31  | (reserved) |
| 29  | reserved |
| 28  | reserved |
| 27  | LP_I2C_SCL_RST_SLV_EN |
| 26  | LP_I2C_SCL_RST_SLV_NUM[4:0] |
| 25  | (reserved) |
| 24  | (reserved) |
| 23  | (reserved) |
| 22  | (reserved) |
| 21  | (reserved) |
| 20  | (reserved) |
| 19  | (reserved) |
| 18  | (reserved) |
| 17  | (reserved) |
| 16  | (reserved) |
| 15  | (reserved) |
| 14  | (reserved) |
| 13  | (reserved) |
| 12  | (reserved) |
| 11  | (reserved) |
| 10  | (reserved) |
| 9   | (reserved) |
| 8   | (reserved) |
| 7   | (reserved) |
| 6   | (reserved) |
| 5   | (reserved) |
| 4   | (reserved) |
| 3   | (reserved) |
| 2   | (reserved) |
| 1   | Reset |

LP_I2C_SCL_RST_SLV_EN Configures to send out SCL pulses when I2C master is IDLE. The number of pulses equals to LP_I2C_SCL_RST_SLV_NUM[4:0]. (R/W/SC)

LP_I2C_SCL_RST_SLV_NUM Configure the pulses of SCL generated in I2C master mode.
Valid when LP_I2C_SCL_RST_SLV_EN is 1.
Measurement unit: i2c_sclk
(R/W)
```