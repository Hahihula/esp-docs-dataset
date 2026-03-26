
```markdown
Register 55.16. LEDC_INT_ST_REG (0x00C4)

| Bit | Name                                 | Description                                                                 |
|-----|---------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                           |                                                                             |
| 30  | LEDC_OVF_CNT_CH7_INT_ST              | The masked interrupt status of LEDC_OVF_CNT_CH7_INT. Valid only when LEDC_OVF_CNT_CH7_INT_ENA is set to 1. (RO) |
| 29  | LEDC_OVF_CNT_CH6_INT_ST              |                                                                             |
| 28  | LEDC_OVF_CNT_CH5_INT_ST              |                                                                             |
| 27  | LEDC_OVF_CNT_CH4_INT_ST              |                                                                             |
| 26  | LEDC_OVF_CNT_CH3_INT_ST              |                                                                             |
| 25  | LEDC_OVF_CNT_CH2_INT_ST              |                                                                             |
| 24  | LEDC_OVF_CNT_CH1_INT_ST              |                                                                             |
| 23  | LEDC_OVF_CNT_CH0_INT_ST              |                                                                             |
| 22  | LEDC_DUTY_CHNG_END_CH7_INT_ST        | The masked interrupt status of LEDC_DUTY_CHNG_END_CH7_INT. Valid only when LEDC_DUTY_CHNG_END_CH7_INT_ENA is set to 1. (RO) |
| 21  | LEDC_DUTY_CHNG_END_CH6_INT_ST        |                                                                             |
| 20  | LEDC_DUTY_CHNG_END_CH5_INT_ST        |                                                                             |
| 19  | LEDC_DUTY_CHNG_END_CH4_INT_ST        |                                                                             |
| 18  | LEDC_DUTY_CHNG_END_CH3_INT_ST        |                                                                             |
| 17  | LEDC_DUTY_CHNG_END_CH2_INT_ST        |                                                                             |
| 16  | LEDC_DUTY_CHNG_END_CH1_INT_ST        |                                                                             |
| 15  | LEDC_DUTY_CHNG_END_CH0_INT_ST        |                                                                             |
| 14  | LEDC_TIMER3_OVF_INT_ST               | The masked interrupt status of LEDC_TIMER3_OVF_INT. Valid only when LEDC_TIMER3_OVF_INT_ENA is set to 1. (RO) |
| 13  | LEDC_TIMER2_OVF_INT_ST               |                                                                             |
| 12  | LEDC_TIMER1_OVF_INT_ST               |                                                                             |
| 11  | LEDC_TIMER0_OVF_INT_ST               |                                                                             |
| 10  | LEDC_DUTY_CHNG_END_CH7_INT_ENA       | (reserved)                                                                    |
| 9   | LEDC_DUTY_CHNG_END_CH6_INT_ENA       |                                                                             |
| 8   | LEDC_DUTY_CHNG_END_CH5_INT_ENA       |                                                                             |
| 7   | LEDC_DUTY_CHNG_END_CH4_INT_ENA       |                                                                             |
| 6   | LEDC_DUTY_CHNG_END_CH3_INT_ENA       |                                                                             |
| 5   | LEDC_DUTY_CHNG_END_CH2_INT_ENA       |                                                                             |
| 4   | LEDC_DUTY_CHNG_END_CH1_INT_ENA       |                                                                             |
| 3   | LEDC_DUTY_CHNG_END_CH0_INT_ENA       |                                                                             |
| 2   | LEDC_TIMER3_OVF_INT_ENA              | The enable bit for LEDC_TIMER3_OVF_INT. (R/W)                               |
| 1   | LEDC_TIMER2_OVF_INT_ENA              |                                                                             |
| 0   | LEDC_TIMER1_OVF_INT_ENA              |                                                                             |

LEDC_TIMERx_OVF_INT_ST (x: 0-3) Masked status bit: The masked interrupt status of LEDC_TIMERx_OVF_INT. Valid only when LEDC_TIMERx_OVF_INT_ENA is set to 1. (RO)

LEDC_DUTY_CHNG_END_CHn_INT_ST (n: 0-7) Masked status bit: The masked interrupt status of LEDC_DUTY_CHNG_END_CHn_INT. Valid only when LEDC_DUTY_CHNG_END_CHn_INT_ENA is set to 1. (RO)

LEDC_OVF_CNT_CHn_INT_ST (n: 0-7) Masked status bit: The masked interrupt status of LEDC_OVF_CNT_CHn_INT. Valid only when LEDC_OVF_CNT_CHn_INT_ENA is set to 1. (RO)


Register 55.17. LEDC_INT_ENA_REG (0x00C8)

| Bit | Name                                 | Description                                                                 |
|-----|---------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                           |                                                                             |
| 30  | LEDC_OVF_CNT_CH7_INT_ENA             | Enable bit: Write 1 to enable LEDC_OVF_CNT_CH7_INT. (R/W)                   |
| 29  | LEDC_OVF_CNT_CH6_INT_ENA             |                                                                             |
| 28  | LEDC_OVF_CNT_CH5_INT_ENA             |                                                                             |
| 27  | LEDC_OVF_CNT_CH4_INT_ENA             |                                                                             |
| 26  | LEDC_OVF_CNT_CH3_INT_ENA             |                                                                             |
| 25  | LEDC_OVF_CNT_CH2_INT_ENA             |                                                                             |
| 24  | LEDC_OVF_CNT_CH1_INT_ENA             |                                                                             |
| 23  | LEDC_OVF_CNT_CH0_INT_ENA             |                                                                             |
| 22  | LEDC_DUTY_CHNG_END_CH7_INT_ENA       | Enable bit: Write 1 to enable LEDC_DUTY_CHNG_END_CH7_INT. (R/W)            |
| 21  | LEDC_DUTY_CHNG_END_CH6_INT_ENA       |                                                                             |
| 20  | LEDC_DUTY_CHNG_END_CH5_INT_ENA       |                                                                             |
| 19  | LEDC_DUTY_CHNG_END_CH4_INT_ENA       |                                                                             |
| 18  | LEDC_DUTY_CHNG_END_CH3_INT_ENA       |                                                                             |
| 17  | LEDC_DUTY_CHNG_END_CH2_INT_ENA       |                                                                             |
| 16  | LEDC_DUTY_CHNG_END_CH1_INT_ENA       |                                                                             |
| 15  | LEDC_DUTY_CHNG_END_CH0_INT_ENA       |                                                                             |
| 14  | LEDC_TIMER3_OVF_INT_ENA              | Enable bit: Write 1 to enable LEDC_TIMER3_OVF_INT. (R/W)                   |
| 13  | LEDC_TIMER2_OVF_INT_ENA              |                                                                             |
| 12  | LEDC_TIMER1_OVF_INT_ENA              |                                                                             |
| 11  | LEDC_TIMER0_OVF_INT_ENA              |                                                                             |

LEDC_TIMERx_OVF_INT_ENA (x: 0-3) Enable bit: Write 1 to enable LEDC_TIMERx_OVF_INT. (R/W)

LEDC_DUTY_CHNG_END_CHn_INT_ENA (n: 0-7) Enable bit: Write 1 to enable LEDC_DUTY_CHNG_END_CHn_INT. (R/W)

LEDC_OVF_CNT_CHn_INT_ENA (n: 0-7) Enable bit: Write 1 to enable LEDC_OVF_CNT_CHn_INT. (R/W)
```