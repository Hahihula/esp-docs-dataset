

```markdown
## Register 34.12. APB_SARADC_THRES1_CTRL_REG (0x0038)

| Bit Range | Field Name                     | Description                                                                 |
|-----------|---------------------------------|-----------------------------------------------------------------------------|
| 31:30     | (reserved)                     |                                                                             |
| 18        | APB_SARADC_THRES1_LOW          | The low threshold for SAR ADC monitor 1. (R/W)                               |
| 17        | APB_SARADC_THRES1_HIGH         | The high threshold for SAR ADC monitor 1. (R/W)                              |
| 5:4       | (reserved)                     |                                                                             |
| 3:0       | APB_SARADC_THRES1_CHANNEL      | The channel for SAR ADC monitor 1. (R/W)                                     |

Reset value: `0x1fff`

APB_SARADC_THRES1_CHANNEL  The channel for SAR ADC monitor 1. (R/W)
APB_SARADC_THRES1_HIGH     The high threshold for SAR ADC monitor 1. (R/W)
APB_SARADC_THRES1_LOW      The low threshold for SAR ADC monitor 1. (R/W)

## Register 34.13. APB_SARADC_THRES_CTRL_REG (0x003C)

| Bit Range | Field Name                     | Description                                                                 |
|-----------|---------------------------------|-----------------------------------------------------------------------------|
| 31:27     | (reserved)                     |                                                                             |
| 26        | APB_SARADC_THRES0_EN           | Enable threshold monitor 0. (R/W)                                           |
| 25        | APB_SARADC_THRES1_EN           | Enable threshold monitor 1. (R/W)                                           |
| 24:0      | APB_SARADC_THRES_ALL_EN        | Enable the threshold monitoring for all configured channels. (R/W)            |

Reset value: `0`

APB_SARADC_THRES_ALL_EN    Enable the threshold monitoring for all configured channels. (R/W)
APB_SARADC_THRES1_EN       Enable threshold monitor 1. (R/W)
APB_SARADC_THRES0_EN       Enable threshold monitor 0. (R/W)
```