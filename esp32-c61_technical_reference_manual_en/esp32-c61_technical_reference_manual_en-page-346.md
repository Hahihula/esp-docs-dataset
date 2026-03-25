

```markdown
Register 7.11. PCR_I2C_SCLK_CONF_REG (0x0030)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 23  | PCR_I2C_SCLK_EN                                                             |
| 22  | (reserved)                                                                  |
| 21  | PCR_I2C_SCLK_SEL                                                            |
| 20  | PCR_I2C_SCLK_DIV_NUM                                                       |
| 19  | PCR_I2C_SCLK_DIV_B                                                         |
| 12  | PCR_I2C_SCLK_DIV_A                                                         |
| 6   | Reset                                                                      |

PCR_I2C_SCLK_DIV_A Configures the denominator of the divisor's fractional part for I2C functional clock. (R/W)

PCR_I2C_SCLK_DIV_B Configures the numerator of the divisor's fractional part for I2C functional clock. (R/W)

PCR_I2C_SCLK_DIV_NUM Configures the integral part of the divisor for I2C functional clock. (R/W)

PCR_I2C_SCLK_SEL Configures the clock source of I2C.
0 (default): XTAL_CLK
1: RC_FAST_CLK
(R/W)

PCR_I2C_SCLK_EN Configures whether or not to enable I2C functional clock.
0: Not enable
1: Enable
(R/W)
```