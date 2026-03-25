

```markdown
| Scenario | Range                                                                 | Alarm                                                                 |
|----------|------------------------------------------------------------------------|-----------------------------------------------------------------------|
| 1        | ALARM_VALUE – TIMG_VALUE > 2^53                                       | Triggered                                                            |
| 2        | 0 < ALARM_VALUE – TIMG_VALUE ≤ 2^53                                   | Triggered when the up-down counter counts TIMG_VALUE up to ALARM_VALUE |
| 3        | 0 ≤ TIMG_VALUE – ALARM_VALUE < 2^53                                   | Triggered                                                            |

Table 15.4-2. Alarm Generation When Up-Down Counter Decrements

| Scenario | Range                                                                 | Alarm                                                                 |
|----------|------------------------------------------------------------------------|-----------------------------------------------------------------------|
| 5        | TIMG_VALUE – ALARM_VALUE > 2^53                                       | Triggered                                                            |
| 6        | 0 < TIMG_VALUE – ALARM_VALUE ≤ 2^53                                   | Triggered when the up-down counter counts TIMG_VALUE down to ALARM_VALUE |
| 7        | 0 ≤ ALARM_VALUE – TIMG_VALUE < 2^53                                   | Triggered                                                            |
| 8        | ALARM_VALUE – TIMG_VALUE ≥ 2^53                                       | Triggered when the up-down counter restarts counting down from the timer’s maximum value after reaching the minimum value and counts TIMG_VALUE down to ALARM_VALUE |

15.4.4 Timer Reload

A timer is reloaded when a timer's current value is overwritten with a reload value stored in the TIMG_TO_LOAD_LO and TIMG_TO_LOAD_HI fields that correspond to the lower 32-bits and higher 22-bits of the timer's new value, respectively. However, writing a reload value to TIMG_TO_LOAD_LO and TIMG_TO_LOAD_HI will not cause the timer's current value to change. Instead, the reload value is ignored by the timer until a reload event occurs. A reload event can be triggered either by a software instant reload or an auto-reload at alarm.

A software instant reload is triggered by the CPU writing any value to TIMG_TOLOAD_REG, which causes the timer's current value to be instantly reloaded. If TIMG_TO_EN is set, the timer will continue incrementing or decrementing from the new value. In this case, if TIMG_TO_ALARM_EN is set, the timer will still trigger alarms in scenarios listed in Table 15.4-1 and 15.4-2. If TIMG_TO_EN is cleared, the timer will remain frozen at the new value until counting is re-enabled.

An auto-reload at alarm will cause a timer reload when an alarm occurs, thus allowing the timer to continue incrementing or decrementing from the reload value. This is generally useful for resetting the timer's value when using periodic alarms. To enable auto-reload at alarm, the TIMG_TO_AUTORELOAD field should be set. If not enabled, the timer's value will continue to increment or decrement past the alarm value after an alarm.
```