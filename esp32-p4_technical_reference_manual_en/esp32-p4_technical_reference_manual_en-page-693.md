

```markdown
Register 10.27. HP_SYS_CLKRST_PERI_CLK_CTRL110_REG (0x0068)

| Bit | Field Name                                 | Description                                                                 |
|-----|---------------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                                 |                                                                             |
| 30  | HP_SYS_CLKRST_UART0_CLK_EN                 | Configures whether to enable UART0_CLK.                                    |
| 29  | HP_SYS_CLKRST_LCD_CLK_DIV_NUM              | Configures the integer part of the LCD_CLK clock divisor. (R/W)             |
| 28  | HP_SYS_CLKRST_LCD_CLK_DIV_Numerator        | Configures the numerator of the divisor's fractional part for LCD_CLK. (R/W)|
| 27  | HP_SYS_CLKRST_LCD_CLK_DIV_DENOMINATOR      | Configures the denominator of the divisor's fractional part for LCD_CLK. (R/W)|
| 26  | HP_SYS_CLKRST_UART0_CLK_SRC_SEL            | Configures the clock source for UART0_CLK.<br>0: XTAL_CLK<br>1: RC_FAST_CLK<br>2: PLL_F80M_CLK<br>3: Invalid (R/W) |
| 25  | Reset                                      |                                                                             |
| 24  | HP_SYS_CLKRST_LCD_CLK_DIV_NUM              | Configures the integer part of the LCD_CLK clock divisor. (R/W)             |
| 23  | HP_SYS_CLKRST_LCD_CLK_DIV_Numerator        | Configures the numerator of the divisor's fractional part for LCD_CLK. (R/W)|
| 22  | HP_SYS_CLKRST_LCD_CLK_DIV_DENOMINATOR      | Configures the denominator of the divisor's fractional part for LCD_CLK. (R/W)|
| 21  | HP_SYS_CLKRST_UART0_CLK_SRC_SEL            | Configures the clock source for UART0_CLK.<br>0: XTAL_CLK<br>1: RC_FAST_CLK<br>2: PLL_F80M_CLK<br>3: Invalid (R/W) |
| 20  | Reset                                      |                                                                             |
```