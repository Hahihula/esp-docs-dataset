

```markdown
Register 28.18. I2C_SCL_STRETCH_CONF_REG (0x0084)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | I2C_STRETCH_PROTECT_NUM | I2C_SLAVE_BYTE_ACK_CTL_EN | I2C_SLAVE_SCL_STRETCH_CLR | I2C_SLAVE_SCL_STRETCH_EN |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    | (Reserved) |                    |                          |                        |

I2C_STRETCH_PROTECT_NUM Configures the time period to release the SCL line from stretching to avoid timing violation. Usually it should be larger than the SDA setup time. (R/W)

I2C_SLAVE_SCL_STRETCH_EN The enable bit for SCL clock stretching. 0: Disable; 1: Enable. The SCL output line will be stretched low when I2C_SLAVE_SCL_STRETCH_EN is 1 and one of the four stretching events occurs. The cause of stretching can be seen in I2C_STRETCH_CAUSE. (R/W)

I2C_SLAVE_SCL_STRETCH_CLR Set this bit to clear SCL clock stretching. (WT)

I2C_SLAVE_BYTE_ACK_CTL_EN The enable bit for slave to control the level of the ACK bit. (R/W)

I2C_SLAVE_BYTE_ACK_LVL Set the level of the ACK bit when I2C_SLAVE_BYTE_ACK_CTL_EN is set. (R/W)
```