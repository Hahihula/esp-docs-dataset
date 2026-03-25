

```markdown
Register 46.2. APB_SARADC_CTRL2_REG (0x0004)

| Bit Range | Field Name                     | Description                                                                 |
|-----------|---------------------------------|-----------------------------------------------------------------------------|
| 31        | (reserved)                     |                                                                             |
| 25        | APB_SARADC_TIMER_EN            | Configures whether to enable SAR ADC timer trigger.                         |
|           |                                 | O: Disable                                                                   |
|           |                                 | 1: Enable                                                                    |
|           |                                 | (R/W)                                                                        |
| 24..10    | APB_SARADC_TIMER_TARGET        | Configures SAR ADC timer target.                                            |
|           |                                 | (R/W)                                                                        |
| 9         | (reserved)                     |                                                                             |
| 8         | APB_SARADC_SAR1_INV            | Configures whether to invert the data of SAR ADC.                           |
|           |                                 | O: No effect                                                                 |
|           |                                 | 1: Invert the data of SAR ADC                                                |
|           |                                 | (R/W)                                                                        |
| 7         | APB_SARADC_MAX_MEAS_NUM_LIMIT  | Configures whether to enable the limitation of SAR ADC's maximum conversion times. |
|           |                                 | O: Disable                                                                   |
|           |                                 | 1: Enable                                                                    |
|           |                                 | (R/W)                                                                        |
| 6         | APB_SARADC_MAX_MEAS_NUM        | Configures the SAR ADC's maximum conversion times.                          |
|           |                                 | (R/W)                                                                        |
| 5..0      | APB_SARADC_MEAS_NUM_LIMIT      |                                                                             |
|           |                                 | Reset                                                                       |

```
```markdown
APB_SARADC_MEAS_NUM_LIMIT Configures whether to enable the limitation of SAR ADC's maximum conversion times.
O: Disable
1: Enable
(R/W)

APB_SARADC_MAX_MEAS_NUM Configures the SAR ADC's maximum conversion times. (R/W)

APB_SARADC_SAR1_INV Configures whether to invert the data of SAR ADC.
O: No effect
1: Invert the data of SAR ADC
(R/W)

APB_SARADC_TIMER_TARGET Configures SAR ADC timer target. (R/W)

APB_SARADC_TIMER_EN Configures whether to enable SAR ADC timer trigger.
O: Disable
1: Enable
(R/W)
```