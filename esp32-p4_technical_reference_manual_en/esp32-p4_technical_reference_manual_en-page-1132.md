

```markdown
Register 18.5. RTC_TIMER_UPDATE_REG (0x0010)

RTC_TIMER_MAIN_TIMER_UPDATE   Configure to log the current time through software configuration. (WO)
RTC_TIMER_MAIN_TIMER_XTAL_OFF  Configure to enable RTC Timer to log the time when the crystal powers up or down. (R/W)
RTC_TIMER_MAIN_TIMER_SYS_STALL  Configure to enable the RTC Timer to log the time when the CPU enters or exits the stall state. (R/W)
RTC_TIMER_MAIN_TIMER_SYS_RST   Configure to enable RTC Timer to log the time of system reset. (R/W)

Register 18.6. RTC_TIMER_MAIN_BUFLO_LOW_REG (0x0014)

RTC_TIMER_MAIN_TIMER_BUFLO_LOW  Represent the low 32 bits of the cached value 0 in RTC Timer. (RO)
```