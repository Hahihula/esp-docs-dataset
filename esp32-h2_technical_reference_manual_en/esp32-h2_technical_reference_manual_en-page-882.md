

```markdown
Register 30.17. I2C_SCL_STRETCH_CONF_REG (0x0084)

| Bit | Field Name                     | Description                                                                 |
|-----|---------------------------------|-----------------------------------------------------------------------------|
| 31  | Reserved                       |                                                                             |
| 30  | I2C_SLAVE_BYTE_ACK_CTL_EN     | Configures whether to enable the function for slave to control ACK level.    |
| 29  | I2C_SLAVE_BYTE_ACK_LVL         | Configures the ACK level when slave controlling ACK level function enables.   |
| 28  | I2C_SLAVE_SCL_STRETCH_CLR      | Configures whether or not to clear the I2C slave SCL stretch function.       |
| 27  | I2C_SLAVE_SCL_STRETCH_EN      | Configures whether to enable slave SCL stretch function. The SCL output line will be stretched low when this bit is 1 and a stretch event happens. The stretch cause can be seen in `I2C_STRETCH_CAUSE`. |
| 26  | I2C_STRETCH_PROTECT_NUM        | Configures the time period to release the SCL line from stretching to avoid timing violation. Usually it should be larger than the SDA setup time. Measurement unit: `I2C_SCLK` (R/W) |

- **I2C_STRETCH_PROTECT_NUM**: Configures the time period to release the SCL line from stretching to avoid timing violation. Usually it should be larger than the SDA setup time. Measurement unit: I2C_SCLK (R/W)

- **I2C_SLAVE_SCL_STRETCH_EN**: Configures whether to enable slave SCL stretch function. The SCL output line will be stretched low when this bit is 1 and a stretch event happens. The stretch cause can be seen in `I2C_STRETCH_CAUSE`.
    - 0: Disable
    - 1: Enable (R/W)

- **I2C_SLAVE_SCL_STRETCH_CLR**: Configures whether or not to clear the I2C slave SCL stretch function.
    - 0: No effect
    - 1: Clear (WT)

- **I2C_SLAVE_BYTE_ACK_CTL_EN**: Configures whether to enable the function for slave to control ACK level.
    - 0: Disable
    - 1: Enable (R/W)

- **I2C_SLAVE_BYTE_ACK_LVL**: Configures the ACK level when slave controlling ACK level function enables.
    - 0: Low level
    - 1: High level (R/W)
```