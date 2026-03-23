
```markdown
Register 32.9. LEDC_INT_RAW_REG (0x00CO)

| Bit | Field Name                             | Description                                                                 |
|-----|-----------------------------------------|-----------------------------------------------------------------------------|
| 31  | reserved                                |                                                                             |
| 30-26| LEDC_OVF_CNT_CH5_INT_RAW               |                                                                             |
| 25-21| LEDC_OVF_CNT_CH4_INT_RAW               |                                                                             |
| 20-16| LEDC_OVF_CNT_CH3_INT_RAW               |                                                                             |
| 15-11| LEDC_OVF_CNT_CH2_INT_RAW               |                                                                             |
| 10-6 | LEDC_OVF_CNT_CH1_INT_RAW               |                                                                             |
| 5-1  | LEDC_DUTY_CHNG_END_CH0_INT_RAW         |                                                                             |
| 0    | LEDC_TIMER0_OVF_INT_RAW                |                                                                             |

LEDC_TIMERx_OVF_INT_RAW Triggered when the timerx has reached its maximum counter value. (R/WTC/SS)

LEDC_DUTY_CHNG_END_CHn_INT_RAW Interrupt raw bit for channel n. Triggered when the gradual change of duty has finished. (R/WTC/SS)

LEDC_OVF_CNT_CHn_INT_RAW Interrupt raw bit for channel n. Triggered when the ovf_cnt has reached the value specified by LEDC_OVF_NUM_CHn. (R/WTC/SS)


Register 32.10. LEDC_INT_ST_REG (0x00C4)

| Bit | Field Name                             | Description                                                                 |
|-----|-----------------------------------------|-----------------------------------------------------------------------------|
| 31  | reserved                                |                                                                             |
| 30-26| LEDC_OVF_CNT_CH5_INT_ST                |                                                                             |
| 25-21| LEDC_OVF_CNT_CH4_INT_ST                |                                                                             |
| 20-16| LEDC_OVF_CNT_CH3_INT_ST                |                                                                             |
| 15-11| LEDC_OVF_CNT_CH2_INT_ST                |                                                                             |
| 10-6 | LEDC_OVF_CNT_CH1_INT_ST                |                                                                             |
| 5-1  | LEDC_DUTY_CHNG_END_CH0_INT_ST          |                                                                             |
| 0    | LEDC_TIMER0_OVF_INT_ST                 |                                                                             |

LEDC_TIMERx_OVF_INT_ST This is the masked interrupt status bit for the LEDC_TIMERx_OVF_INT interrupt when LEDC_TIMERx_OVF_INT_ENA is set to 1. (RO)

LEDC_DUTY_CHNG_END_CHn_INT_ST This is the masked interrupt status bit for the LEDC_DUTY_CHNG_END_CHn_INT interrupt when LEDC_DUTY_CHNG_END_CHn_INT_ENA is set to 1. (RO)

LEDC_OVF_CNT_CHn_INT_ST This is the masked interrupt status bit for the LEDC_OVF_CNT_CHn_INT interrupt when LEDC_OVF_CNT_CHn_INT_ENA is set to 1. (RO)
```