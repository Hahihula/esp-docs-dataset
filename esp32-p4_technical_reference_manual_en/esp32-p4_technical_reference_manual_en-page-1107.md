

```markdown
Register 16.19. TIMG_RTCCALICFG1_REG (0x006C)

| Bit | Description                  |
|-----|------------------------------|
| 31  | TIMG_RTC_CALI_VALUE          |
|     |                              |
| 7   | (reserved)                   |
| 6   | TIMG_RTC_CALI_CYCLING_DATA_VLD | 1 | 0 |
|     | Reset                        | 0 | 0 | 0 | 0 |

TIMG_RTC_CALI_CYCLING_DATA_VLD Represents whether periodic frequency calculation is done.
- 0: Not done
- 1: Done (RO)

TIMG_RTC_CALI_VALUE Represents the value countered by XTAL_CLK when one-shot or periodic frequency calculation is done. It is used to calculate RTC slow clock's frequency. (RO)

Register 16.20. TIMG_RTCCALICFG2_REG (0x0080)

| Bit | Description                              |
|-----|------------------------------------------|
| 31  | TIMG_RTC_CALI_TIMEOUT_THRES             |
|     |                                          |
| 7   | (reserved)                               |
| 6   | TIMG_RTC_CALI_TIMEOUT_RST_CNT            |
| 3   | TIMG_RTC_CALI_TIMEOUT                    |
| 2   | (reserved)                               |
| 1   | Reset                                    |
| 0   |                                        |

TIMG_RTC_CALI_TIMEOUT Represents whether RTC frequency calculation is timeout.
- 0: No timeout
- 1: Timeout (RO)

TIMG_RTC_CALI_TIMEOUT_RST_CNT Configures the cycles that reset frequency calculation timeout. Measurement unit: XTAL_CLK. (R/W)

TIMG_RTC_CALI_TIMEOUT_THRES Configures the threshold value for the RTC frequency calculation timer. If the timer's value exceeds this threshold, a timeout is triggered. Measurement unit: XTAL_CLK. (R/W)
```