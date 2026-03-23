

```markdown
Register 28.12. I2C_TO_REG (0x000C)

| Bit | Description                     |
|-----|---------------------------------|
| 31  | (reserved)                      |
| 6   | 5                               | 4                               | 0                               |
|     |                                 |                                 |                                 |
| 0   | I2C_TIME_OUT_VALUE             |                                 |                                 |
|     |                                 |                                 |                                 |

I2C_TIME_OUT_VALUE This field is used to configure the timeout value for receiving a data bit in I2C_SCLK clock cycles. The configured timeout value equals `2^I2C_TIME_OUT_VALUE` clock cycles. (R/W)

I2C_TIME_OUT_EN This is the enable bit for timeout control. (R/W)


Register 28.13. I2C_SLAVE_ADDR_REG (0x0010)

| Bit | Description                     |
|-----|---------------------------------|
| 31  | 30                              | 15                               | 14                              | 0                               |
|     |                                 |                                 |                                 |                                 |
| 0   | I2C_SLAVE_ADDR                 |                                 |                                 |                                 |

I2C_SLAVE_ADDR When the I2C controller is in slave mode, this field is used to configure the slave address. (R/W)

I2C_ADDR_10BIT_EN This field is used to enable the 10-bit addressing mode in master mode. (R/W)
```