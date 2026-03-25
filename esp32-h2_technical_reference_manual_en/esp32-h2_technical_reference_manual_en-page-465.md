

```markdown
## 13.3.2 54-bit Time-base Counter

The 54-bit time-base counter is based on TB_CLK and can be configured to increment or decrement via the TIMGn_TO_INCREASE field. The time-base counter can be enabled or disabled by setting or clearing the TIMGn_TO_EN field, respectively. When enabled, the time-base counter increments or decrements on each cycle of TB_CLK. When disabled, the time-base counter is essentially frozen. Note that the TIMGn_TO_INCREASE field can be changed no matter whether TIMGn_TO_EN is set or not, and this will cause the time-base counter to change direction instantly.

To read the 54-bit value of the time-base counter, the timer value must be latched to two registers before being read by the CPU (due to the CPU being 32-bit). By writing any value to the TIMGn_TOUPDATE_REG, the current value of the 54-bit timer starts to be latched into the TIMGn_TOLO_REG and TIMGn_TOHI_REG registers containing the lower 32-bits and higher 22-bits, respectively. When TIMGn_TOUPDATE_REG is cleared by hardware, it indicates the latch operation has been completed and current timer value can be read from the TIMGn_TOLO_REG and TIMGn_TOHI_REG registers. TIMGn_TOLO_REG and TIMGn_TOHI_REG registers will remain unchanged for the CPU to read in its own time until TIMGn_TOUPDATE_REG is written to again.

## 13.3.3 Alarm Generation

A timer can be configured to trigger an alarm when the timer’s current value matches the alarm value. An alarm will cause an interrupt to occur and (optionally) an automatic reload of the timer’s current value (see Section 13.3.4).

The 54-bit alarm value is configured using TIMGn_TOALARMLO_REG and TIMGn_TOALARMHI_REG, which represent the lower 32-bits and higher 22-bits of the alarm value, respectively. However, the configured alarm value is ineffective until the alarm is enabled by setting the TIMGn_TO_ALARM_EN field. To avoid alarm being enabled “too late” (i.e., the timer value has already passed the alarm value when the alarm is enabled), the hardware will trigger the alarm immediately if the current timer value is:

*   higher than the alarm value (within a defined range) when the up-down counter increments
*   lower than the alarm value (within a defined range) when the up-down counter decrements

Table 13.3-1 and Table 13.3-2 show the relationship among the current value of the timer, the alarm value, and when an alarm is triggered. The current time value and the alarm value are defined as follows:

*   TIMG_VALUE = {TIMGn_TOHI_REG, TIMGn_TOLO_REG}
*   ALARM_VALUE = {TIMGn_TOALARMHI_REG, TIMGn_TOALARMLO_REG}

Table 13.3-1. Alarm Generation When Up-Down Counter Increments

| Scenario | Range                                                                 | Alarm                          |
|----------|-----------------------------------------------------------------------|--------------------------------|
| 1        | ALARM_VALUE – TIMG_VALUE > 2^53                                      | Triggered                     |
| 2        | 0 < ALARM_VALUE – TIMG_VALUE ≤ 2^53                                  | Triggered when the up-down counter counts TIMG_VALUE up to ALARM_VALUE |
| 3        | 0 ≤ TIMG_VALUE – ALARM_VALUE < 2^53                                  | Triggered                     |
| 4        | TIMG_VALUE – ALARM_VALUE ≥ 2^53                                      | Triggered when the up-down counter restarts counting up from 0 after reaching the timer’s maximum value and counts TIMG_VALUE up to ALARM_VALUE |
```