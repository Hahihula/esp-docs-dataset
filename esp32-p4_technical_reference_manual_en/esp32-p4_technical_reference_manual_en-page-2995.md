

```markdown
Register 60.7. RTC_TOUCH_STATUS_15_REG (0x0050)

| 31 | 23 | 22 | 19 | 18 | 16 | 15 |
|-----|-----|-----|-----|-----|-----|-----|
| 0   | 0   | 0   | 0   | 0x0 | 0x0 |      |
|     |     |     |     |      |      | Reset |

RTC_TOUCH_SLP_DATA Indicates the touch_smooth_data or benchmark sampled by touch pin in sleep mode. (RO)

RTC_TOUCH_SLP_DEBOUNCE_CNT Indicates the cumulative number of consecutive touch or touch release detection by touch pin in sleep mode. (RO)

RTC_TOUCH_SLP_NN_CNT Indicates the cumulative number of consecutive instances where touch_smooth_data < benchmark – passive_noise_threshold has been detected by touch pin in sleep mode. (RO)


Register 60.8. RTC_TOUCH_STATUS_16_REG (0x0054)

| 31 | 24 | 23 | 16 | 15 | 8 | 7 |
|-----|-----|-----|-----|-----|---|---|
|     |     |     | 0x0 | 0x0 |   |   |
|     |     |     |      |      | Reset |

RTC_TOUCH_APPROACH_PAD2_CNT Indicates the cumulative number of samplings of touch pin 2 in proximity mode. (RO)

RTC_TOUCH_APPROACH_PAD1_CNT Indicates the cumulative number of samplings of touch pin 1 in proximity mode. (RO)

RTC_TOUCH_APPROACH_PADO_CNT Indicates the cumulative number of samplings of touch pin 0 in proximity mode. (RO)

RTC_TOUCH_SLP_APPROACH_CNT Indicates the cumulative number of samplings of the sleeping touch pin in proximity mode. (RO)
```