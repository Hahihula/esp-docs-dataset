

```markdown
Register 34.16. I2C_SCL_SP_CONF_REG (0x0080)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 7   | I2C_SCL_RST_SLV_EN                                                         |
| 6   | I2C_SDA_PD_EN                                                               |
| 5   | I2C_SCL_PD_EN                                                               |
| 4   | I2C_SCL_RST_SLV_NUM                                                        |
| 3   | (reserved)                                                                  |
| 2   | Reset                                                                      |
| 1   | I2C_SCL_RST_SLV_EN                                                         |
| 0   | I2C_SCL_RST_SLV_NUM                                                        |

I2C_SCL_RST_SLV_EN Configures to send out SCL pulses when I2C master is IDLE. The number of pulses equals to I2C_SCL_RST_SLV_NUM.
- 0: Invalid
- 1: Send out SCL pulses (R/W/SC)

I2C_SCL_RST_SLV_NUM Configure the pulses of SCL generated in I2C master mode.
Valid when I2C_SCL_RST_SLV_EN is 1.
Measurement unit: I2C_SCLK clock cycles (R/W)

I2C_SCL_PD_EN Configures to power down the I2C output SCL line.
- 0: Not power down.
- 1: Not work and power down.
Valid only when I2C_SCL_FORCE_OUT is 1. (R/W)

I2C_SDA_PD_EN Configures to power down the I2C output SDA line.
- 0: Not power down.
- 1: Not work and power down.
Valid only when I2C_SDA_FORCE_OUT is 1. (R/W)
```