

```markdown
Register 10.30. HP_SYS_CLKRST_PERI_CLK_CTRL113_REG (0x0074)

| Bit | Field Description                                                                 |
|-----|------------------------------------------------------------------------------------|
| 31  | (reserved)                                                                         |
| 30  | HP_SYS_CLKRST_UART2_SCLK_DIV_NUM                                                   | Configures the integer part of the UART2_SCLK clock divisor. (R/W)               |
| 29  | HP_SYS_CLKRST_UART3_CLK_EN                                                          | Configures whether to enable the UART3_CLK clock.<br>0: Disable<br>1: Enable      |
| 28  | HP_SYS_CLKRST_UART3_CLK_SRC_SEL                                                    | Configures the clock source for UART3_CLK.<br>0: XTAL_CLK<br>1: RC_FAST_CLK<br>2: PLL_F80M_CLK<br>3: Invalid (R/W) |
| 27-24| HP_SYS_CLKRST_UART2_SCLK_DIV_NUMERATOR                                             | Configures the numerator of the fractional part of the UART2_SCLK. (R/W)         |
| 23-16| HP_SYS_CLKRST_UART2_SCLK_DIV_DENOMINATOR                                          | Configures the denominator of the fractional part of the UART2_SCLK. (R/W)       |
| 15-8 | HP_SYS_CLKRST_UART2_SCLK_DIV_NUM                                                   | Configures the integer part of the UART2_SCLK clock divisor.<br>0: Disable<br>1: Enable (R/W) |
```