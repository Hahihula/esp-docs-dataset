

```markdown
Register 16.18. TIMG_RTCCALICFG_REG (0x0068)

| Bit | Field Name                     | Description                                                                 |
|-----|--------------------------------|-----------------------------------------------------------------------------|
| 31  | TIMG_RTC_CALI_START_CYCLING   | Configures the frequency calculation mode.<br>0: One-shot frequency calculation<br>1: Periodic frequency calculation.<br>(R/W) |
| 30  | TIMG_RTC_CALI_RDY             | Represents whether one-shot frequency calculation is done.<br>0: Not done<br>1: Done<br>(RO) |
| 16  | TIMG_RTC_CALI_MAX             | Configures the time to calculate RTC slow clock's frequency.<br>Measurement unit: XTAL_CLK.<br>(R/W) |
| 15  | TIMG_RTC_CALI_START           | Configures whether to enable one-shot frequency calculation.<br>0: Disable<br>1: Enable<br>(R/W) |
| 14  | (reserved)                    |                                                                             |
| 13  | TIMG_RTC_CALI_RDY             |                                                                             |
| 12  | TIMG_RTC_CALI_START_CYCLING   |                                                                             |
| 11  | (reserved)                    |                                                                             |
| 10  | (reserved)                    |                                                                             |
| 9   | (reserved)                    |                                                                             |
| 8   | (reserved)                    |                                                                             |
| 7   | (reserved)                    |                                                                             |
| 6   | (reserved)                    |                                                                             |
| 5   | (reserved)                    |                                                                             |
| 4   | (reserved)                    |                                                                             |
| 3   | (reserved)                    |                                                                             |
| 2   | (reserved)                    |                                                                             |
| 1   | (reserved)                    |                                                                             |
| 0   | TIMG_RTC_CALI_START_CYCLING   |                                                                             |

TIMG_RTCCALICFG_REG Bit Field Descriptions:

- **TIMG_RTC_CALI_START_CYCLING**: Configures the frequency calculation mode.
  - 0: One-shot frequency calculation
  - 1: Periodic frequency calculation.
  - (R/W)

- **TIMG_RTC_CALI_RDY**: Represents whether one-shot frequency calculation is done.
  - 0: Not done
  - 1: Done
  - (RO)

- **TIMG_RTC_CALI_MAX**: Configures the time to calculate RTC slow clock's frequency.
  - Measurement unit: XTAL_CLK.
  - (R/W)

- **TIMG_RTC_CALI_START**: Configures whether to enable one-shot frequency calculation.
  - 0: Disable
  - 1: Enable
  - (R/W)
```