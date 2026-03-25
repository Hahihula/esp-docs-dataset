

```markdown
Register 33.10. APB_SARADC_THRESH1_CTRL_REG (0x0038)

| Bit Range | Field Name                          | Description                                                                 |
|-----------|--------------------------------------|-----------------------------------------------------------------------------|
| 31:30     | (reserved)                          |                                                                             |
| 18        | APB_SARADC_THRESH1_LOW               | Configures the low threshold for SAR ADC monitor 1. (R/W)                   |
| 17        | APB_SARADC_THRESH1_HIGH              | Configures the high threshold for SAR ADC monitor 1. (R/W)                  |
| 5:4       | (reserved)                          |                                                                             |
| 3         | APB_SARADC_THRESH1_CHANNEL           | Configures the channel for SAR ADC monitor 1. (R/W)                         |
| 0         | Reset                               | 0x1fff                                                                       |

APB_SARADC_THRESH1_CHANNEL Configures the channel for SAR ADC monitor 1. (R/W)
APB_SARADC_THRESH1_HIGH Configures the high threshold for SAR ADC monitor 1. (R/W)
APB_SARADC_THRESH1_LOW Configures the low threshold for SAR ADC monitor 1. (R/W)

Register 33.11. APB_SARADC_THRESH_CTRL_REG (0x003C)

| Bit Range | Field Name                          | Description                                                                 |
|-----------|--------------------------------------|-----------------------------------------------------------------------------|
| 31        | O                                   |                                                                             |
| 30:29     | APB_SARADC_THRESH0_EN                | Configures whether to enable threshold monitor 0. (R/W)                     |
| 28:27     | APB_SARADC_THRESH1_EN                | Configures whether to enable threshold monitor 1. (R/W)                     |
| 26        | O                                   |                                                                             |

APB_SARADC_THRESH_ALL_EN Configures whether to enable the threshold monitoring for all configured channels.
O: Disable
1: Enable
(R/W)

APB_SARADC_THRESH1_EN Configures whether to enable threshold monitor 1.
O: Disable
1: Enable
(R/W)

APB_SARADC_THRESH0_EN Configures whether to enable threshold monitor 0.
O: Disable
1: Enable
(R/W)
```