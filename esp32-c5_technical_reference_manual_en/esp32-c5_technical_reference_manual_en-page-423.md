

```markdown
|31|23|22|21|20|19|12|11|6|5|0|
|---|---|---|---|---|---|---|---|---|---|---|
|0| | | | | |4||||
|| ||||||||||
PCR_SARADC_CLKM_DIV_A Configures the denominator of the divisor's fractional part for SAR ADC functional clock. (R/W)
```

```markdown
PCR_SARADC_CLKM_DIV_B Configures the numerator of the divisor's fractional part for SAR ADC functional clock. (R/W)
```

```markdown
PCR_SARADC_CLKM_DIV_NUM Configures the integral part of the divisor for SAR ADC functional clock. (R/W)
```

```markdown
PCR_SARADC_CLKM_SEL Configures the clock source of SAR ADC.
O (default): XTAL_CLK
1: RC_FAST_CLK
2: PLL_F80M_CLK
3: No clock source
(R/W)
```

```markdown
PCR_SARADC_CLKM_EN Configures whether or not to enable SAR ADC functional clock.
O: Not enable
1: Enable
(R/W)
```
```