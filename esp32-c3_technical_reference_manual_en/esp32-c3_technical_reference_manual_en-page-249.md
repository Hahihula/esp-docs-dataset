

```markdown
Register 9.27. RTC_CNTL_REG (0x0080)

| Bit | Description |
|-----|-------------|
| 31  | RTC_CNTL_DIG_REG_CAL_EN<br>Set this bit to enable digital regulator calibration by software. (R/W) |
| 30  | RTC_CNTL_SCK_DCAP<br>Configures the RC_SLOW_CLK frequency. (R/W) |
| 29  | RTC_CNTL_REGULATOR_FORCE_PD<br>Set this bit to FPD the low-power voltage regulator, which means decreasing its voltage to 0.8 V or lower. (R/W) |
| 28  | RTC_CNTL_REGULATOR_FORCE_PU<br>Set this bit to FPU the low-power voltage regulator, which means increasing its voltage to higher than 0.8 V. (R/W) |
| ... | ... |

Register 9.28. RTC_CNTL_PWC_REG (0x0084)

| Bit | Description |
|-----|-------------|
| 31  | RTC_CNTL_PAD_FORCE_HOLD<br>Set this bit to force RTC pad into hold state. (R/W) |
```