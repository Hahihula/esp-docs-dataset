

```markdown
## Register 39.2. APB_SARADC_CTRL2_REG (0x0004)

| Bit Range | Field Name                     | Description                                                                 |
|-----------|---------------------------------|-----------------------------------------------------------------------------|
| 31        | (reserved)                     |                                                                             |
| 25–24     | APB_SARADC_TIMER_EN            | Configures whether to enable SAR ADC timer trigger. (R/W)<br>0: Disable<br>1: Enable |
| 12–11     | APB_SARADC_TIMER_TARGET        | Configures SAR ADC timer target. (R/W)                                     |
| 10        | (reserved)                     |                                                                             |
| 9         | APB_SARADC_SAR1_INV            | Configures whether to invert the data of SAR ADC.<br>0: No effect<br>1: Invert the data of SAR ADC (R/W) |
| 8         | APB_SARADC_MAX_MEAS_NUM        | Configures the SAR ADC’s maximum conversion times. (R/W)                     |
| 7–0       | APB_SARADC_MEAS_NUM_LIMIT      | Configures whether to enable the limitation of SAR ADC’s maximum conversion times.<br>0: Disable<br>1: Enable (R/W) |

## Register 39.3. APB_SARADC_FILTER_CTRL1_REG (0x0008)

| Bit Range | Field Name                     | Description                                                                 |
|-----------|---------------------------------|-----------------------------------------------------------------------------|
| 31        | (reserved)                     |                                                                             |
| 29–26     | APB_SARADC_FILTER_FACTOR1      | Configures the filter coefficient for SAR ADC filter 1. (R/W)                |
| 25–0      | APB_SARADC_FILTER_FACTOR0      | Configures the filter coefficient for SAR ADC filter 0. (R/W)                |
```