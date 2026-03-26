

```markdown
## Register 62.14: ADC_THRESH1_CTRL_REG (0x0048)

| Bit | Field         | Description                                                                 |
|-----|---------------|-----------------------------------------------------------------------------|
| 31  | (reserved)    |                                                                             |
| 30  |               |                                                                             |
| 18  |               |                                                                             |
| 17  | ADC_THRESH1_LOW |                                                                             |
|     |               |                                                                             |
| 5   |               |                                                                             |
| 4   |               |                                                                             |
| 0   | Reset         |                                                                             |

**ADC_THRESH1_CHANNEL** Configures the ADC channel for threshold monitor 1. Value 0 ~ 7 corresponds to channel 0 ~ 7 in HP ADC1, value 10 ~ 15 corresponds to channel 0 ~ 5 in HP ADC2. (R/W)

**ADC_THRESH1_HIGH** Configures the high threshold for HP ADC threshold monitor 1. (R/W)

**ADC_THRESH1_LOW** Configures the low threshold for HP ADC threshold monitor 1. (R/W)


## Register 62.15: ADC_THRESH_CTRL_REG (0x004C)

| Bit | Field         | Description                                                                 |
|-----|---------------|-----------------------------------------------------------------------------|
| 31  |               |                                                                             |
| 30  |               |                                                                             |
| 29  |               |                                                                             |
| 28  | ADC_THRESH0_EN |                                                                             |
|     | (reserved)    |                                                                             |
| 27  |               |                                                                             |
| 26  | ADC_THRESH1_EN |                                                                             |
|     | (reserved)    |                                                                             |
| 0   | Reset         |                                                                             |

**ADC_THRESH_ALL_EN** Configures whether to enable the threshold monitoring for all configured channels.
- O: Disable
- 1: Enable
(R/W)

**ADC_THRESH1_EN** Configures whether to enable threshold monitor 1.
- O: Disable
- 1: Enable
(R/W)

**ADC_THRESH0_EN** Configures whether to enable threshold monitor 0.
- O: Disable
- 1: Enable
(R/W)
```