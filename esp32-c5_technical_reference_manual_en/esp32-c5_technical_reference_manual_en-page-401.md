

```markdown
Chapter 9 Reset and Clock

GoBack

Register 9.2. PCR_UARTO_SCLK_CONF_REG (0x0004)

| 31 | 23 | 22 | 21 | 20 | 19 | reserved) | PCR_UARTO_SCLK_EN | PCR_UARTO_SCLK_SEL | PCR_UARTO_SCLK_DIV_NUM | PCR_UARTO_SCLK_DIV_B | PCR_UARTO_SCLK_DIV_A |
|----:|----:|----:|----:|----:|----:|------------:|-------------------:|--------------------:|------------------------:|----------------------:|----------------------:|
| 0 | 0 | 0 | 0 | 0 | 0 | 1 | 3 | 0 | 0 | 0 | Reset |

PCR_UARTO_SCLK_DIV_A Configures the denominator of the divisor's fractional part's fractional part for UARTO functional clock. (R/W)

PCR_UARTO_SCLK_DIV_B Configures the numerator of the divisor's fractional part for UARTO functional clock. (R/W)

PCR_UARTO_SCLK_DIV_NUM Configures the integral part of the divisor for UARTO functional clock. (R/W)

PCR_UARTO_SCLK_SEL Configures the clock source of UARTO.
0: No clock source
1: PLL_F8OM_CLK
2: RC_FAST_CLK
3 (default): XTAL_CLK
(R/W)

PCR_UARTO_SCLK_EN Configures whether or not to enable UARTO functional clock.
0: Not enable
1: Enable
(R/W)
```