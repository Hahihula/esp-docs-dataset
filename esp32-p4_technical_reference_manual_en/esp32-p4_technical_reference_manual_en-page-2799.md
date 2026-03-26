
```markdown
Chapter 55 LED PWM Controller (LEDC)

Register 55.18. LEDC_INT_CLR_REG (0x00CC)
| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  |
|     | Reset |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |

LEDC_TIMERx_OVF_INT_CLR (x: 0-3) Clear bit: Write 1 to clear LEDC_TIMERx_OVF_INT. (WT)

LEDC_DUTY_CHNG_END_Chn_INT_CLR (n: 0-7) Clear bit: Write 1 to clear LEDC_DUTY_CHNG_END_Chn_INT. (WT)

LEDC_OVF_CNT_Chn_INT_CLR (n: 0-7) Clear bit: Write 1 to clear LEDC_OVF_CNT_Chn_INT. (WT)

Register 55.19. LEDC_DATE_REG (0x0174)
| Bit | 31 | 28 | 27 | ... | 0 |
|-----|----|----|----|-----|---|
|     | 0  | 0  | 0  | Ox2303070 | Reset |

LEDC_LEDC_DATE Configures the version. (R/W)
```