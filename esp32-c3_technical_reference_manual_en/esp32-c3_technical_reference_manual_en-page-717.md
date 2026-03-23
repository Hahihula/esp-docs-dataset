
```markdown
Register 28.16. I2C_CLK_CONF_REG (0x0054)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 30  | I2C_SCLK_ACTIVE                                                              |
| 29  | I2C_SCLK_SEL                                                                 |
| 28  | I2C_SCLK_DIV_B                                                               |
| 27  | I2C_SCLK_DIV_A                                                               |
| 26  | (reserved)                                                                  |
| 25  | (reserved)                                                                  |
| 24  | (reserved)                                                                  |
| 23  | (reserved)                                                                  |
| 22  | (reserved)                                                                  |
| 21  | (reserved)                                                                  |
| 20  | (reserved)                                                                  |
| 19  | (reserved)                                                                  |
| 18  | (reserved)                                                                  |
| 17  | (reserved)                                                                  |
| 16  | (reserved)                                                                  |
| 15  | (reserved)                                                                  |
| 14  | (reserved)                                                                  |
| 13  | (reserved)                                                                  |
| 12  | (reserved)                                                                  |
| 11  | (reserved)                                                                  |
| 10  | (reserved)                                                                  |
| 9   | (reserved)                                                                  |
| 8   | (reserved)                                                                  |
| 7   | I2C_SCLK_DIV_NUM                                                             |

I2C_SCLK_DIV_NUM The integral part of the divisor. (R/W)
I2C_SCLK_DIV_A The numerator of the divisor's fractional part. (R/W)
I2C_SCLK_DIV_B The denominator of the divisor's fractional part. (R/W)
I2C_SCLK_SEL The clock selection bit for the I2C controller. 0: XTAL_CLK; 1: RC_FAST_CLK. (R/W)
I2C_SCLK_ACTIVE The clock switch bit for the I2C controller. (R/W)

Register 28.17. I2C_SCL_SP_CONF_REG (0x0080)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 30  | (reserved)                                                                  |
| 29  | (reserved)                                                                  |
| 28  | (reserved)                                                                  |
| 27  | I2C_SDA_PD_EN                                                                |
| 26  | I2C_SCL_PD_EN                                                                |
| 25  | I2C_SCL_RST_SLV_NUM                                                          |
| 24  | I2C_SCL_RST_SLV_EN                                                           |

I2C_SCL_RST_SLV_EN When the master is idle, set this bit to send out SCL pulses. The number of pulses equals to I2C_SCL_RST_SLV_NUM[4:0]. (R/W/SC)
I2C_SCL_RST_SLV_NUM Configures the pulses of SCL generated in master mode. Valid when I2C_SCL_RST_SLV_EN is 1. (R/W)
I2C_SCL_PD_EN The power down enable bit for the I2C output SCL line. 0: Not power down; 1: Power down. Set I2C_SCL_FORCE_OUT and I2C_SCL_PD_EN to 1 to stretch SCL low. (R/W)
I2C_SDA_PD_EN The power down enable bit for the I2C output SDA line. 0: Not power down; 1: Power down. Set I2C_SDA_FORCE_OUT and I2C_SDA_PD_EN to 1 to stretch SDA low. (R/W)
```