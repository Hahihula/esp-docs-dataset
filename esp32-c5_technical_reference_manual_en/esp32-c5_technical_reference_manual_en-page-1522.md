

```markdown
Register 40.16. LEDC_INT_ST_REG (0x00C4)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | (reserved) | LEDC_OVF_CNT_CH6_INT_ST | ... | Reset |

LEDC_TIMERx_OVF_INT_ST (x: 0-3) Masked status bit: The masked interrupt status of LEDC_TIMERx_OVF_INT_ST. Valid only when LEDC_TIMERx_OVF_INT_ENA is set to 1. (RO)

LEDC_DUTY_CHNG_END_CHn_INT_ST (n: 0-5) Masked status bit: The masked interrupt status of LEDC_DUTY_CHNG_END_CHn_INT. Valid only when LEDC_DUTY_CHNG_END_CHn_INT_ENA is set to 1. (RO)

LEDC_OVF_CNT_CHn_INT_ST (n: 0-5) Masked status bit: The masked interrupt status of LEDC_OVF_CNT_CHn_INT. Valid only when LEDC_OVF_CNT_CHn_INT_ENA is set to 1. (RO)


Register 40.17. LEDC_INT_ENA_REG (0x00C8)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | (reserved) | LEDC_OVF_CNT_CH6_INT_ENA | ... | Reset |

LEDC_TIMERx_OVF_INT_ENA (x: 0-3) Enable bit: Write 1 to enable LEDC_TIMERx_OVF_INT. (R/W)

LEDC_DUTY_CHNG_END_CHn_INT_ENA (n: 0-5) Enable bit: Write 1 to enable LEDC_DUTY_CHNG_END_CHn_INT. (R/W)

LEDC_OVF_CNT_CHn_INT_ENA (n: 0-5) Enable bit: Write 1 to enable LEDC_OVF_CNT_CHn_INT. (R/W)
```