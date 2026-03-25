

```markdown
Register 13.18. TIMG_RTCCALICFG_REG (0x0068)

| Bit | Field Name                  | Description                                                                 |
|-----|-----------------------------|-----------------------------------------------------------------------------|
| 31  | TIMG_RTC_CALI_START_CYCLING| Configures the frequency calculation mode.<br>0: one-shot frequency calculation<br>1: periodic frequency calculation (R/W) |
| 30  | TIMG_RTC_CALI_MAX           | Configures the time to calculate RTC slow clock's frequency. Measurement unit: XTAL_CLK (R/W) |
| 16  | TIMG_RTC_CALI_RDY           | Represents whether one-shot frequency calculation is done.<br>0: Not done<br>1: Done (RO) |
| 15  | reserved                    |                                                                             |
| 14  | TIMG_RTC_CALI_START_CYCLING |                                                                             |
| 13  | TIMG_RTC_CALI_MAX           |                                                                             |
| 12  | TIMG_RTC_CALI_RDY           |                                                                             |
| 11  | (reserved)                  |                                                                             |
| 0   | Reset                       | 0x01                                                                          |

TIMG_RTC_CALI_START_CYCLING Configures the frequency calculation mode.
- 0: one-shot frequency calculation
- 1: periodic frequency calculation
(R/W)

TIMG_RTC_CALI_RDY Represents whether one-shot frequency calculation is done.
- 0: Not done
- 1: Done
(RO)

TIMG_RTC_CALI_MAX Configures the time to calculate RTC slow clock's frequency.
Measurement unit: XTAL_CLK
(R/W)

TIMG_RTC_CALI_START Configures whether to enable one-shot frequency calculation.
- 0: Disable
- 1: Enable
(R/W)
```