

```markdown
Register 32.3. APB_TSENS_WAKE_REG (0x0064)

APB_SARADC_WAKEUP_TH_LOW Configures the low threshold for automatic temperature monitoring. (R/W)

APB_SARADC_WAKEUP_TH_HIGH Configures the high threshold for automatic temperature monitoring. (R/W)

APB_SARADC_WAKEUP_OVER_UPPER_TH Represents whether the temperature output value exceeds the threshold. Valid only when APB_SARADC_WAKEUP_EN=1.
0: The temperature output value is below the low threshold
1: The temperature output value is above the high threshold
(RO)

APB_SARADC_WAKEUP_MODE Selects the temperature monitoring mode.
0: Absolute value mode
1: Change value mode
(R/W)

APB_SARADC_WAKEUP_EN Configures whether to enable the temperature monitoring function.
0: Disable
1: Enable
(R/W)
```