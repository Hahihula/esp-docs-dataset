

```markdown
## Register 10.77: LPPERI_ADC_CTRL_REG (0x002C)

| Bit Range | Field Name                                 | Description                                                                 |
|-----------|---------------------------------------------|-----------------------------------------------------------------------------|
| 31        |                                             |                                                                             |
| 24-23     | LPPERI_LPADC_SAR1_DIV_NUM                  | Configures the LP ADC SAR1 clock divisor. (R/W)                              |
| 16-15     | LPPERI_LPADC_SAR2_DIV_NUM                  | Configures the LP ADC SAR2 clock divisor. (R/W)                              |
| 8-7       | LPPERI_LPADC_FUNC_DIV_NUM                  | Configures the LP ADC function clock divisor. (R/W)                          |
| 6-5       |                                             |                                                                             |
| 0         | Reset                                      |                                                                             |

### Bit Field Descriptions

**LPPERI_SAR2_CLK_FORCE_ON**: Configures whether to force on the LP ADC SAR1 clock.
- 0: Controlled by hardware
- 1: Force on, bypassing hardware control (R/W)

**LPPERI_SAR1_CLK_FORCE_ON**: Configures whether to force on the LP ADC SAR2 clock.
- 0: Controlled by hardware
- 1: Force on, bypassing hardware control (R/W)

**LPPERI_LPADC_FUNC_DIV_NUM**: Configures the LP ADC function clock divisor. (R/W)

**LPPERI_LPADC_SAR2_DIV_NUM**: Configures the LP ADC SAR1 clock divisor.(R/W)

**LPPERI_LPADC_SAR1_DIV_NUM**: Configures the LP ADC SAR2 clock divisor.(R/W)
```

```markdown
## Register 10.78: LPPERI_LP_I2S_RXCLK_DIV_NUM_REG (0x0030)

| Bit Range | Field Name                                 | Description                                                                 |
|-----------|---------------------------------------------|-----------------------------------------------------------------------------|
| 31        |                                             |                                                                             |
| 24-23     |                                             |                                                                             |
| 0         | Reset                                      |                                                                             |

### Bit Field Descriptions

**LPPERI_LP_I2S_RX_CLKM_DIV_NUM**: Configures the integer part of the LP I2S RX clock divisor. (R/W)
```