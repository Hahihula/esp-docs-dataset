

```markdown
Register 34.19. APB_SARADC_APB_ADC_CLKM_CONF_REG (0x0054)

| 31 | 23 | 22 | 21 | 20 | 19           | 14   | 13     | 8      | 7        | 0            |
|----:|----:|----:|----:|----:|--------------|------:|--------:|-------:|---------:|---------------|
|    |    |    |    |    | APB_SARADC_CLK_SEL | Oxo   | OxO     |        |         | Reset         |
| 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 4 |

APB_SARADC_CLKM_DIV_NUM The integer part of ADC clock divider. Divider value = APB_SARADC_CLKM_DIV_NUM + APB_SARADC_CLKM_DIV_B/APB_SARADC_CLKM_DIV_A. (R/W)

APB_SARADC_CLKM_DIV_B The numerator value of fractional clock divider. (R/W)

APB_SARADC_CLKM_DIV_A The denominator value of fractional clock divider. (R/W)

APB_SARADC_CLK_EN Enable the SAR ADC register clock. (R/W)

APB_SARADC_CLK_SEL 0: Use APB_CLK as clock source, 1: use divided-down PLL_240 as clock source. (R/W)
```

```markdown
Register 34.20. APB_SARADC_APB_TSENS_CTRL_REG (0x0058)

| 31 | 23 | 22 | 21           | 14   | 13     | 12      | 8        | 7         | 0            |
|----:|----:|----:|-------------:|------:|--------:|---------:|---------:|----------:|---------------|
|    |    |    | APB_SARADC_TSENS_PU | Oxo   | OxO     |          | Reset    |           |               |
| 0 | 0 | 0 | 0 | 6 | 0 | 0 | 0 | 4 |

APB_SARADC_TSENS_OUT Temperature sensor data out. (RO)

APB_SARADC_TSENS_IN_INV Invert temperature sensor input value. (R/W)

APB_SARADC_TSENS_CLK_DIV Temperature sensor clock divider. (R/W)

APB_SARADC_TSENS_PU Temperature sensor power up. (R/W)
```