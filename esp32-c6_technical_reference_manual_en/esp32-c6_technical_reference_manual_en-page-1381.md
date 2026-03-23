

```markdown
Register 39.20. APB_TSENS_WAKE_REG (0x0064)

APB_SARADC_WAKEUP_TH_LOW Configures the low threshold for temperature sensor wake-up function. (R/W)

APB_SARADC_WAKEUP_TH_HIGH Configures the high threshold for temperature sensor wake-up function. (R/W)

APB_SARADC_WAKEUP_OVER_UPPER_TH Represents whether the temperature value exceeds the threshold.
0: The temperature value is below the low threshold
1: The temperature value is above the high threshold
(RO)

APB_SARADC_WAKEUP_MODE Configures the wake-up mode for temperature sensor.
0: Absolute value mode
1: Incremental value mode
(R/W)

APB_SARADC_WAKEUP_EN Configures whether to enable wake-up.
0: Disable
1: Enable
(R/W)
```