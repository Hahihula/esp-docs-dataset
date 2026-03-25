

```markdown
| 31 | 23 | 22 | 21 | 20 | 19 | 12 | 11 | 6 | 5 | 0 |
|----:|----:|----:|----:|----:|----:|----:|----:|---:|---:|---:|
|    |    |    |    |    |     |    |    |   |   | Reset |
```

PCR_SARADC_CLKM_DIV_A Configures the denominator of the divisor's fractional part for SAR ADC functional clock. (R/W)

PCR_SARADC_CLKM_DIV_B Configures the numerator of the divisor's fractional part for SAR ADC functional clock. (R/W)

PCR_SARADC_CLKM_DIV_NUM Configures the integral part of the divisor for SAR ADC functional clock. (R/W)

PCR_SARADC_CLKM_SEL Configures the clock source of SAR ADC.
- O (default): XTAL_CLK
- 1: PLL_F96M_CLK
- 2: RC_FAST_CLK
- 3: No clock source
(R/W)

PCR_SARADC_CLKM_EN Configures whether or not to enable SAR ADC functional clock.
- O: Not enable
- 1: Enable
(R/W)
```