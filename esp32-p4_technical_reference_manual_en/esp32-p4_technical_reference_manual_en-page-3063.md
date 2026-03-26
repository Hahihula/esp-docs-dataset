

```markdown
## Register 62.38. LPADC_WAKEUP2_REG (0x0064)

| Bit | Field Name                             | Description                                                                 |
|-----|-----------------------------------------|-----------------------------------------------------------------------------|
| 31  |                                         |                                                                             |
| 30  | LPADC_SAR2_WAKEUP_MODE                 | Selects the wake-up mode for automatic monitoring. Valid only when LPADC_SAR2_WAKEUP_EN=1.<br>0: Absolute value mode<br>1: Change value mode (R/W) |
| 29  | LPADC_SAR2_WAKEUP_EN                   | Configures whether to enable wake-up function for LP ADC2.<br>0: Disable<br>1: Enable (R/W) |
| 28  | LPADC_SAR2_WAKEUP_OVER_UPPER_TH        | Indicates whether the wake-up event is triggered by the conversion data exceeding high threshold. (RO) |
| 27  |                                         |                                                                             |
| 26  | LPADC_SAR2_WAKEUP_TH_HIGH              | Configures the high threshold for LP ADC2's wake-up function. (R/W)          |
| 25  | LPADC_SAR2_WAKEUP_TH_LOW               | Configures the low threshold for LP ADC2's wake-up function. (R/W)           |
| 14  |                                         |                                                                             |
| 13  |                                         |                                                                             |
| 12  |                                         |                                                                             |
| 11  |                                         |                                                                             |
| 0   | Reset                                  | 0x0004                                                                       |

LPADC_SAR2_WAKEUP_TH_LOW Configures the low threshold for LP ADC2's wake-up function. (R/W)

LPADC_SAR2_WAKEUP_TH_HIGH Configures the high threshold for LP ADC2's wake-up function. (R/W)

LPADC_SAR2_WAKEUP_OVER_UPPER_TH Indicates whether the wake-up event is triggered by the conversion data exceeding high threshold. (RO)

LPADC_SAR2_WAKEUP_EN Configures whether to enable wake-up function for LP ADC2.<br>0: Disable<br>1: Enable (R/W)

LPADC_SAR2_WAKEUP_MODE Selects the wake-up mode for automatic monitoring. Valid only when LPADC_SAR2_WAKEUP_EN=1.<br>0: Absolute value mode<br>1: Change value mode (R/W)
```

```markdown
## Register 62.39. LPADC_WAKEUP_SEL_REG (0x0068)

| Bit | Field Name                             | Description                                                                 |
|-----|-----------------------------------------|-----------------------------------------------------------------------------|
| 31  |                                         |                                                                             |
| 30  |                                         |                                                                             |
| 29  |                                         |                                                                             |
| 28  |                                         |                                                                             |
| 27  |                                         |                                                                             |
| 26  |                                         |                                                                             |
| 25  |                                         |                                                                             |
| 24  |                                         |                                                                             |
| 23  |                                         |                                                                             |
| 22  |                                         |                                                                             |
| 21  |                                         |                                                                             |
| 20  |                                         |                                                                             |
| 19  |                                         |                                                                             |
| 18  |                                         |                                                                             |
| 17  |                                         |                                                                             |
| 16  |                                         |                                                                             |
| 15  |                                         |                                                                             |
| 14  |                                         |                                                                             |
| 13  |                                         |                                                                             |
| 12  |                                         |                                                                             |
| 11  |                                         |                                                                             |
| 10  |                                         |                                                                             |
| 9   |                                         |                                                                             |
| 8   |                                         |                                                                             |
| 7   |                                         |                                                                             |
| 6   |                                         |                                                                             |
| 5   |                                         |                                                                             |
| 4   |                                         |                                                                             |
| 3   |                                         |                                                                             |
| 2   |                                         |                                                                             |
| 1   | LPADC_SAR_WAKEUP_SEL                  | Enables the wake-up function for LP ADC1 or LP ADC2.<br>0: LP ADC1<br>1: LP ADC2. (R/W) |
| 0   | Reset                                  | 0x0068                                                                       |
```