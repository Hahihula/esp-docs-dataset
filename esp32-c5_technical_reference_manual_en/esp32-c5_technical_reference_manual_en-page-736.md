

```markdown
Register 17.18. RTC_TIMER_DATE_REG (0x03FC)
```

| 31 | 30 | [Reserved] | 0 |
|----:|----:|:------------|---|
|   0 |     |             | Reset |

RTC_TIMER_DATE Version control register. (R/W)

RTC_TIMER_CLK_EN Configures RTC timer clock gating.
- 0: Support clock only when the application writes registers.
- 1: Always force the clock on for registers.
(R/W)
```