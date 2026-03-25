

```markdown
Register 35.22. LEDC_CHn_GAMMA_CONF_REG (n: 0-5) (0x0180+0x4*n)

| Bit | 31 | ... | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|------|---|---|---|---|---|---|---|---|
|     |    | (reserved) | LEDC_CHn_GAMMA_RESUME | LEDC_CHn_GAMMA_PAUSE | LEDC_CHn_GAMMA_ENTRY_NUM | Reset |
| Value | 0 | ... | 0 | 0 | 0 | 0x0 |

LEDC_CHn_GAMMA_ENTRY_NUM Configures the number of duty cycle ranges. Maximum value is 16. (R/W)

LEDC_CHn_GAMMA_PAUSE Configures whether or not to pause duty cycle fading.
- 0: Invalid. No effect
- 1: Pause (WT)

LEDC_CHn_GAMMA_RESUME Configures whether or not to resume duty cycle fading.
- 0: Invalid. No effect
- 1: Resume (WT)

Register 35.23. LEDC_DATE_REG (0x01FC)

| Bit | 31 | 28 | 27 | ... | 0 |
|-----|----|-----|----|------|---|
|     |    | (reserved) | LEDC_DATE | Reset |
| Value | 0 | 0 | 0 | Ox211150 | |

LEDC_LEDC_DATE Version control register. (R/W)
```