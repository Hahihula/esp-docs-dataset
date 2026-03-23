

```markdown
Register 39.6. APB_SARADC_ONETIME_SAMPLE_REG (0x0020)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | APB_SARADC_ONETIME_SAMPLE (reserved)                                       |
| 30  | APB_SARADC_ONETIME_START                                                   |
| 29  | APB_SARADC_ONETIME_CHANNEL                                                 |
| 28  | APB_SARADC_ONETIME_ATTEN                                                   |
| 27-0| (reserved)                                                                 |

APB_SARADC_ONETIME_ATTEN Configures the attenuation for a one-time sampling. (R/W)
APB_SARADC_ONETIME_CHANNEL Configures the channel for a one-time sampling. (R/W)
APB_SARADC_ONETIME_START Configures whether to start SAR ADC one-time sampling.
  O: No effect
  1: Start
  (R/W)

APB_SARADC_ONETIME_SAMPLE Configures whether to enable SAR ADC one-time sampling.
  O: Disable
  1: Enable
  (R/W)
```

```markdown
Register 39.7. APB_SARADC_FILTER_CTRL0_REG (0x0028)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | APB_SARADC_FILTER_RESET (reserved)                                          |
| 30  | APB_SARADC_FILTER_CHANNEL1                                                 |
| 29  | APB_SARADC_FILTER_CHANNEL0                                                 |
| 28-17| (reserved)                                                                 |
| 16-14| (reserved)                                                                 |
| 13  | APB_SARADC_FILTER_RESET                                                    |

APB_SARADC_FILTER_CHANNEL1 Configures the filter channel for SAR ADC filter 1. (R/W)
APB_SARADC_FILTER_CHANNEL0 Configures the filter channel for SAR ADC filter 0. (R/W)

APB_SARADC_FILTER_RESET Configures whether to reset SAR ADC filter.
  O: No effect
  1: Reset
  (R/W)
```