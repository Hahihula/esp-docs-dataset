

```markdown
Register 10.17. HP_SYS_CLKRST_PERI_CLK_CTRL10_REG (0x0040)

| Bit | Field Name                                 | Description                                                                 |
|-----|---------------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                                 |                                                                             |
| 30  | HP_SYS_CLKRST_I2C1_CLK_EN                  | Enables I2C1 clock.                                                         |
| 29  | HP_SYS_CLKRST_I2C1_CLK_SRC_SEL             | Configures the clock source for I2C1_CLK.<br>0: XTAL_CLK<br>1: RC_FAST_CLK (R/W) |
| 28  | HP_SYS_CLKRST_I2CO_CLK_DIV_NUMENATOR       | Configures the numerator of fractional part of I2CO_CLK's clock divider.    |
| 27  | HP_SYS_CLKRST_I2CO_CLK_DIV_DENOMINATOR     | Configures the denominator of fraction part for divisor of I2CO_CLK.        |
| 26  | HP_SYS_CLKRST_I2CO_CLK_SRC_SEL             | Configures clock source for I2CO_CLK.<br>0: XTAL_CLK<br>1: RC_FAST_CLK (R/W) |
| 25  | HP_SYS_CLKRST_I2CO_CLK_EN                  | Enables/disables I2CO_CLK.                                                  |
| 24  | (reserved)                                 |                                                                             |
| 23  | (reserved)                                 |                                                                             |
| 22  | (reserved)                                 |                                                                             |
| 21  | (reserved)                                 |                                                                             |
| 20  | (reserved)                                 |                                                                             |
| 19  | (reserved)                                 |                                                                             |
| 18  | (reserved)                                 |                                                                             |
| 17  | (reserved)                                 |                                                                             |
| 16  | (reserved)                                 |                                                                             |
| 15  | (reserved)                                 |                                                                             |
| 14  | (reserved)                                 |                                                                             |
| 13  | (reserved)                                 |                                                                             |
| 12  | (reserved)                                 |                                                                             |
| 11  | (reserved)                                 |                                                                             |
| 10  | (reserved)                                 |                                                                             |
| 9   | (reserved)                                 |                                                                             |
| 8   | (reserved)                                 |                                                                             |
| 7   | (reserved)                                 |                                                                             |
| 6   | (reserved)                                 |                                                                             |
| 5   | (reserved)                                 |                                                                             |
| 4   | (reserved)                                 |                                                                             |
| 3   | (reserved)                                 |                                                                             |
| 2   | (reserved)                                 |                                                                             |
| 1   | (reserved)                                 |                                                                             |
| 0   | Reset                                      |                                                                             |

HP_SYS_CLKRST_I2CO_CLK_SRC_SEL Configures the clock source for I2CO_CLK.
O: XTAL_CLK
1: RC_FAST_CLK
(R/W)

HP_SYS_CLKRST_I2CO_CLK_EN Configures whether to enable I2CO_CLK.
O: Disable
1: Enable
(R/W)

HP_SYS_CLKRST_I2CO_CLK_DIV_NUM Configures the integer part of the clock divisor of I2CO_CLK. (R/W)

HP_SYS_CLKRST_I2CO_CLK_DIV_NUMENATOR Configures the numerator of the divisor's fractional part for clock divisor of I2CO_CLK. (R/W)

HP_SYS_CLKRST_I2CO_CLK_DIV_DENOMINATOR Configures the denominator of the divisor's fractional part for clock divisor of I2CO_CLK. (R/W)

HP_SYS_CLKRST_I2C1_CLK_SRC_SEL Configures the clock source for I2C1_CLK.
O: XTAL_CLK
1: RC_FAST_CLK
(R/W)

HP_SYS_CLKRST_I2C1_CLK_EN Configures whether to enable I2C1_CLK.
O: Disable
1: Enable
(R/W)
```