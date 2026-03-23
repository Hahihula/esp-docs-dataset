

```markdown
## 14.6 Registers

The addresses in this section are relative to Timer Group base address provided in Table 5.3-2 in Chapter 5 System and Memory.

### Register 14.1. TIMG_TOCONFIG_REG (0x0000)

| Bit | Description                     |
|-----|----------------------------------|
| 31  | O                               |
| 30  | 1                              |
| 29  | 1                              |
| 28  | Ox01                            |
|     | TIMG_TO_DIVIDER                 |
|     | TIMG_TO_AUTORELOAD               |
|     | TIMG_TO_INCREASE                 |
|     | TIMG_TO_EN                      |
|     | (reserved)                      |
| 13  | TIMG_TO_DIVCNT_RST              |
| 12  | (reserved)                      |
| 11  | TIMG_TO_ALARM_EN                |
| 10  | O                               |
| 9   | O                               |
| ... | O                               |
| 0   | Reset                           |

**TIMG_TO_ALARM_EN** Configures whether or not to enable the timer 0 alarm function. This bit will be automatically cleared once an alarm occurs.
- 0: Disable
- 1: Enable (R/W/SC)

**TIMG_TO_DIVCNT_RST** Configures whether or not to reset the timer 0’s clock divider counter.
- 0: No effect
- 1: Reset (WT)

**TIMG_TO_DIVIDER** Represents the timer 0 clock (TO_clk) prescaler value. (R/W)

**TIMG_TO_AUTORELOAD** Configures whether or not to enable the timer 0 auto-reload function at the time of alarm.
- 0: No effect
- 1: Enable (R/W)

**TIMG_TO_INCREASE** Configures the counting direction of the timer 0 time-base counter.
- 0: Decrement
- 1: Increment (R/W)

**TIMG_TO_EN** Configures whether or not to enable the timer 0 time-base counter.
- 0: Disable
- 1: Enable (R/W/SS/SC)
```