

```markdown
Register 13.18. TIMG_RTCCALICFG_REG (0x0068)

| Bit | Field Name                     | Description                                                                 |
|-----|---------------------------------|-----------------------------------------------------------------------------|
| 31  | TIMG_RTC_CALI_START_CYCLING    | Configures the frequency calculation mode.<br>0: one-shot frequency calculation<br>1: periodic frequency calculation.<br>(R/W) |
| 30  | TIMG_RTC_CALI_CLK_SEL          | Configures to select the clock to be calibrated.<br>0: RTC_SLOW_CLK<br>1: RC_FAST_DIV_CLK<br>2: XTAL32K_CLK<br>(R/W) |
| 16  | TIMG_RTC_CALI_RDY              | Represents whether one-shot frequency calculation is done.<br>0: Not done<br>1: Done<br>(RO) |
| 15  | TIMG_RTC_CALI_MAX              | Configures the time to calculate RTC slow clock's frequency.<br>Measurement unit: XTAL_CLK.<br>(R/W) |
| 14  | TIMG_RTC_CALI_START            | Configures whether to enable one-shot frequency calculation.<br>0: Disable<br>1: Enable<br>(R/W) |
```