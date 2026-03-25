

```markdown
Register 40.2. APB_SARADC_CTRL2_REG (0x0004)

| Bit Range | Field Name                     | Description                                                                 |
|-----------|---------------------------------|-----------------------------------------------------------------------------|
| 31        | (reserved)                     |                                                                             |
| 25..24    | APB_SARADC_TIMER_EN            | Configures whether to enable SAR ADC timer trigger.                         |
|           |                                 | O: Disable                                                                   |
|           |                                 | 1: Enable                                                                    |
|           |                                 | (R/W)                                                                        |
| 12        | APB_SARADC_TIMER_TARGET        | Configures SAR ADC timer target.                                            |
|           |                                 | (R/W)                                                                        |
| 11..8     | (reserved)                     |                                                                             |
| 7         | APB_SARADC_SAR1_INV            | Configures whether to invert the data of SAR ADC.                           |
|           |                                 | O: No effect                                                                 |
|           |                                 | 1: Invert the data of SAR ADC                                                |
|           |                                 | (R/W)                                                                        |
| 6         | APB_SARADC_MAX_MEAS_NUM_LIMIT  | Configures whether to enable the limitation of SAR ADC’s maximum conversion times. |
|           |                                 | O: Disable                                                                   |
|           |                                 | 1: Enable                                                                    |
|           |                                 | (R/W)                                                                        |
| 5         | APB_SARADC_MAX_MEAS_NUM        | Configures the SAR ADC’s maximum conversion times.                          |
|           |                                 | (R/W)                                                                        |
```