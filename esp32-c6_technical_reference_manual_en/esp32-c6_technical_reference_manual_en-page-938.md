

```markdown
Register 29.16. I2C_SCL_SP_CONF_REG (0x0080)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 30  | I2C_SCL_RST_SLV_EN                                                          |
| 29  | I2C_SCL_RST_SLV_NUM                                                         |
| 28  | I2C_SCL_PD_EN                                                               |
| 27  | I2C_SDA_PD_EN                                                               |
| 26  | (reserved)                                                                  |
| 25  | Reset                                                                      |
| ... | ...                                                                        |

I2C_SCL_RST_SLV_EN Configures to send out SCL pulses when I2C master is IDLE. The number of pulses equals to I2C_SCL_RST_SLV_NUM[4:0]. (R/W/SC)

I2C_SCL_RST_SLV_NUM Configure the pulses of SCL generated in I2C master mode.
Valid when I2C_SCL_RST_SLV_EN is 1.
Measurement unit: i2c_sclk
(R/W)

I2C_SCL_PD_EN Configures to power down the I2C output SCL line.
0: Not power down.
1: Not work and power down.
Valid only when I2C_SCL_FORCE_OUT is 1. (R/W)

I2C_SDA_PD_EN Configures to power down the I2C output SDA line.
0: Not power down.
1: Not work and power down.
Valid only when I2C_SDA_FORCE_OUT is 1. (R/W)
```