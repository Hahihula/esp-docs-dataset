

```markdown
Register 62.22. LPADC_READER1_CTRL_REG (0x0000)

| Bit | Name                                 | Description                                                                 |
|-----|---------------------------------------|-----------------------------------------------------------------------------|
| 31  | O                                    | Reserved                                                                    |
| 30  | LPADC_SAR1_EN_PAD_FORCE_ENABLE       | Configures whether to use software to force enable LPADC_SAR1_EN_PAD.      |
|     |                                       | - 2: Force off                                                              |
|     |                                       | - 3: Force enable                                                           |
|     | Other values: Hardware control (enabled during sampling)                     |                                                                             |
| 29  | LPADC_SAR1_INT_EN                    | Enables LP ADC1 to send out interrupt. (R/W)                                |
| 28  | LPADC_SAR1_DATA_INV                  | Configures whether to invert the data of LP ADC1.                           |
|     |                                       | - 0: Do not invert the data.                                                |
|     |                                       | - 1: Invert the data.                                                        |
| 27  | LPADC_SAR1_CLK_DIV                  | Configures the division of LP ADC1's clock LPADC_SARCLK. (R/W)              |
```