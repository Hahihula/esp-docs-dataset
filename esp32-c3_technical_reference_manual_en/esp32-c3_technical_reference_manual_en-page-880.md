

```markdown
## Register 34.2. APB_SARADC_CTRL2_REG (0x0004)

| Bit | Field Name                     | Description                                                                 |
|-----|---------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                     |                                                                             |
| 30  | APB_SARADC_TIMER_EN            | Enable SAR ADC timer trigger. (R/W)                                        |
| 29  | APB_SARADC_TIMER_TARGET        | Set SAR ADC timer target. (R/W)                                            |
| 28  | (reserved)                     |                                                                             |
| 27  | APB_SARADC_SAR2_INV            | Write 1 here to invert the data of SAR ADC2. (R/W)                         |
| 26  | APB_SARADC_SAR1_INV            | Write 1 here to invert the data of SAR ADC1. (R/W)                         |
| 25  | APB_SARADC_MEAS_NUM_LIMIT      | Enable the limitation of SAR ADCs maximum conversion times. (R/W)           |
| 24  | APB_SARADC_MAX_MEAS_NUM        | The SAR ADCs maximum conversion times. (R/W)                                |
| 15-8| (reserved)                     |                                                                             |
| 7   | APB_SARADC_SAR2_INV            | Write 1 here to invert the data of SAR ADC2. (R/W)                         |
| 6   | APB_SARADC_SAR1_INV            | Write 1 here to invert the data of SAR ADC1. (R/W)                         |
| 5   | APB_SARADC_TIMER_TARGET        | Set SAR ADC timer target. (R/W)                                            |
| 4   | (reserved)                     |                                                                             |
| 3   | APB_SARADC_MEAS_NUM_LIMIT      | Enable the limitation of SAR ADCs maximum conversion times. (R/W)           |
| 2   | APB_SARADC_MAX_MEAS_NUM        | The SAR ADCs maximum conversion times. (R/W)                                |
| 1   | Reset                          |                                                                             |
| 0   | Reset                          |                                                                             |

APB_SARADC_MEAS_NUM_LIMIT Enable the limitation of SAR ADCs maximum conversion times. (R/W)
APB_SARADC_MAX_MEAS_NUM The SAR ADCs maximum conversion times. (R/W)
APB_SARADC_SAR1_INV Write 1 here to invert the data of SAR ADC1. (R/W)
APB_SARADC_SAR2_INV Write 1 here to invert the data of SAR ADC2. (R/W)
APB_SARADC_TIMER_TARGET Set SAR ADC timer target. (R/W)
APB_SARADC_TIMER_EN Enable SAR ADC timer trigger. (R/W)

## Register 34.3. APB_SARADC_FILTER_CTRL1_REG (0x0008)

| Bit | Field Name                     | Description                                                                 |
|-----|---------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                     |                                                                             |
| 30  | APB_SARADC_FILTER_FACTORO      | The filter coefficient for SAR ADC filter O. (R/W)                          |
| 29  | APB_SARADC_FILTER_FACTOR1      | The filter coefficient for SAR ADC filter 1. (R/W)                          |
| 28  | (reserved)                     |                                                                             |
| 27-0| Reset                          |                                                                             |

APB_SARADC_FILTER_FACTOR1 The filter coefficient for SAR ADC filter 1. (R/W)
APB_SARADC_FILTER_FACTORO The filter coefficient for SAR ADC filter O. (R/W)
```