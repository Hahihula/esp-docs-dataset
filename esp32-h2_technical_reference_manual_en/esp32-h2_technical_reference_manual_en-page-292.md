

```markdown
Register 7.10. PCR_I2C1_SCLK_CONF_REG (0x002C)

| 31 | 23 | 22 | 21 | 20 | 19 | 12 | 11 | 6 | 5 | 0 |
|----|----|----|----|----|----|----|----|---|---|---|
|    |    |    | (reserved) | PCR_I2C1_SCLK_EN<br>(reserved) | PCR_I2C1_SCLK_SEL | PCR_I2C1_SCLK_DIV_NUM | PCR_I2C1_SCLK_DIV_B | PCR_I2C1_SCLK_DIV_A |
| 0 | 0 | 0 | 0 | 0 | 0 | 1 | 0 |   |   | Reset |

PCR_I2C1_SCLK_DIV_A Configures the denominator of the divisor's fractional part for I2C1 functional clock. (R/W)

PCR_I2C1_SCLK_DIV_B Configures the numerator of the divisor's fractional part for I2C1 functional clock. (R/W)

PCR_I2C1_SCLK_DIV_NUM Configures the integral part of the divisor for I2C1 functional clock. (R/W)

PCR_I2C1_SCLK_SEL Configures the clock source of I2C1.
  O (default): XTAL_CLK
  1: RC_FAST_CLK
(R/W)

PCR_I2C1_SCLK_EN Configures whether or not to enable I2C1 functional clock.
  O: Not enable
  1: Enable
(R/W)
```