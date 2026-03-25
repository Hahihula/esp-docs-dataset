

```markdown
## 13.6 Registers

The addresses in this section are relative to Timer Group base address provided in Table 4.3-2 in Chapter 4 System and Memory.

### Register 13.1. TIMG_TOCONFIG_REG (0x0000)

| Bit | Description                  |
|-----|------------------------------|
| 31  | TIMG_TO_EN                   |
| 30  | TIMG_TO_INCREASE             |
| 29  | TIMG_TO_AUTORELOAD           |
| 28  | TIMG_TO_DIVIDER              |
|     |                              |
| 13  | TIMG_TO_DIVCNT_RST (reserved)|
| 12  | TIMG_TO_DIVCNT_RST           |
| 11  | TIMG_TO_ALARM_EN             |
| 10  | (reserved)                   |
| 9   | (reserved)                   |
|     |                              |
| 0   | Reset                        |

```
```markdown
TIMG_TO_ALARM_EN Configures whether to enable the Timer 0 alarm function. This bit will be automatically cleared once an alarm occurs.
- O: Disable
- 1: Enable
(R/W/SC)

TIMG_TO_DIVCNT_RST Configures whether to reset the Timer 0's clock divider counter.
- O: No effect
- 1: Reset (WT)

TIMG_TO_DIVIDER Represents the Timer 0 clock (TO_clk) prescaler value. (R/W)

TIMG_TO_AUTORELOAD Configures whether to enable the Timer 0 auto-reload function at the time of alarm.
- O: No effect
- 1: Enable (R/W)

TIMG_TO_INCREASE Configures the counting direction of the Timer 0 time-base counter.
- O: Decrease
- 1: Increase (R/W)

TIMG_TO_EN Configures whether to enable the Timer 0 time-base counter.
- O: Disable
- 1: Enable (R/W/SS/SC)
```