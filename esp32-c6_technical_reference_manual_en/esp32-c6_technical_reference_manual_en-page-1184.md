

```markdown
Register 35.9. LEDC_CHn_HPOINT_REG (n: 0-5) (0x0004+0x14*n)

LEDC_HPOINT_CH0

| 31 | 20 | 19 | ... | 0 |
|-----|----|----|-----|---|
|     |    |    | Ox000 | Reset |

LEDC_HPOINT_CHn Configures the value of Hpoint. (R/W)

Register 35.10. LEDC_CHn_DUTY_REG (n: 0-5) (0x0008+0x14*n)

LEDC_DUTY_CH0

| 31 | 25 | 24 | ... | 0 |
|-----|----|----|-----|---|
|     |    |    | Ox00000 | Reset |

LEDC_DUTY_CHn Configures the initial value of Lpoint. (R/W)

Register 35.11. LEDC_CHn_DUTY_R_REG (n: 0-5) (0x0010+0x14*n)

LEDC_DUTY_CH0_R

| 31 | 25 | 24 | ... | 0 |
|-----|----|----|-----|---|
|     |    |    | Ox00000 | Reset |

LEDC_DUTY_CHn_R Represents the current duty cycle of the output signal on channel n. (RO)
```