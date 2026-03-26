

```markdown
Register 10.28. HP_SYS_CLKRST_PERI_CLK_CTRL111_REG (0x006C)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     |    |    |    |    | (reserved) | HP_SYS_CLKRST_UART1_CLK_EN | HP_SYS_CLKRST_UART0_SCLK_DIV_NUM | HP_SYS_CLKRST_UART0_SCLK_DIV_DENOMINATOR | HP_SYS_CLKRST_UART0_SCLK_SRC_SEL | HP_SYS_CLKRST_UART0_SCLK_DIV_NUM | HP_SYS_CLKRST_UART0_SCLK_DIV_Numerator | HP_SYS_CLKRST_UART0_SCLK_DIV_DENominator |

0 0 0 0 0 1 0 0 0

HP_SYS_CLKRST_UART0_SCLK_DIV_NUM Configures the integer part of the UART0_SCLK clock divisor. (R/W)

HP_SYS_CLKRST_UART0_SCLK_DIV_Numerator Configures the numerator of the divisor's fractional part for UART0_SCLK. (R/W)

HP_SYS_CLKRST_UART0_SCLK_DIV_DENominator Configures the denominator of the divisor's fractional part for UART0_SCLK. (R/W)

HP_SYS_CLKRST_UART1_CLK_SRC_SEL Configures the clock source for UART1_CLK.
0: XTAL_CLK
1: RC_FAST_CLK
2: PLL_F80M_CLK
3: Invalid
(R/W)

HP_SYS_CLKRST_UART1_CLK_EN Configures whether to enable UART1_CLK.
0: Disable
1: Enable
(R/W)
```