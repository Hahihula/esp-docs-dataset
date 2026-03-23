

```markdown
| 31 | 23 | 22 | 21 | 20 | 19 | 12 | 11 | 6 | 5 | 0 |
|-----:|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|
| 0   | 0   | 0   | 0  | 0  | 1  | 3  | 0  | 0  | 0  | Reset |
```

PCR_UARTO_SCLK_DIV_A Configures the denominator of the frequency divider factor for UARTO function clock. (R/W)

PCR_UARTO_SCLK_DIV_B Configures the numerator of the frequency divider factor for UARTO function clock. (R/W)

PCR_UARTO_SCLK_DIV_NUM Configures the integral part of the frequency divider factor for UARTO function clock. (R/W)

PCR_UARTO_SCLK_SEL Configures to select clock source.
0: Not select any clock
1: Select PLL_F80M_CLK
2: Select RC_FAST_CLK
3: Select XTAL_CLK
(R/W)

PCR_UARTO_SCLK_EN Configures whether or not to enable UARTO function clock.
0: Not enable
1: Enable
(R/W)
```