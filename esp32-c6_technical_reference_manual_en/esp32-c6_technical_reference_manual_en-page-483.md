

```markdown
Chapter 12 Low-Power Management

Register 12.64. RTC_TIMER_TARO_HIGH_REG (0x0004)

RTC_TIMER_MAIN_TIMER_TAR_ENO   Configures whether to generate interrupts for the target count value O of the RTC timer.
    O: Do not generate interrupts
    1: Generate interrupts
(R/W)

RTC_TIMER_MAIN_TIMER_TAR_HIGO   Configures the high 16 bits of the target count value O (48 bits total) of the RTC timer. (R/W)

Register 12.65. RTC_TIMER_TAR1_LOW_REG (0x0008)

RTC_TIMER_MAIN_TIMER_TAR_LOW1   Configures the low 32 bits of the target count value 1 (48 bits total) of the RTC timer. (R/W)
```