

```markdown
Register 62.37. LPADC_WAKEUP1_REG (0x0060)

| Bit | Field Name                                 | Description                                                                 |
|-----|---------------------------------------------|-----------------------------------------------------------------------------|
| 31  |                                             |                                                                             |
| 30  | LPADC_SAR1_WAKEUP_MODE                     | Selects the wake-up mode for automatic monitoring. Valid only when LPADC_SAR1_WAKEUP_EN=1.<br>0: Absolute value mode<br>1: Change value mode (R/W) |
| 29  | LPADC_SAR1_WAKEUP_EN                       | Configures whether to enable wake-up function for LP ADC1.<br>0: Disable<br>1: Enable (R/W) |
| 28  | LPADC_SAR1_WAKEUP_OVER_UPPER_TH            | Indicates whether the wake-up event is triggered by the conversion data exceeding high threshold. (RO) |
| 27  |                                             |                                                                             |
| 26  | LPADC_SAR1_WAKEUP_TH_HIGH                  | Configures the high threshold for LP ADC1's wake-up function. (R/W)          |
| 25  |                                             |                                                                             |
| 24  |                                             |                                                                             |
| 23  |                                             |                                                                             |
| 22  |                                             |                                                                             |
| 21  |                                             |                                                                             |
| 20  |                                             |                                                                             |
| 19  |                                             |                                                                             |
| 18  |                                             |                                                                             |
| 17  |                                             |                                                                             |
| 16  |                                             |                                                                             |
| 15  |                                             |                                                                             |
| 14  | LPADC_SAR1_WAKEUP_TH_LOW                   | Configures the low threshold for LP ADC1's wake-up function. (R/W)           |
| 13  |                                             |                                                                             |
| 12  |                                             |                                                                             |
| 11  |                                             |                                                                             |
| 10  |                                             |                                                                             |
| 9   |                                             |                                                                             |
| 8   |                                             |                                                                             |
| 7   |                                             |                                                                             |
| 6   |                                             |                                                                             |
| 5   |                                             |                                                                             |
| 4   |                                             |                                                                             |
| 3   |                                             |                                                                             |
| 2   |                                             |                                                                             |
| 1   |                                             |                                                                             |
| 0   |                                             | Reset                                                                         |

LPADC_SAR1_WAKEUP_TH_LOW Configures the low threshold for LP ADC1's wake-up function. (R/W)

LPADC_SAR1_WAKEUP_TH_HIGH Configures the high threshold for LP ADC1's wake-up function. (R/W)

LPADC_SAR1_WAKEUP_OVER_UPPER_TH Indicates whether the wake-up event is triggered by the conversion data exceeding high threshold. (RO)

LPADC_SAR1_WAKEUP_EN Configures whether to enable wake-up function for LP ADC1.<br>0: Disable<br>1: Enable (R/W)

LPADC_SAR1_WAKEUP_MODE Selects the wake-up mode for automatic monitoring. Valid only when LPADC_SAR1_WAKEUP_EN=1.<br>0: Absolute value mode<br>1: Change value mode (R/W)
```