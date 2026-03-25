

```markdown
Register 7.5. PCR_UART1_SCLK_CONF_REG (0x0010)

| 31 | 23 | 22 | 21 | 20 | 19 | reserved) | 12 | 11 | 6 | 5 | 0 |
|----|----|----|----|----|----|------------|----|----|---|---|---|
|    |    |    |    |    |    | PCR_UART1_SCLK_EN<br>PCR_UART1_SCLK_SEL<br>PCR_UART1_SCLK_DIV_NUM<br>PCR_UART1_SCLK_DIV_B<br>PCR_UART1_SCLK_DIV_A | O | O | 0 | Reset |

PCR_UART1_SCLK_DIV_A Configures the denominator of the frequency divider factor of the UART1 functional clock. (R/W)

PCR_UART1_SCLK_DIV_B Configures the numerator of the frequency divider factor of the UART1 functional clock. (R/W)

PCR_UART1_SCLK_DIV_NUM Configures the integral part of the frequency divider factor of the UART1 functional clock. (R/W)

PCR_UART1_SCLK_SEL Configures the clock source of UART1.
O (default): XTAL_CLK
1: RC_FAST_CLK
2: PLL_F80M_CLK
(R/W)

PCR_UART1_SCLK_EN Configures whether or not to enable UART1 functional clock.
O: Not enable
1: Enable
(R/W)
```