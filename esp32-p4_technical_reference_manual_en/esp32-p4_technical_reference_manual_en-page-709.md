

```markdown
Register 10.40. HP_SYS_CLKRST_PERI_CLK_CTRL22_REG (0x009C)

Continued from the previous page...

HP_SYS_CLKRST_ADC_CLK_SRC_SEL Configures the clock source for HPADC_CLK.
0: XTAL_CLK
1: RC_FAST_CLK
2: PLL_F8OM_CLK
3: Invalid
(R/W)
```

```markdown
Register 10.41. HP_SYS_CLKRST_PERI_CLK_CTRL23_REG (0x00A0)

HP_SYS_CLKRST_ADC_CLK_EN Configures whether to enable HPADC_CLK.
0: Disable
1: Enable
(R/W)

HP_SYS_CLKRST_ADC_CLK_DIV_NUM Configures the integer part of the HPADC_CLK clock divisor.
(R/W)

HP_SYS_CLKRST_ADC_CLK_DIV_NUMERATOR Configures the numerator of the divisor's fractional part for HPADC_CLK. (R/W)

HP_SYS_CLKRST_ADC_CLK_DIV_DENOMINATOR Configures the denominator of the divisor's fractional part for HPADC_CLK. (R/W)
```