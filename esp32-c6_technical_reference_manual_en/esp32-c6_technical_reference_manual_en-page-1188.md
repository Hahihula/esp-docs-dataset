

```markdown
Register 35.18. LEDC_CHn_GAMMA_WR_REG (n: 0-5) (0x0100+0x10*n)

| 31 | 30           | 21        | 20          | 11   | 10         | 1 | 0 |
|----|--------------|-----------|-------------|------|------------|---|---|
|    | (reserved)   | LEDC_CHn_GAMMA_DUTY_NUM |             |      |            |   |   |
|    |              |           |             |      |            |   |   |
| 0  | 0x0          | 0x0       |             | 0x0  | 0          | Reset |

LEDC_CHn_GAMMA_DUTY_INC Configures the direction of duty cycle fading for PWM signals on channel n.
O: Decrease.
1: Increase
(R/W)

LEDC_CHn_GAMMA_DUTY_CYCLE Configures the number of times the counter overflows per an duty cycle fade. (R/W)

LEDC_CHn_GAMMA_SCALE Configures the amount by which Lpointn increase or decrease each time. (R/W)

LEDC_CHn_GAMMA_DUTY_NUM Configures the number of fades in a duty cycle range. (R/W)
```

```markdown
Register 35.19. LEDC_CHn_GAMMA_WR_ADDR_REG (n: 0-5) (0x0104+0x10*n)

| 31 | ... | 4 | 3 | 0 |
|----|-----|---|---|---|
|    |     |   |   | Reset |

LEDC_CHn_GAMMA_WR_ADDR Configures LEDC channel n gamma RAM write address. (R/W)
```