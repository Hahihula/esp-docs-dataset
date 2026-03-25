

```markdown
Register 35.12. LEDC_TIMERx_CONF_REG (x: 0-3) (0x00A0+0x8*n)

| 31 | 27 | 26 | 25 | 24 | 23 | 22 | 5 | 4 | 0 |
|----|----|----|----|----|----|----|---|---|---|
|    | (reserved) | LEDC_TIMER0_PARA_UP | LEDC_TIMERx_RST | LEDC_TIMERx_PAUSE | LEDC_CLK_DIV_TIMERx | LEDC_TIMER0_DUTY_RES |
| 0 | 0 | 0 | 0 | 0 | 1 | 0 |    |    | Reset |

LEDC_TIMERx_DUTY_RES   Configures the duty cycle resolution (the width of the counter in timer n). (R/W)

LEDC_CLK_DIV_TIMERx   Configures the divisor for the divider in timer n.
The least significant eight bits represent the fractional part. The most significant ten bits represent the integer part. (R/W)

LEDC_TIMERx_PAUSE      Configures whether or not to suspend the counter in timer n.
0: Not suspend
1: Suspend
(R/W)

LEDC_TIMERx_RST        Configures whether or not to reset timer n (the counter will show 0 after reset).
0: Not reset
1: Reset
(R/W)

LEDC_TIMERx_PARA_UP     Configures whether or not to update LEDC_CLK_DIV_TIMERx and LEDC_TIMERx_DUTY_RES.
0: Invalid. No effect
1: Update
(WT)
```

Register 35.13. LEDC_TIMERx_VALUE_REG (x: 0-3) (0x00A4+0x8*n)

```markdown
| 31 | 20 | 19 | ... | 0 |
|----|----|----|-----|---|
|    | (reserved) | LEDC_TIMER0_CNT | Reset |

LEDC_TIMERx_CNT   Represents the current counter value of timer n. (RO)
```