

```markdown
Register 11.46. RTC_TIMER_UPDATE_REG (0x0010)

| 31 | 30 | 29 | 28 | 27 | ... | reserved |
|----:|----:|----:|----:|----:|-----|----------|
| 0x0| 0x0| 0x0| 0x0|     | 0x0 |          |

RTC_TIMER_MAIN_TIMER_SYS_RST   Configures whether to trigger RTC timer upon system reset.
O: Do not trigger
1: Trigger
(R/W)

RTC_TIMER_MAIN_TIMER_SYS_STALL   Configures whether to trigger RTC timer when the CPU enters or exits stall state.
O: Do not trigger
1: Trigger
(R/W)

RTC_TIMER_MAIN_TIMER_XTAL_OFF    Configures whether to trigger RTC timer when PMU powers up or down the 40 MHz crystal.
O: Do not trigger
1: Trigger
(R/W)

RTC_TIMER_UPDATE   Configures whether to trigger RTC timer by software.
O: Do not trigger
1: Trigger
(R/W)
```

Register 11.47. RTC_TIMER_MAIN_BUFO_LOW_REG (0x0014)

```markdown
| 31 | ... | reserved |
|----|-----|----------|
|    |     |          |

RTC_TIMER_MAIN_BUFO_LOW   Register group O records the count value of the RTC timer, bit0 to bit31. (RO)
```

Espressif Systems

ESP32-H2 TRM (Version 1.1)

Submit Documentation Feedback
```