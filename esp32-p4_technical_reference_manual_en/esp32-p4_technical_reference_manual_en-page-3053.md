

```markdown
Register 62.27. LPADC_MEAS2_CTRL2_REG (0x0030)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | LPADC_SAR2_EN_PAD_FORCE                                                   |
| 30  | LPADC_SAR2_EN_PAD                                                          |
| 19  | LPADC_MEAS2_DATA_SAR                                                       |
| 18  | LPADC_MEAS2_DONE_SAR                                                       |
| 17  | LPADC_MEAS2_START_SAR                                                      |
| 16  | LPADC_MEAS2_START_FORCE                                                   |
| 15  | 0                                                                           |
|     | Reset                                                                      |

LPADC_MEAS2_DATA_SAR Stores LP ADC2's conversion data in one-shot sampling mode. (RO)

LPADC_MEAS2_DONE_SAR Indicates whether LP ADC2 conversion is done. (RO)

LPADC_MEAS2_START_SAR Configures whether to start LP ADC2 by software.
  - 0: No effect
  - 1: Start LP ADC2 by software
    Valid only when LPADC_MEAS2_START_FORCE = 1. (R/W)

LPADC_MEAS2_START_FORCE Configures whether to use software to enable LP ADC2 sampling.
  - 0: Select FSM to start LP ADC2 sampling
  - 1: Select software to start LP ADC2 sampling (R/W)

LPADC_SAR2_EN_PAD Configures the sampling channel for LP ADC2. Value 2 ~ 7 corresponds to channel 0 ~ 5. (R/W)

LPADC_SAR2_EN_PAD_FORCE Configures whether to use software to select the sampling channel for LP ADC1.
  - 0: No effect
  - 1: Use software to control (R/W)
```