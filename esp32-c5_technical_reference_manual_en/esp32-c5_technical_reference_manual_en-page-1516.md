

```markdown
Register 40.6. LEDC_CHn_GAMMA_CONF_REG (n: 0-5) (0x0100+0x4*n)
```

| bit 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|--------|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
| (reserved) |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    | LEDC_CHn_GAMMA_RESUME | LEDC_CHn_GAMMA_PAUSE | LEDC_CHn_GAMMA_ENTRY_NUM |
| 0x0    | Reset |

LEDC_CHn_GAMMA_ENTRY_NUM Configures the number of duty cycle fading ranges for LEDC channel n. (R/W)

LEDC_CHn_GAMMA_PAUSE Configures whether to pause duty cycle fading of LEDC channel n.
- 0: Invalid. No effect
- 1: Pause (WT)

LEDC_CHn_GAMMA_RESUME Configures whether to resume duty cycle fading of LEDC channel n.
- 0: Invalid. No effect
- 1: Resume (WT)
```