
```markdown
Register 35.14. LEDC_INT_RAW_REG (0x00CO)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     |    |    |    |    |    |    |    |    |    |    |    |    | (reserved) | LEDC_OVF_CNT_CH5_INT_RAW | LEDC_OVF_CNT_CH4_INT_RAW | LEDC_OVF_CNT_CH3_INT_RAW | LEDC_OVF_CNT_CH2_INT_RAW | LEDC_OVF_CNT_CH1_INT_RAW | LEDC_OVF_CNT_CH0_INT_RAW |    |    |    |    |    |    |    |    | Reset |
|     | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  |      |                                  |                                  |                                  |                                  |                                  |                                  |                                  |                                  |                                  |                                  |                                  |                                  |                                  |                                  |                                  |                                  |                                  |

LEDC_TIMERx_OVF_INT_RAW The raw interrupt status of LEDC_TIMERx_OVF_INT. (R/WTC/SS)

LEDC_DUTY_CHNG_END_CHn_INT_RAW The raw interrupt status of LEDC_DUTY_CHNG_END_CHn_INT. (R/WTC/SS)

LEDC_OVF_CNT_CHn_INT_RAW The raw interrupt status of LEDC_OVF_CNT_CHn_INT. (R/WTC/SS)


Register 35.15. LEDC_INT_ST_REG (0x00C4)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     |    |    |    |    |    |    |    |    |    |    |    |    | (reserved) | LEDC_OVF_CNT_CH5_INT_ST | LEDC_OVF_CNT_CH4_INT_ST | LEDC_OVF_CNT_CH3_INT_ST | LEDC_OVF_CNT_CH2_INT_ST | LEDC_OVF_CNT_CH1_INT_ST | LEDC_OVF_CNT_CH0_INT_ST |    |    |    |    |    |    |    |    | Reset |
|     | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  |      |                                  |                                  |                                  |                                  |                                  |                                  |                                  |                                  |                                  |                                  |                                  |                                  |                                  |                                  |                                  |                                  |                                  |

LEDC_TIMERx_OVF_INT_ST The masked interrupt status of LEDC_TIMERx_OVF_INT.
Valid only when LEDC_TIMERx_OVF_INT_ENA is 1. (RO)

LEDC_DUTY_CHNG_END_CHn_INT_ST The masked interrupt status of LEDC_DUTY_CHNG_END_CHn_INT.
Valid only when LEDC_DUTY_CHNG_END_CHn_INT_ENA is 1. (RO)

LEDC_OVF_CNT_CHn_INT_ST The masked interrupt status of LEDC_OVF_CNT_CHn_INT.
Valid only when LEDC_OVF_CNT_CHn_INT_ENA is 1. (RO)
```