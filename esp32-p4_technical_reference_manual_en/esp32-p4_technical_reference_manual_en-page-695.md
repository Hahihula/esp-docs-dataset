

```markdown
Register 10.29. HP_SYS_CLKRST_PERI_CLK_CTRL112_REG (0x0070)

| Bit | Field Name                                 | Description                                                                 |
|-----|---------------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                                 |                                                                             |
| 30  | HP_SYS_CLKRST_UART2_CLK_EN                 | Configures whether to enable the UART2_CLK clock. <br> 0: Disable <br> 1: Enable (R/W) |
| 27  | HP_SYS_CLKRST_UART1_SCLK_DIV_NUM           | Configures the integer part of the UART1_SCLK clock divisor. (R/W)          |
| 26  |                                             |                                                                             |
| 25  | HP_SYS_CLKRST_UART1_SCLK_DIV_NUMERATOR     | Configures the numerator of the divisor's fractional part for UART1_SCLK. (R/W) |
| 24  |                                             |                                                                             |
| 23  | HP_SYS_CLKRST_UART1_SCLK_DIV_DENOMINATOR   | Configures the denominator of the divisor's fractional part for UART1_SCLK. (R/W) |
| 22  |                                             |                                                                             |
| 16  | HP_SYS_CLKRST_UART2_CLK_SRC_SEL            | Configures the clock source for UART2_CLK. <br> 0: XTAL_CLK <br> 1: RC_FAST_CLK <br> 2: PLL_F80M_CLK <br> 3: Invalid (R/W) |
| 15  |                                             |                                                                             |
| 8   |                                             |                                                                             |
| 7   |                                             |                                                                             |
| 0   | Reset                                      |                                                                             |

HP_SYS_CLKRST_UART1_SCLK_DIV_NUM Configures the integer part of the UART1_SCLK clock divisor. (R/W)

HP_SYS_CLKRST_UART1_SCLK_DIV_NUMERATOR Configures the numerator of the divisor's fractional part for UART1_SCLK. (R/W)

HP_SYS_CLKRST_UART1_SCLK_DIV_DENOMINATOR Configures the denominator of the divisor's fractional part for UART1_SCLK. (R/W)

HP_SYS_CLKRST_UART2_CLK_SRC_SEL Configures the clock source for UART2_CLK.
0: XTAL_CLK
1: RC_FAST_CLK
2: PLL_F80M_CLK
3: Invalid
(R/W)

HP_SYS_CLKRST_UART2_CLK_EN Configures whether to enable the UART2_CLK clock.
0: Disable
1: Enable
(R/W)
```