

```markdown
Register 62.26. LPADC_READER2_CTRL_REG (0x0024)

| Bit | Field Name                     | Description                                                                 |
|-----|---------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                     |                                                                             |
| 30  | LPADC_SAR2_INT_EN              | Enables LP ADC2 to send out interrupt. (R/W)                                |
| 29  | LPADC_SAR2_DATA_INV            | Configures whether to invert the data of LP ADC2.<br>0: Do not invert the data.<br>1: Invert the data.<br>(R/W) |
| 28  | LPADC_SAR2_EN_PAD_FORCE_ENABLE| Configures whether to use software to force enable LPADC_SAR2_EN_PAD.<br>2: Force off<br>3: Force enable<br>Other values: Hardware control (enabled during sampling)<br>(R/W) |
| 27  | (reserved)                     |                                                                             |
| 26  | LPADC_SAR2_CLK_DIV             | Configures the division of LP ADC2’s clock LPADC_SARCLK. (R/W)              |
| 31-0|                                 |                                                                             |

LPADC_SAR2_CLK_DIV    Configures the division of LP ADC2’s clock LPADC_SARCLK. (R/W)

LPADC_SAR2_EN_PAD_FORCE_ENABLE   Configures whether to use software to force enable LPADC_SAR2_EN_PAD
  2: Force off
  3: Force enable
  Other values: Hardware control (enabled during sampling)
  (R/W)

LPADC_SAR2_DATA_INV    Configures whether to invert the data of LP ADC2.
  0: Do not invert the data.
  1: Invert the data.
  (R/W)

LPADC_SAR2_INT_EN      Enable LP ADC2 to send out interrupt. (R/W)
```