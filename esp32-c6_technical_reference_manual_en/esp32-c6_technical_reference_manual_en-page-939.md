

```markdown
Register 29.17: I2C_SCL_STRETCH_CONF_REG (0x0084)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | Reserved                                                                    |
| 30  | I2C_SLAVE_BYTE_ACK_CTL_EN                                                 |
| 29  | I2C_SLAVE_BYTE_ACK_LVL                                                    |
| 28  | I2C_SLAVE_SCL_STRETCH_CLR                                                 |
| 27  | I2C_SLAVE_SCL_STRETCH_EN                                                  |
| 26..0 | I2C_STRETCH_PROTECT_NUM                                                |

I2C_STRETCH_PROTECT_NUM Configures the time period to release the SCL line from stretching to avoid timing violation. Usually it should be larger than the SDA set up time.
Measurement unit: i2c_sclk
(R/W)

I2C_SLAVE_SCL_STRETCH_EN Configures to enable slave SCL stretch function. The SCL output line will be stretched low when I2C_SLAVE_SCL_STRETCH_EN is 1 and stretch event happens. The stretch cause can be seen in I2C_STRETCH_CAUSE.
0: Disable
1: Enable
(R/W)

I2C_SLAVE_SCL_STRETCH_CLR Configures to clear the I2C slave SCL stretch function.
0: No effect
1: Clear
(WT)

I2C_SLAVE_BYTE_ACK_CTL_EN Configures to enable the function for slave to control ACK level.
0: Disable
1: Enable
(R/W)

I2C_SLAVE_BYTE_ACK_LVL Set the ACK level when slave controlling ACK level function enables.
0: Low level
1: High level
(R/W)
```