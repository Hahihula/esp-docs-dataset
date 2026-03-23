

```markdown
## Register 11.20. TIMG_RTCCALICFG2_REG (0x0080)

| Bit | Field Name                     | Description                                                                 |
|-----|---------------------------------|-----------------------------------------------------------------------------|
| 7   | TIMG_RTC_CALI_TIMEOUT_THRES    | Threshold value for the frequency calculation timer. If the timer's value exceeds this threshold, a timeout is triggered. (R/W) |
| 6   | TIMG_RTC_CALI_TIMEOUT_RST_CNT   | Cycles to reset frequency calculation timeout. (R/W)                         |
| 31  |                                 | Ox1fffff                                                                     |

TIMG_RTC_CALI_TIMEOUT Indicates frequency calculation timeout. (RO)

## Register 11.21. TIMG_INT_ENA_TIMERS_REG (0x0070)

| Bit | Field Name                     | Description                                                                 |
|-----|---------------------------------|-----------------------------------------------------------------------------|
| 31  |                                 | Reset                                                                       |

TIMG_TO_INT_ENA The interrupt enable bit for the TIMG_TO_INT interrupt. (R/W)
TIMG_WDT_INT_ENA The interrupt enable bit for the TIMG_WDT_INT interrupt. (R/W)

## Register 11.22. TIMG_INT_RAW_TIMERS_REG (0x0074)

| Bit | Field Name                     | Description                                                                 |
|-----|---------------------------------|-----------------------------------------------------------------------------|
| 31  |                                 | Reset                                                                       |

TIMG_TO_INT_RAW The raw interrupt status bit for the TIMG_TO_INT interrupt. (R/SS/WTC)
TIMG_WDT_INT_RAW The raw interrupt status bit for the TIMG_WDT_INT interrupt. (R/SS/WTC)
```