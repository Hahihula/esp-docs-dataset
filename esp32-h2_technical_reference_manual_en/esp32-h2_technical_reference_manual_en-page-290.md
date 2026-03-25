

```markdown
Register 7.8. PCR_I2CO_SCLK_CONF_REG (0x0024)

| Bit | Field Name                  | Description                                                                 |
|-----|-----------------------------|-----------------------------------------------------------------------------|
| 31  | reserved                    |                                                                             |
| 23  | PCR_I2CO_SCLK_DIV_A         | Configures the denominator of the divisor's fractional part for I2CO functional clock. (R/W) |
| 22  |                             |                                                                             |
| 21  |                             |                                                                             |
| 20  | PCR_I2CO_SCLK_SEL           | Configures the clock source of I2CO.<br>0 (default): XTAL_CLK<br>1: RC_FAST_CLK (R/W) |
| 19  | reserved                    |                                                                             |
| 12  | PCR_I2CO_SCLK_DIV_NUM       | Configures the integral part of the divisor for I2CO functional clock. (R/W)   |
| 11  |                             |                                                                             |
| 6   | PCR_I2CO_SCLK_DIV_B         | Configures the numerator of the divisor's fractional part for I2CO functional clock. (R/W) |
| 5   |                             |                                                                             |
| 0   | PCR_I2CO_SCLK_EN            | Configures whether or not to enable I2CO functional clock.<br>0: Not enable<br>1: Enable (R/W) |

PCR_I2CO_SCLK_DIV_A Configures the denominator of the divisor's fractional part for I2CO functional clock. (R/W)

PCR_I2CO_SCLK_DIV_B Configures the numerator of the divisor's fractional part for I2CO functional clock. (R/W)

PCR_I2CO_SCLK_DIV_NUM Configures the integral part of the divisor for I2CO functional clock. (R/W)

PCR_I2CO_SCLK_SEL Configures the clock source of I2CO.
0 (default): XTAL_CLK
1: RC_FAST_CLK
(R/W)

PCR_I2CO_SCLK_EN Configures whether or not to enable I2CO functional clock.
0: Not enable
1: Enable
(R/W)
```