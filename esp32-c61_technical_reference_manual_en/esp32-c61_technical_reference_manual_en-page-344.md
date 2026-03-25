

```markdown
Chapter 7 Reset and Clock

Register 7.8. PCR_UART2_SCLK_CONF_REG (0x001C)

| 31 | 23 | 22 | 21 | 20 | 19 | 12 | 11 | 6 | 5 | 0 |
|----|----|----|----|----|----|----|----|---|---|---|
|    |    |    |    |    |    |    |    |   |   | Reset |

PCR_UART2_SCLK_DIV_A Configures the denominator of the frequency divider factor of the UART2 functional clock. (R/W)

PCR_UART2_SCLK_DIV_B Configures the numerator of the frequency divider factor of the UART2 functional clock. (R/W)

PCR_UART2_SCLK_DIV_NUM Configures the integral part of the frequency divider factor of the UART2 functional clock. (R/W)

PCR_UART2_SCLK_SEL Configures the clock source of UART2.
0 (default): XTAL_CLK
1: RC_FAST_CLK
2: PLL_F80M_CLK
(R/W)

PCR_UART2_SCLK_EN Configures whether or not to enable UART2 functional clock.
0: Not enable
1: Enable
(R/W)
```