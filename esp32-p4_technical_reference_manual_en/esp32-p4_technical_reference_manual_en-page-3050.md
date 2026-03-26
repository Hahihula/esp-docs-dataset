

```markdown
Register 62.23. LPADC_MEAS1_CTRL2_REG (0x000C)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | LPADC_SAR1_EN_PAD_FORCE                                                   |
| 30  | LPADC_SAR1_EN_PAD                                                          |
| 19  | LPADC_MEAS1_START_FORCE                                                    |
| 18  | LPADC_MEAS1_DONE_SAR                                                       |
| 17  | LPADC_MEAS1_DATA_SAR                                                       |
| 16  | Reset                                                                     |
|     | 0x0                                                                        |
|     | 0x00                                                                      |

LPADC_MEAS1_DATA_SAR Stores LP ADC1's conversion data in one-shot sampling mode. (RO)

LPADC_MEAS1_DONE_SAR Indicates whether LP ADC1 conversion is done. (RO)

LPADC_MEAS1_START_SAR Configures whether to start LP ADC1 by software.
  O: No effect
  1: Start LP ADC1 by software
Valid only when LPADC_MEAS1_START_FORCE = 1. (R/W)

LPADC_MEAS1_START_FORCE Configures whether to use software to enable LP ADC1 sampling.
  O: Select FSM to start LP ADC1 sampling
  1: Select software to start LP ADC1 sampling
(R/W)

LPADC_SAR1_EN_PAD Configures the sampling channel for LP ADC1. Value 0 ~ 7 corresponds to channel 0 ~ 7. (R/W)

LPADC_SAR1_EN_PAD_FORCE Configures whether to use software to select the sampling channel for LP ADC1.
  O: No effect
  1: Use software to control
(R/W)
```