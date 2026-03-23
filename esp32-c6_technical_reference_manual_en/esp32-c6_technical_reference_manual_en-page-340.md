

```markdown
Chapter 8 Reset and Clock

Register 8.32. PCR_SARADC_CLKM_CONF_REG (0x0084)

| 31 | 23 | 22 | 21 | 20 | 19 | 12 | 11 | 6 | 5 | 0 |
|----|----|----|----|----|----|----|----|---|---|---|
|    |    |    |    |    | PCR_SARADC_CLKM_EN<br>PCR_SARADC_CLKM_SEL<br>PCR_SARADC_CLKM_DIV_NUM<br>PCR_SARADC_CLKM_DIV_B<br>PCR_SARADC_CLKM_DIV_A | Reset |

PCR_SARADC_CLKM_DIV_A Configures the denominator of the frequency divider factor for SAR ADC function clock. (R/W)

PCR_SARADC_CLKM_DIV_B Configures the numerator of the frequency divider factor for SAR ADC function clock. (R/W)

PCR_SARADC_CLKM_DIV_NUM Configures the integral part of the frequency divider factor for SAR ADC function clock. (R/W)

PCR_SARADC_CLKM_SEL Configures to select clock source.
0 (default): Select XTAL_CLK
1: Select PLL_F80M_CLK
2: Select RC_FAST_CLK
3: Reserved
(R/W)

PCR_SARADC_CLKM_EN Configures whether or not to enable SAR ADC function clock.
0: Not enable
1: Enable
(R/W)
```