
```markdown
Chapter 32 LED PWM Controller (LEDC)

Register 32.7. LEDC_TIMERx_CONF_REG (x: 0-3) (0x0DA0+8*x)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 30  | LEDC_TIMERx_PARA_UP                                                         |
| 29  | LEDC_TIMERx_RST                                                              |
| 28  | LEDC_TIMERx_PAUSE                                                            |
| 27  | LEDC_CLK_DIV_TIMERx                                                         |
| 26  | (reserved)                                                                  |
| 25  | LEDC_TIMERx_DUTY_RES                                                        |

0x000 | D'xO
Reset

LEDC_TIMERx_DUTY_RES    This field is used to control the range of the counter in timer x. (R/W)

LEDC_CLK_DIV_TIMERx     This field is used to configure the divisor for the divider in timer x. The least significant eight bits represent the fractional part. (R/W)

LEDC_TIMERx_PAUSE       This bit is used to suspend the counter in timer x. (R/W)

LEDC_TIMERx_RST         This bit is used to reset timer x. The counter will show 0 after reset. (R/W)

LEDC_TIMERx_PARA_UP     Set this bit to update LEDC_CLK_DIV_TIMERx and LEDC_TIMERx_DUTY_RES. (WT)

Register 32.8. LEDC_TIMERx_VALUE_REG (x: 0-3) (0x00A4+8*x)

| Bit | Description |
|-----|-------------|
| 31  | (reserved)  |

LEDC_TIMERx_CNT    This field stores the current counter value of timer x. (RO)
```