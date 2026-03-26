

```markdown
Register 10.31. HP_SYS_CLKRST_PERI_CLK_CTRL114_REG (0x0078)

| Bit | Field Name                                 | Description                                                                 |
|-----|---------------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                                 |                                                                             |
| 30  | HP_SYS_CLKRST_UART4_CLK_EN                 | Configures whether to enable the UART4_CLK clock. <br> 0: Disable <br> 1: Enable (R/W) |
| 29  | HP_SYS_CLKRST_UART4_UARTA_CLK_SRC_SEL      | Configures the clock source for UART4_CLK. <br> 0: XTAL_CLK <br> 1: RC_FAST_CLK <br> 2: PLL_F80M_CLK <br> 3: Invalid (R/W) |
| 28  | HP_SYS_CLKRST_UART3_SCLK_DIV_NUM           | Configures the integer part of the UART3_SCLK clock divisor. (R/W)            |
| 27  | HP_SYS_CLKRST_UART3_SCLK_DIV_Numerator      | Configures the numerator of the fractional part of the UART3_SCLK. (R/W)     |
| 26  | HP_SYS_CLKRST_UART3_SCLK_DIV_DENOMINATOR   | Configures the denominator of the fractional part of the UART3_SCLK. (R/W)   |
| 25  | (reserved)                                 |                                                                             |
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

HP_SYS_CLKRST_UART3_SCLK_DIV_NUM Configures the integer part of the UART3_SCLK clock divisor. (R/W)

HP_SYS_CLKRST_UART3_SCLK_DIV_Numerator Configures the numerator of the fractional part of the UART3_SCLK. (R/W)

HP_SYS_CLKRST_UART3_SCLK_DIV_DENOMINATOR Configures the denominator of the fractional part of the UART3_SCLK. (R/W)

HP_SYS_CLKRST_UART4_CLK_SRC_SEL Configures the clock source for UART4_CLK.
0: XTAL_CLK
1: RC_FAST_CLK
2: PLL_F80M_CLK
3: Invalid
(R/W)

HP_SYS_CLKRST_UART4_CLK_EN Configures whether to enable the UART4_CLK clock.
0: Disable
1: Enable
(R/W)
```