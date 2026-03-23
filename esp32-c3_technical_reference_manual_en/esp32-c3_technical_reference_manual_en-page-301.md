
```markdown
Register 11.18. TIMG_RTCCALICFG_REG (0x0068)

| Bit | Field Name                     | Description                                                                 |
|-----|---------------------------------|-----------------------------------------------------------------------------|
| 31  |                                 |                                                                             |
| 30  | TIMG_RTC_CALI_START_CYCLING    | Enables periodic frequency calculation. (R/W)                               |
| 29  | TIMG_RTC_CALI_CLK_SEL          | 0: RC_SLOW_CLK; 1: RC_FAST_DIV_CLK; 2: XTAL32K_CLK. (R/W)                   |
| 28  | TIMG_RTC_CALI_RDY              | Marks the completion of one-shot frequency calculation. (RO)                 |
| 27  | TIMG_RTC_CALI_MAX              | Configures the time to calculate the frequency of RTC_SLOW_CLK. Measurement unit: RTC_SLOW_CLK cycle. (R/W) |
| 26  | TIMG_RTC_CALI_START            | Set this bit to enable one-shot frequency calculation. (R/W)                 |

Register 11.19. TIMG_RTCCALICFG1_REG (0x006C)

| Bit | Field Name                                 | Description                                                                 |
|-----|---------------------------------------------|-----------------------------------------------------------------------------|
| 31  |                                         |                                                                             |
| 7   | TIMG_RTC_CALI_CYCLING_DATA_VLD             | Marks the completion of periodic frequency calculation. (RO)                 |
| 6   | TIMG_RTC_CALI_VALUE                        | When one-shot or periodic frequency calculation completes, read this value to calculate the frequency of RTC_SLOW_CLK. Measurement unit: XTAL_CLK cycle. (RO) |
```