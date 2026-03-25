
```markdown
Register 31.16. LEDC_INT_ST_REG (0x00C4)

LEDC_TIMERx_OVF_INT_ST (x: 0-3) Masked status bit: The masked interrupt status of LEDC_TIMERx_OVF_INT_ST. Valid only when LEDC_TIMERx_OVF_INT_ENA is set to 1. (RO)

LEDC_DUTY_CHNG_END_ChINT_ST (n: 0-5) Masked status bit: The masked interrupt status of LEDC_DUTY_CHNG_END_ChINT. Valid only when LEDC_DUTY_CHNG_END_ChINT_ENA is set to 1. (RO)

LEDC_OVF_CNT_ChINT_ST (n: 0-5) Masked status bit: The masked interrupt status of LEDC_OVF_CNT_ChINT. Valid only when LEDC_OVF_CNT_ChINT_ENA is set to 1. (RO)


Register 31.17. LEDC_INT_ENA_REG (0x00C8)

LEDC_TIMERx_OVF_INT_ENA (x: 0-3) Enable bit: Write 1 to enable LEDC_TIMERx_OVF_INT. (R/W)

LEDC_DUTY_CHNG_END_ChINT_ENA (n: 0-5) Enable bit: Write 1 to enable LEDC_DUTY_CHNG_END_ChINT. (R/W)

LEDC_OVF_CNT_ChINT_ENA (n: 0-5) Enable bit: Write 1 to enable LEDC_OVF_CNT_ChINT. (R/W)
```