

```markdown
Register 17.11. RTC_TIMER_INT_ST_REG (0x002C)

| Bit | Description |
|-----|-------------|
| 31  | RTC_TIMER_SOC_WAKEUP_INT_ST<br>RTC_TIMER_OVERFLOW_ST |
| 30  | (reserved) |
| 29  | Reset |

RTC_TIMER_OVERFLOW_ST The masked interrupt status of RTC_TIMER_OVERFLOW_INT (HP CPU).<br>(RO)

RTC_TIMER_SOC_WAKEUP_INT_ST The masked interrupt status of RTC_TIMER_CMPO_INT.<br>(RO)


Register 17.12. RTC_TIMER_INT_ENA_REG (0x0030)

| Bit | Description |
|-----|-------------|
| 31  | RTC_TIMER_SOC_WAKEUP_INT_ENA<br>RTC_TIMER_OVERFLOW_ENA |
| 30  | (reserved) |
| 29  | Reset |

RTC_TIMER_OVERFLOW_ENA Write 1 to enable RTC_TIMER_OVERFLOW_INT (HP CPU).<br>(R/W)

RTC_TIMER_SOC_WAKEUP_INT_ENA Write 1 to enable RTC_TIMER_CMPO_INT.<br>(R/W)


Register 17.13. RTC_TIMER_INT_CLR_REG (0x0034)

| Bit | Description |
|-----|-------------|
| 31  | RTC_TIMER_SOC_WAKEUP_INT_CLR<br>RTC_TIMER_OVERFLOW_CLR |
| 30  | (reserved) |
| 29  | Reset |

RTC_TIMER_OVERFLOW_CLR Write 1 to clear RTC_TIMER_OVERFLOW_INT (HP CPU).<br>(WT)

RTC_TIMER_SOC_WAKEUP_INT_CLR Write 1 to clear RTC_TIMER_CMPO_INT.<br>(WT)
```