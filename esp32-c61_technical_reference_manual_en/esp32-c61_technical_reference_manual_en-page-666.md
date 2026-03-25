

```markdown
Register 15.9. RTC_TIMER_INT_ST_REG (0x002C)

RTC_TIMER_OVERFLOW_ST   The masked interrupt status of RTC_TIMER_OVERFLOW_INT (HP CPU).  
(RO)

RTC_TIMER_SOC_WAKEUP_INT_ST   The masked interrupt status of RTC_TIMER_CMPO_INT. (RO)
```

```markdown
Register 15.10. RTC_TIMER_INT_ENA_REG (0x0030)

RTC_TIMER_OVERFLOW_ENA   Write 1 to enable RTC_TIMER_OVERFLOW_INT (HP CPU). (R/W)

RTC_TIMER_SOC_WAKEUP_INT_ENA   Write 1 to enable RTC_TIMER_CMPO_INT. (R/W)
```

```markdown
Register 15.11. RTC_TIMER_INT_CLR_REG (0x0034)

RTC_TIMER_OVERFLOW_CLR   Write 1 to clear RTC_TIMER_OVERFLOW_INT (HP CPU). (WT)

RTC_TIMER_SOC_WAKEUP_INT_CLR   Write 1 to clear RTC_TIMER_CMPO_INT. (WT)
```