

```markdown
Register 61.9. TSENS_WAKEUP_CTRL_REG (0x0024)

| Bit | Description |
|-----|-------------|
| 31  | TSNS_WAKEUP_MODE |
| 30  | TSNS_WAKEUP_EN |
| 29  | TSNS_WAKEUP_OVER_UPPER_TH |
| 28  | (reserved) |
| 27  | (reserved) |
| 26  | TSENS_WAKEUP_TH_HIGH |
| 25  | TSENS_WAKEUP_TH_LOW |
| 24  | Reset |
|     |             |

TSNS_WAKEUP_TH_LOW Configures the low threshold for temperature monitoring wake-up function. (R/W)

TSNS_WAKEUP_TH_HIGH Configures the high threshold for temperature monitoring wake-up function. (R/W)

TSNS_WAKEUP_OVER_UPPER_TH Represents whether the temperature output value exceeds the threshold.
- 0: The temperature output value is below the low threshold.
- 1: The temperature output value is above the high threshold. (RO)

TSNS_WAKEUP_EN Configures whether to enable temperature monitoring wake-up function.
- 0: Disable
- 1: Enable (R/W)

TSNS_WAKEUP_MODE Selects the wake-up mode for temperature monitoring. Valid only when TSNS_WAKEUP_EN = 1.
- 0: Absolute value mode
- 1: Change value mode (R/W)
```

```markdown
Register 61.10. TSENS_SAMPLE_RATE_REG (0x0028)

| Bit | Description |
|-----|-------------|
| 31  | (reserved) |
| 30  | (reserved) |
| 29  | (reserved) |
| 28  | (reserved) |
| 27  | (reserved) |
| 26  | (reserved) |
| 25  | (reserved) |
| 24  | TSENS_SAMPLE_RATE |
|     |             |

TSNS_SAMPLE_RATE Configures the sampling rate for hardware-triggered temperature monitoring. The sampling period = configured value × sensor’s working clock cycle. (R/W)
```