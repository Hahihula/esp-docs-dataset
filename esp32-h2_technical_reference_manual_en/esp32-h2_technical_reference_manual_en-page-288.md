

```markdown
Register 7.5. PCR_UART1_SCLK_CONF_REG (0x0010)

| 31 | 23 | 22 | 21 | 20 | 19 | reserved) | 12 | 11 | 6 | 5 | 0 |
|----:|----:|----:|----:|----:|----:|-----------:|----:|----:|---:|---:|---:|
|    |    |    |    |    |    |            |    |    |   |   |   |
| 0 | 0 | 0 | 0 | 0 | 0 | 1 | 3 | 0 | 0 | Reset |

PCR_UART1_SCLK_DIV_A Configures the denominator of the divisor's fractional part for UART1 functional clock. (R/W)

PCR_UART1_SCLK_DIV_B Configures the numerator of the divisor's fractional part for UART1 functional clock. (R/W)

PCR_UART1_SCLK_DIV_NUM Configures the integral part of the divisor for UART1 functional clock. (R/W)

PCR_UART1_SCLK_SEL Configures the clock source of UART1.
0: No clock source
1: PLL_F48M_CLK
2: RC_FAST_CLK
3 (default): XTAL_CLK
(R/W)

PCR_UART1_SCLK_EN Configures whether or not to enable UART1 functional clock.
0: Not enable
1: Enable
(R/W)
```