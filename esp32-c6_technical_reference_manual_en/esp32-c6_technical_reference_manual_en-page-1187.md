
```markdown
Register 35.16. LEDC_INT_ENA_REG (0x00C8)

| Bit 31 | Bit 30 | Bit 29 | Bit 28 | Bit 27 | Bit 26 | Bit 25 | Bit 24 | Bit 23 | Bit 22 | Bit 21 | Bit 20 | Bit 19 | Bit 18 | Bit 17 | Bit 16 | Bit 15 | Bit 14 | Bit 13 | Bit 12 | Bit 11 | Bit 10 | Bit 9 | Bit 8 | Bit 7 | Bit 6 | Bit 5 | Bit 4 | Bit 3 | Bit 2 | Bit 1 | Bit 0 |
|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|
| (reserved) |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        | Reset |
| LEDC_OVF_CNT_CH5_INT_ENA | LEDC_OVF_CNT_CH4_INT_ENA | LEDC_OVF_CNT_CH3_INT_ENA | LEDC_OVF_CNT_CH2_INT_ENA | LEDC_OVF_CNT_CH1_INT_ENA | LEDC_OVF_CNT_CH0_INT_ENA | (reserved) |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |
| LEDC_DUTY_CHNG_END_CH5_INT_ENA | LEDC_DUTY_CHNG_END_CH4_INT_ENA | LEDC_DUTY_CHNG_END_CH3_INT_ENA | LEDC_DUTY_CHNG_END_CH2_INT_ENA | LEDC_DUTY_CHNG_END_CH1_INT_ENA | LEDC_DUTY_CHNG_END_CH0_INT_ENA |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |
| LEDC_TIMER5_OVF_INT_ENA | LEDC_TIMER4_OVF_INT_ENA | LEDC_TIMER3_OVF_INT_ENA | LEDC_TIMER2_OVF_INT_ENA | LEDC_TIMER1_OVF_INT_ENA | LEDC_TIMER0_OVF_INT_ENA |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |

LEDC_TIMERx_OVF_INT_ENA (x: 0-3) Write 1 to enable LEDC_TIMERx_OVF_INT. (R/W)

LEDC_DUTY_CHNG_END_CHn_INT_ENA (n: 0-5) Write 1 to enable
LEDC_DUTY_CHNG_END_CHn_INT. (R/W)

LEDC_OVF_CNT_CHn_INT_ENA (n: 0-5) Write 1 to enable LEDC_OVF_CNT_CHn_INT. (R/W)


Register 35.17. LEDC_INT_CLR_REG (0x00CC)

| Bit 31 | Bit 30 | Bit 29 | Bit 28 | Bit 27 | Bit 26 | Bit 25 | Bit 24 | Bit 23 | Bit 22 | Bit 21 | Bit 20 | Bit 19 | Bit 18 | Bit 17 | Bit 16 | Bit 15 | Bit 14 | Bit 13 | Bit 12 | Bit 11 | Bit 10 | Bit 9 | Bit 8 | Bit 7 | Bit 6 | Bit 5 | Bit 4 | Bit 3 | Bit 2 | Bit 1 | Bit 0 |
|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|
| (reserved) |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        | Reset |
| LEDC_OVF_CNT_CH5_INT_CLR | LEDC_OVF_CNT_CH4_INT_CLR | LEDC_OVF_CNT_CH3_INT_CLR | LEDC_OVF_CNT_CH2_INT_CLR | LEDC_OVF_CNT_CH1_INT_CLR | LEDC_OVF_CNT_CH0_INT_CLR | (reserved) |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |
| LEDC_DUTY_CHNG_END_CH5_INT_CLR | LEDC_DUTY_CHNG_END_CH4_INT_CLR | LEDC_DUTY_CHNG_END_CH3_INT_CLR | LEDC_DUTY_CHNG_END_CH2_INT_CLR | LEDC_DUTY_CHNG_END_CH1_INT_CLR | LEDC_DUTY_CHNG_END_CH0_INT_CLR |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |
| LEDC_TIMER5_OVF_INT_CLR | LEDC_TIMER4_OVF_INT_CLR | LEDC_TIMER3_OVF_INT_CLR | LEDC_TIMER2_OVF_INT_CLR | LEDC_TIMER1_OVF_INT_CLR | LEDC_TIMER0_OVF_INT_CLR |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |        |

LEDC_TIMERx_OVF_INT_CLR (x: 0-3) Write 1 to clear LEDC_TIMERx_OVF_INT. (WT)

LEDC_DUTY_CHNG_END_CHn_INT_CLR (n: 0-5) Write 1 to clear LEDC_DUTY_CHNG_END_CHn_INT.
(WT)

LEDC_OVF_CNT_CHn_INT_CLR (n: 0-5) Write 1 to clear LEDC_OVF_CNT_CHn_INT. (WT)
```