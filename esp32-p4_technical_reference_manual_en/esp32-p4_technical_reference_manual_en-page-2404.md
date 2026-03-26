

```markdown
Register 44.17. I2C_SCL_STRETCH_CONF_REG (0x0084)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | Reserved                                                                     |
| 30-0| 0                                                                             |

I2C_STRETCH_PROTECT_NUM Configures the time period to release the SCL line from stretching<br>to avoid timing violation. Usually it should be larger than the SDA setup time.<br>Measurement unit: I2C_SCLK clock cycles<br>(R/W)

I2C_SLAVE_SCL_STRETCH_EN Configures to enable slave SCL stretch function. The SCL output<br>line will be stretched low when I2C_SLAVE_SCL_STRETCH_EN is 1 and a stretch event happens.<br>The stretch cause can be seen in I2C_STRETCH_CAUSE.<br>0: Disable<br>1: Enable<br>(R/W)

I2C_SLAVE_SCL_STRETCH_CLR Configures to clear the I2C slave SCL stretch function.<br>0: No effect<br>1: Clear<br>(WT)

I2C_SLAVE_BYTE_ACK_CTL_EN Configures to enable the function for the slave to control ACK<br>level.<br>0: Disable<br>1: Enable<br>(R/W)

I2C_SLAVE_BYTE_ACK_LVL Configures the ACK level when slave controlling ACK level function is<br>enabled.<br>0: Low level<br>1: High level<br>(R/W)
```