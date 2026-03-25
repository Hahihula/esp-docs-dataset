

```markdown
Chapter 7 Reset and Clock

Register 7.2. PCR_UARTO_SCLK_CONF_REG (0x0004)

| 31 | 23 | 22 | 21 | 20 | 19 | 12 | 11 | 6 | 5 | 0 |
|----|----|----|----|----|----|----|----|---|---|---|
|    |    |    |    |    |    |    |    |   |   | Reset |

PCR_UARTO_SCLK_DIV_A Configures the denominator of the frequency divider factor of the UARTO functional clock. (R/W)

PCR_UARTO_SCLK_DIV_B Configures the numerator of the frequency divider factor of the UARTO functional clock. (R/W)

PCR_UARTO_SCLK_DIV_NUM Configures the integral part of the frequency divider factor of the UARTO functional clock. (R/W)

PCR_UARTO_SCLK_SEL Configures the clock source of UARTO.
0 (default): XTAL_CLK
1: RC_FAST_CLK
2: PLL_F80M_CLK
(R/W)

PCR_UARTO_SCLK_EN Configures whether or not to enable UARTO functional clock.
0: Not enable
1: Enable
(R/W)
```