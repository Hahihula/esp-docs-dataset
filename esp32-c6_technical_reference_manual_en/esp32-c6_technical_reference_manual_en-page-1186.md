
```markdown
Register 35.14. LEDC_INT_RAW_REG (0x00CO)

LEDC_TIMERX_OVF_INT_RAW(x: 0-3) The raw interrupt status of LEDC_TIMERX_OVF_INT.
(R/WTC/SS)

LEDC_DUTY_CHNG_END_CHn_INT_RAW(n: 0-5) The raw interrupt status of
LEDC_DUTY_CHNG_END_CHn_INT. (R/WTC/SS)

LEDC_OVF_CNT_CHn_INT_RAW(n: 0-5) The raw interrupt status of LEDC_OVF_CNT_CHn_INT.
(R/WTC/SS)


Register 35.15. LEDC_INT_ST_REG (0x00C4)

LEDC_TIMERX_OVF_INT_ST(x: 0-3) The masked interrupt status of LEDC_TIMERX_OVF_INT.
Valid only when LEDC_TIMERX_OVF_INT_ENA is 1. (RO)

LEDC_DUTY_CHNG_END_CHn_INT_ST(n: 0-5) The masked interrupt status of
LEDC_DUTY_CHNG_END_CHn_INT.
Valid only when LEDC_DUTY_CHNG_END_CHn_INT_ENA is 1. (RO)

LEDC_OVF_CNT_CHn_INT_ST(n: 0-5) The masked interrupt status of LEDC_OVF_CNT_CHn_INT.
Valid only when LEDC_OVF_CNT_CHn_INT_ENA is 1. (RO)
```