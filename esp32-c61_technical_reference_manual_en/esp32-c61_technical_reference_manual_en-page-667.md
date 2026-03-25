

```markdown
Register 15.12. RTC_TIMER_DATE_REG (0x03FC)
```

| 31 | 30 | 0 |
|----:|----:|---|
|   O |     | Reset |

RTC_TIMER_DATE Version control register. (R/W)

RTC_TIMER_CLK_EN Configures RTC timer clock gating.
- 0: Support clock only when the application writes registers.
- 1: Always force the clock on for registers.
(R/W)
```