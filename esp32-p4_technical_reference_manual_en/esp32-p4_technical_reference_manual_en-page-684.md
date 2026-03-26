

```markdown
Register 1018. HP_SYS_CLKRST_PERI_CLK_CTRL11_REG (0x0044)

| Bit | Field Name                                 | Description                                                                 |
|-----|---------------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                                 |                                                                             |
| 30  | HP_SYS_CLKRST_I2SO_RX_CLK_SRC_SEL          | Configures the clock source for I2SO_RX_CLK.                                |
|     |                                             | 0: XTAL_CLK                                                                  |
|     |                                             | 1: APLL_CLK                                                                  |
|     |                                             | 2: PAD_I2SO_MCLK                                                             |
|     |                                             | 3: Invalid                                                                   |
| (R/W) |                                         |                                                                             |
| 29  | HP_SYS_CLKRST_I2SO_RX_CLK_EN               | Configures whether to enable I2SO_RX_CLK.                                  |
|     |                                             | 0: Disable                                                                  |
|     |                                             | 1: Enable                                                                   |
| (R/W) |                                         |                                                                             |
| 28-24| HP_SYS_CLKRST_I2C1_CLK_DIV_NUM             | Configures the integer part of the I2C1_CLK clock divisor.                  |
| (R/W)|                                         |                                                                             |
| 23-16| HP_SYS_CLKRST_I2C1_CLK_DIV_Numerator       | Configures the numerator of the divisor’s fractional part for I2C1_CLK clock divisor. (R/W) |
|     |                                             |                                                                             |
| 15-8 | HP_SYS_CLKRST_I2C1_CLK_DIV_Denominator     | Configures the denominator of the divisor’s fractional part for I2C1_CLK clock divisor. (R/W) |
| (R/W)|                                         |                                                                             |
```