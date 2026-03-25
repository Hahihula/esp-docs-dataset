

```markdown
Register 39.3. APB_TSENS_WAKE_REG (0x0064)
```

| Bit | Field Name                     | Description                                                                 |
|-----|---------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                     |                                                                             |
| 19  | APB_SARADC_WAKEUP_EN           | Configures whether to enable temperature monitoring wake-up function.       |
| 18  | APB_SARADC_WAKEUP_MODE         | Selects the wake-up mode for temperature monitoring.<br>0: Absolute value mode<br>1: Change value mode (R/W) |
| 17  | APB_SARADC_WAKEUP_OVER_UPPER_TH| Represents whether the temperature output value exceeds the threshold.<br>0: The temperature output value is below the low threshold<br>1: The temperature output value is above the high threshold (RO) |
| 16  | APB_SARADC_WAKEUP_TH_HIGH      | Configures the high threshold for temperature monitoring wake-up function. (R/W) |
| 15  | APB_SARADC_WAKEUP_TH_LOW       | Configures the low threshold for temperature monitoring wake-up function. (R/W) |

```markdown
APB_SARADC_WAKEUP_TH_LOW Configures the low threshold for temperature monitoring wake-up function. (R/W)

APB_SARADC_WAKEUP_TH_HIGH Configures the high threshold for temperature monitoring wake-up function. (R/W)

APB_SARADC_WAKEUP_OVER_UPPER_TH Represents whether the temperature output value exceeds the threshold.<br>0: The temperature output value is below the low threshold<br>1: The temperature output value is above the high threshold (RO)

APB_SARADC_WAKEUP_MODE Selects the wake-up mode for temperature monitoring.<br>0: Absolute value mode<br>1: Change value mode (R/W)

APB_SARADC_WAKEUP_EN Configures whether to enable temperature monitoring wake-up function.<br>0: Disable<br>1: Enable (R/W)
```

```markdown
Espressif Systems

Submit Documentation Feedback

ESP32-H2 TRM (Version 1.1) 1232
```