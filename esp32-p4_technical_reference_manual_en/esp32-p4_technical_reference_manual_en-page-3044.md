

```markdown
Register 62.12. ADC_FILTER_CTRL0_REG (0x003C)

| 31 | 30           | 24 | 23       | 19 | 18                 | 14 | 13                  |
|----|--------------|-----|----------|----|--------------------|-----|---------------------|
|    | ADC_FILTER_RESET |     |          |    | ADC_FILTER_CHANNEL0 |     | ADC_FILTER_CHANNEL1 |
|    |              | (reserved) |        |    |                    |     | (reserved)          |
| 0  | 0 0 0 0 0 0 0 | 0xd |         | 0xd |                     | 0   | 0 0 0 0 0 0 0       |

ADC_FILTER_CHANNEL0 Configures the ADC channel for filter 0. Value 0 ~ 7 corresponds to channel 0 ~ 7 in HP ADC1, value 10 ~ 15 corresponds to channel 0 ~ 5 in HP ADC2. (R/W)

ADC_FILTER_CHANNEL1 Configure the ADC channel for filter 1. Same as above. (R/W)

ADC_FILTER_RESET Configures whether to reset the filter.
0: No effect
1: Reset
(R/W)
```

```markdown
Register 62.13. ADC_THRESO_CTRL_REG (0x0044)

| 31 | 30           | 18 | 17       | 5   | 4                   | 0   |
|----|--------------|-----|----------|-----|--------------------|-----|
|    |              |     |          |     | ADC_THRESO_CHANNEL | (reserved) |
|    |              |     |          |     |                    | Reset |
| 0  | 0             |      | Ox1fff   | 13  |                     |

ADC_THRESO_CHANNEL Configures the ADC channel for threshold monitor 0. Value 0 ~ 7 corresponds to channel 0 ~ 7 in HP ADC1, value 10 ~ 15 corresponds to channel 0 ~ 5 in HP ADC2. (R/W)

ADC_THRESO_HIGH Configures the high threshold for HP ADC threshold monitor 0. (R/W)

ADC_THRESO_LOW Configures the low threshold for HP ADC threshold monitor 0. (R/W)
```