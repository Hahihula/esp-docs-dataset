

```markdown
| 31 | 23 | 22 | 21 | 20 | 19 | 12 | 11 | 6 | 5 | 0 |
|-----:|:----|:----|:----|:----|:----|:----|:----|:--|:--|:---|
| 0   | 0   | 0   | 0  | 0  | 1  | 0   | 4  | 0 | 0 | Reset |
```

PCR_SARADC_CLKM_DIV_A Configures the denominator of the frequency divider factor of the SAR ADC functional clock. (R/W)

PCR_SARADC_CLKM_DIV_B Configures the numerator of the frequency divider factor of the SAR ADC functional clock. (R/W)

PCR_SARADC_CLKM_DIV_NUM Configures the integral part of the frequency divider factor of the SAR ADC functional clock. (R/W)

PCR_SARADC_CLKM_SEL Configures the clock source of SAR ADC.
- O (default): XTAL_CLK
- 1: RC_FAST_CLK
- 2: PLL_F80M_CLK
(R/W)

PCR_SARADC_CLKM_EN Configures whether or not to enable SAR ADC functional clock.
- 0: Not enable
- 1: Enable
(R/W)
```